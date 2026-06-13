# Secure-VPC-with-Terraform

## Project Overview

This project builds a production-style AWS network using Terraform with minimal console usage. The architecture includes public and private subnets, an Internet Gateway, NAT Gateway, route tables, security groups, a bastion host, and a private EC2 instance.

## Business Use Cases

# Secure Internal Applications
Organizations can host internal systems such as HR, payroll, and inventory platforms within private subnets while providing controlled administrative access through a bastion host.

# Regulated Workloads
Financial, healthcare, and compliance-focused organizations can isolate sensitive workloads from direct internet exposure while maintaining secure management access.

# Enterprise Application Foundation
This architecture provides a scalable network foundation for multi-tier applications, enabling secure separation of public-facing services and private backend resources.

## Architecture

Internet users connect only to the bastion host in the public subnet. The private EC2 instance has no public IP address and can only be accessed through the bastion host.

<img width="1600" height="1100" alt="secure-vpc-terraform-architecture" src="https://github.com/user-attachments/assets/b6faa67c-6091-4bcf-a4df-fc4a6a2439d8" />

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

## Lessons Learned

- Learned how to provision AWS infrastructure using Infrastructure as Code (Terraform) instead of manual console-based deployment.

- Gained hands-on experience creating and managing AWS networking components including VPCs, public and private subnets, route tables, Internet Gateways, and NAT Gateways.

- Implemented a secure bastion host architecture to access private resources without exposing them directly to the internet.

- Learned how Security Groups control network access and how to troubleshoot connectivity between EC2 instances.

- Created and imported SSH key pairs for secure authentication to EC2 instances.

- Used Terraform outputs to expose important deployment information such as VPC IDs and instance IP addresses.

- Practiced validating infrastructure deployments through SSH connectivity testing and AWS CLI commands.

- Implemented Git version control and GitHub repository management for Infrastructure as Code projects.

- Learned how to use `.gitignore` to prevent Terraform state files, credentials, and sensitive data from being committed to source control.

- Improved troubleshooting skills by resolving Terraform deployment errors, IAM permission issues, SSH authentication problems, and Git merge conflicts.
