# 🚀 Project 4: Scalable Web App using ALB & Auto Scaling (AWS)

## 📌 Project Overview
This project demonstrates how to deploy a **highly available and scalable web application** using AWS services.  
It uses **EC2, Application Load Balancer (ALB), Auto Scaling Group, and Launch Template** to automatically manage traffic and maintain availability across multiple Availability Zones.

---

## 🏗️ Architecture Flow
User → Application Load Balancer → Target Group → EC2 Instances (Auto Scaling Group)

---

## ⚙️ AWS Services Used
- Amazon EC2
- Launch Template
- Auto Scaling Group (ASG)
- Application Load Balancer (ALB)
- Target Groups
- VPC (Default)

---

## 🚀 Launch Template Configuration
- Name: `WebAppTemplate`
- AMI: Amazon Linux 2023
- Instance Type: `t3.micro`
- VPC: Default VPC
- Availability Zones:
  - us-east-1a
  - us-east-1b

---

## ⚖️ Load Balancer Configuration
- Type: Application Load Balancer
- Target Group: `WebApp-TG`
- Listener: HTTP (Port 80)
- Internet-facing enabled
- Distributes traffic across multiple EC2 instances

---

## 📈 Auto Scaling Configuration
- Desired Capacity: 2
- Minimum Capacity: 1
- Maximum Capacity: 4

### 🔄 Behavior:
- Automatically launches new instances when traffic increases
- Terminates extra instances when traffic decreases
- Maintains desired capacity at all times

---

## ❤️ Health Checks
- Enabled on Target Group
- Unhealthy instances are automatically replaced
- Ensures high availability and fault tolerance

---

## 🧪 Testing Performed
- Accessed application using ALB DNS name
- Verified multiple EC2 instances running
- Checked load balancing across instances
- Tested instance failure recovery (auto replacement)

---

## 💰 Cost Information (Free Tier Usage)
This project is built using AWS Free Tier eligible services.

### 🟢 Free Tier Components:
- EC2 (t3.micro)
- Auto Scaling Group
- Launch Template
- VPC

### ⚠️ Paid Component:
- Application Load Balancer (ALB) may incur small charges if left running

---

## 🎯 Key Learning Outcomes
- How Auto Scaling works in real environments
- Load balancing using ALB
- High availability architecture design
- Multi-AZ deployment concept
- Basic AWS cost awareness

---

## 🧹 Cleanup Steps (Important)
To avoid AWS charges:
- Delete Auto Scaling Group
- Delete Launch Template
- Delete Target Group
- Delete Load Balancer (ALB)
- Terminate EC2 Instances

--