# 2-Tier AWS Architecture Project

## Problem Statement
Traditional single-server deployments create security risks 
as the database is directly exposed. This project solves that 
by separating the web and database layers using AWS best practices.

## Architecture
2-tier architecture.drawio.png
<img width="872" height="592" alt="2-tier architecture drawio" src="https://github.com/user-attachments/assets/7ff7982d-8bfa-46dd-b9bb-ebd3749fc522" />


## Services Used
- Amazon VPC (Custom - 10.0.0.0/16)
- EC2 (Web Server - Amazon Linux 2)
- Application Load Balancer (Multi-AZ)
- RDS MySQL (Private Subnet)
- Security Groups (ALB-SG, EC2-SG, RDS-SG)
- Internet Gateway
- Route Tables

## Architecture Flow
User → Internet Gateway → ALB → EC2 → RDS MySQL

## Key Design Decisions
- RDS placed in private subnet — not accessible from internet
- EC2 accessible only through ALB — not directly exposed
- Multi-AZ ALB for high availability
- Separate Security Groups for each layer

## Screenshots
EC2

<img width="1600" height="788" alt="image" src="https://github.com/user-attachments/assets/4ec1513e-dd88-4c32-97de-bbafef5f75a0" />

LOAD BALANCER
    <img width="1600" height="785" alt="image" src="https://github.com/user-attachments/assets/2149c084-a5c8-4246-93fc-19f6796f4668" />

RDS 
    <img width="1600" height="707" alt="image" src="https://github.com/user-attachments/assets/2b72364f-8bee-4b01-aa4e-e4d2a033f289" />

SECURITY GROUPS
    <img width="1600" height="776" alt="image" src="https://github.com/user-attachments/assets/fba33e8c-1d67-43e6-a9e4-01882e3768a0" />

SSH LOGIN
    <img width="1600" height="712" alt="image" src="https://github.com/user-attachments/assets/a09ada00-0a4a-415b-99d5-8952eac3e8ff" />

SUBNETS
    <img width="1600" height="779" alt="image" src="https://github.com/user-attachments/assets/d00df780-4c4a-43b2-83bf-150df5d430bf" />

TARGET GROUPS
    <img width="1600" height="772" alt="image" src="https://github.com/user-attachments/assets/59b3c3cd-25be-4b29-9027-59704a6bcaa5" />

VPC
    <img width="1600" height="792" alt="image" src="https://github.com/user-attachments/assets/b1d8bf28-9ccc-4fad-a637-89ea382d1b1a" />

WEB PAGE
   <img width="1600" height="566" alt="image" src="https://github.com/user-attachments/assets/f0f0a2cb-d6f0-483e-b580-da145094279e" />


## Region
Asia Pacific (Mumbai) - ap-south-1


