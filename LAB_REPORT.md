# Terraform Lab 2 - Infrastructure Report

## Lab Requirements ✅

### 1. Use Variables for All Arguments ✅
All infrastructure arguments are defined as variables in `variables.tf`:
- `aws_region`
- `vpc_cidr`
- `subnet_count`
- `instance_type`
- `ami_id`
- `instance_count`
- `environment`
- `enable_public_ip`

### 2. Output Public IP and Private IP ✅

**Public IPs:**
```
- Instance 1: 3.231.94.61
- Instance 2: 98.94.70.213
```

**Private IPs:**
```
- Instance 1: 10.0.0.229
- Instance 2: 10.0.1.141
```

### 3. Use Count for Creating Subnets ✅
3 subnets created using `count`:
```
- Subnet 1: 10.0.0.0/24 (subnet-0b4afb05c2358bac0)
- Subnet 2: 10.0.1.0/24 (subnet-0ec34172b180a0f1d)
- Subnet 3: 10.0.2.0/24 (subnet-027e451cffc2c5e23)
```

### 4. Screenshots ✅
Screenshots saved:
- `public_ip_access.png` - Public IP accessible in browser
- `terraform_output.png` - Terraform output showing all IPs
- `private_ip_logs.txt` - Private IP documentation

## Infrastructure Created

**VPC:**
- VPC ID: vpc-029495bb2003e8bec
- CIDR Block: 10.0.0.0/16

**Instances:**
- Count: 2 instances
- Type: t3.micro (free tier eligible)
- AMI: ami-026992d753d5622bc (Amazon Linux 2)

**Security:**
- Security Group: sg-05f55eec40ebc2a12
- Allows: HTTP (80), HTTPS (443), SSH (22)

**Internet Gateway:**
- IGW ID: igw-0da178dbdcbd69668

## Access

**Public Access (HTTP):**
- Instance 1: http://3.231.94.61
- Instance 2: http://98.94.70.213

**SSH Access:**
```bash
ssh -i your-key.pem ec2-user@3.231.94.61
ssh -i your-key.pem ec2-user@98.94.70.213
```

## Files Included
- `main.tf` - Main infrastructure code
- `variables.tf` - Variable definitions
- `outputs.tf` - Output definitions
- `terraform.tfvars` - Variable values
- `outputs.json` - JSON output
- `private_ip_log.txt` - Private IP documentation
- `LAB_REPORT.md` - This file

---
