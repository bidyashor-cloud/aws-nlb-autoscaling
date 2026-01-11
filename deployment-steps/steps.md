# Scalable Web Application Deployment – NLB and Auto Scaling

In this project, I deployed a scalable web application using a Network Load
Balancer and an Auto Scaling Group.

## What I did

1. I created a launch template using Amazon Linux.
2. I added a user data script to install and start Apache automatically.
3. I created a target group for the Network Load Balancer.
4. I created a Network Load Balancer in multiple Availability Zones.
5. I created an Auto Scaling Group using the launch template.
6. I attached the Auto Scaling Group to the target group.
7. I configured health checks so unhealthy instances are replaced automatically.
8. I tested the setup by accessing the NLB DNS name.

## User data script

```bash
#!/bin/bash
yum update -y
yum install httpd -y
systemctl start httpd
systemctl enable httpd
systemctl status httpd
echo "<h1>Welcome to the NLB Scalable Web App</h1>" > /var/www/html/index.html
