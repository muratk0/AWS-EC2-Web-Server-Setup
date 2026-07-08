\# AWS EC2 Web Server Setup Guide





\## 1. EC2 Instance Creation



\- Created an Ubuntu EC2 instance on AWS.

\- Configured Key Pair for SSH access.

\- Selected appropriate Security Group settings.





\## 2. SSH Connection



Connected to the EC2 instance using SSH.



Example:



ssh -i key.pem ubuntu@public-ip





\## 3. Apache Web Server Installation



Updated Ubuntu packages:



sudo apt update





Installed Apache:



sudo apt install apache2





Checked Apache service:



systemctl status apache2





\## 4. Security Group Configuration



Configured inbound rules:



\- SSH (Port 22) for remote access

\- HTTP (Port 80) for web traffic





\## 5. IAM Role



Created and attached an IAM Role to the EC2 instance

to provide secure AWS permission management.





\## 6. EBS Storage



Created and attached an additional EBS volume

to the EC2 instance.





\## Skills Learned



\- AWS EC2 management

\- Linux server administration

\- SSH usage

\- Apache deployment

\- Cloud security basics

\- Storage management with EBS

