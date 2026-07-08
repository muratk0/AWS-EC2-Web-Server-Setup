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



\### 1. EC2 Instance Setup



\- Created an Ubuntu EC2 instance

\- Configured SSH access with Key Pair

\- Connected to the server using SSH





\### 2. Apache Web Server Deployment



\- Installed Apache Web Server

\- Hosted a static webpage on the EC2 instance





\### 3. Security Configuration



Configured Security Group rules:



\- SSH (Port 22) for remote access

\- HTTP (Port 80) for web traffic





\### 4. IAM Role Configuration



\- Created an IAM Role

\- Attached the role to the EC2 instance for secure permission management





\### 5. Storage Configuration



\- Created and attached an additional EBS volume





\## Project Structure



