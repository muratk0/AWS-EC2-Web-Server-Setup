\# AWS EC2 Web Server Setup





\## Project Overview



This project demonstrates deploying a web server using Amazon EC2.



The goal of this project is to learn basic AWS cloud infrastructure, Linux server management, and web server deployment.





\## Architecture



User  

↓  

Internet  

↓  

Security Group  

↓  

EC2 Ubuntu Server  

↓  

Apache Web Server  

↓  

EBS Storage





\## AWS Services Used



\- Amazon EC2

\- IAM Role

\- Elastic Block Store (EBS)

\- Security Groups





\## Implementation Steps



## Implementation Steps & Proofs

### 1. EC2 Instance Setup
- Created an Ubuntu EC2 instance
- Configured SSH access with Key Pair
- Connected to the server using SSH

### 2. Security Configuration (Security Groups & IAM)
Configured Security Group rules to allow HTTP (Port 80) and restricted SSH (Port 22). Attached an IAM Role (`EC2-S3-ReadOnly-Role`) for secure permission management without hardcoding Access Keys.

![Security Configuration](screenshots/AWS%20IAM%20Role%20And%20Port%20Conf.jpeg)

### 3. Storage Configuration (EBS)
Created and attached an additional 8GB gp3 EBS volume. Formatted with `ext4` and mounted to `/data`.

```bash
# Format the volume and mount it to the directory
sudo mkfs.ext4 /dev/nvme1n1
sudo mkdir /data
sudo mount /dev/nvme1n1 /data

# Install and start Apache HTTP Server
sudo apt update
sudo apt install apache2 -y
sudo systemctl enable apache2
sudo systemctl start apache2

# Test IAM Role Permissions via AWS CLI
aws s3 ls





