# Scalable Web Application – NLB and Auto Scaling

In this project, I deployed a scalable web application using Amazon EC2,
a Network Load Balancer (NLB), and an Auto Scaling Group.

This architecture is designed for high-performance and low-latency
traffic distribution at the network layer.

## AWS Services Used
- Amazon EC2
- Network Load Balancer (NLB)
- Auto Scaling Group
- Amazon VPC
- CloudWatch

## What I built
- A launch template for EC2 instances
- An Auto Scaling Group across multiple Availability Zones
- A Network Load Balancer to distribute traffic
- Health checks and automatic instance replacement
