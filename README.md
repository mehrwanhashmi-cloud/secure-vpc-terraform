# Secure-VPC-with-Terraform

## Project Overview

This project builds a production-style AWS network using Terraform with minimal console usage. The architecture includes public and private subnets, an Internet Gateway, NAT Gateway, route tables, security groups, a bastion host, and a private EC2 instance.

## Architecture

Internet users connect only to the bastion host in the public subnet. The private EC2 instance has no public IP address and can only be accessed through the bastion host.

<img width="1600" height="1100" alt="secure-vpc-terraform-architecture" src="https://github.com/user-attachments/assets/586f1a7e-c1ec-42a8-98fb-51d5488cf94b" />

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
