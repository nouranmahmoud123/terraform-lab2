# Terraform Lab 2: AWS Infrastructure as Code


## Overview
Complete Terraform infrastructure with VPC, subnets (using count), and EC2 instances.

## Lab Requirements 
-  Variables for all arguments
-  Output public_ips: 3.231.94.61, 98.94.70.213
-  Output private_ips: 10.0.0.229, 10.0.1.141
-  Count used for 3 subnets
-  Full documentation and logs

## Infrastructure
- **VPC:** vpc-029495bb2003e8bec (10.0.0.0/16)
- **Subnets:** 3 created with count (10.0.0.0/24, 10.0.1.0/24, 10.0.2.0/24)
- **Instances:** 2 x t3.micro
- **Security Group:** sg-05f55eec40ebc2a12

## Access
- Instance 1: http://3.231.94.61
- Instance 2: http://98.94.70.213

## Files
- `main.tf` - Infrastructure code
- `variables.tf` - Variable definitions
- `outputs.tf` - Output definitions
- `terraform.tfvars` - Variable values
- `LAB_REPORT.md` - Detailed report
- `private_ip_log.txt` - Private IP documentation
