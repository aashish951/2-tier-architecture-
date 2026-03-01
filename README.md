# 2-Tier AWS Architecture Project

## Problem Statement
Traditional single-server deployments create security risks 
as the database is directly exposed. This project solves that 
by separating the web and database layers using AWS best practices.

## Architecture
![Architecture Diagram](diagram.png)

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
[Add screenshots here]

## Region
Asia Pacific (Mumbai) - ap-south-1
