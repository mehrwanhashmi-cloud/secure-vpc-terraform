# Secure-VPC-with-Terraform

## Project Overview

This project builds a production-style AWS network using Terraform with minimal console usage. The architecture includes public and private subnets, an Internet Gateway, NAT Gateway, route tables, security groups, a bastion host, and a private EC2 instance.

## Architecture

Internet users connect only to the bastion host in the public subnet. The private EC2 instance has no public IP address and can only be accessed through the bastion host.

<img width="1600" height="1100" alt="secure-vpc-terraform-architecture" src="https://github.com/user-attachments/assets/b6faa67c-6091-4bcf-a4df-fc4a6a2439d8" />


##Screenshots

#Terraform Apply Success
<img width="960" height="506" alt="terraform apply" src="https://github.com/user-attachments/assets/8b781971-7953-4b7d-80b8-dcb7ca0afbb7" />

#Terraform Code
<img width="960" height="506" alt="terraform apply" src="https://github.com/user-attachments/assets/a835ec49-f554-436c-b0db-3d6d3e0a7fb8" />

#AWS VPC Resources
<img width="960" height="471" alt="aws console" src="https://github.com/user-attachments/assets/15ad4207-7aab-4233-9bcb-05b01f300ac4" />

#Bastion Host Connection
<img width="867" height="464" alt="bastion host" src="https://github.com/user-attachments/assets/0beaafd5-1e2b-4922-99dd-b01e501fc033" />

#Private EC2 Access
<img width="867" height="464" alt="private ec2 access" src="https://github.com/user-attachments/assets/82aa6fc6-7e16-4e21-93f9-4d1f62d01b51" />

## AWS Services Used

- Amazon VPC
- Public Subnets
- Private Subnets
- Internet Gateway
- NAT Gateway
- Elastic IP
- Route Tables
- Security Groups
- EC2
- Key Pair
- Terraform

## Architecture Flow

Internet
   |
Internet Gateway
   |
Public Subnet
   |
Bastion Host
   |
SSH
   |
Private Subnet
   |
Private EC2 Instance
