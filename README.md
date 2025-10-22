# 🌐 AWS VPC Network Setup Project

## 🎯 Project Objective
Create a secure VPC architecture with public and private subnets, and deploy a Linux EC2 instance in the public subnet.

## 🏗️ Architecture Overview
```
Internet 🌍
    ↓
Internet Gateway 🚪
    ↓
Public Subnet (256 IPs) ⚡
    ↓
Linux EC2 Instance 🐧
    ↓
Private Subnet (256 IPs) 🔒
```

## 🛠️ Tech Stack
- **AWS VPC** - Virtual Private Cloud
- **AWS EC2** - Linux Instance
- **Internet Gateway** - Internet Connectivity
- **Route Tables** - Network Traffic Routing

## 🚀 Implementation Steps

### 1. Create VPC
- Create VPC with appropriate CIDR block (e.g., 10.0.0.0/16)

### 2. Create Internet Gateway
- Create and attach Internet Gateway to VPC

### 3. Create Subnets
- **Public Subnet**: 10.0.1.0/24 (256 IP addresses)
- **Private Subnet**: 10.0.2.0/24 (256 IP addresses)

### 4. Configure Route Tables
- Create public route table with route to Internet Gateway
- Associate public subnet with public route table
- Private subnet uses main route table (no internet access)

### 5. Launch EC2 Instance
- Launch Linux instance in public subnet
- Enable auto-assign public IP
- Configure security groups for SSH access

## 📁 Project Structure
```
AWS-VPC-Project/
├── README.md
└── Project-Steps.txt
```

## ⚙️ Configuration Details

### VPC Settings
- **CIDR Block**: 10.0.0.0/16
- **Tenancy**: Default

### Subnet Specifications
- **Public Subnet**: 10.0.1.0/24 (Availability Zone: us-east-1a)
- **Private Subnet**: 10.0.2.0/24 (Availability Zone: us-east-1b)

### EC2 Instance
- **OS**: Amazon Linux 2
- **Instance Type**: t2.micro
- **Subnet**: Public Subnet
- **Security Group**: Allow SSH (port 22)

## 📋 Submission Requirements

### 📸 Required Screenshots:
1. **VPC Created** - Showing VPC details
2. **Subnets Created** - Public and private subnets
3. **Route Tables** - Public route table with IGW route
4. **EC2 Instance** - Instance running in public subnet
5. **SSH Connection** - Successful connection to instance

### 🔗 URLs to Submit:
- GitHub Repository URL

## 🎯 Success Criteria
- ✅ VPC with Internet Gateway created
- ✅ Public and private subnets configured (256 IPs each)
- ✅ Route tables properly configured
- ✅ Linux EC2 instance launched in public subnet
- ✅ SSH access to EC2 instance verified

## 💡 Best Practices
- Use meaningful naming conventions
- Enable DNS hostnames in VPC
- Configure security groups minimally
- Test network connectivity

## 🎉 Output Link with Screenshot:
- https://docs.google.com/document/d/1Cxjr3lIjgPrMuDAdlIli_zPIno5bC7jFYfwV3wyxYSA/edit?usp=drive_link

---
