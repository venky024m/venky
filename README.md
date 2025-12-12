Project 2: 3-Tier Web Application
Goal: Build a scalable, highly available web app architecture.

Architecture
Web Layer (Public): Application Load Balancer (ALB).
App Layer (Private): EC2 Instances in an Auto Scaling Group.
Data Layer (Private): RDS Database (Multi-AZ).
Steps
Create a VPC

Create a VPC with 2 Public Subnets and 4 Private Subnets (2 for App, 2 for DB).
Create an Internet Gateway and attach it.
Create a NAT Gateway for private instances to access the internet.
Set up Database

Create an RDS MySQL instance in the private DB subnets.
Enable Multi-AZ for high availability.
Launch App Servers

Create a Launch Template for your EC2 instances (install Apache/Nginx).
Create an Auto Scaling Group (ASG) using this template.
Place ASG in private app subnets.
Configure Load Balancer

Create an Application Load Balancer (ALB) in public subnets.
Point ALB to the Auto Scaling Group.
Key Concepts
VPC: Your private network in the cloud.
Subnets: Public for things the internet sees, Private for things it shouldn't.
Auto Scaling: Adds servers when busy, removes them when quiet.
Load Balancer: Distributes traffic evenly across servers.3- Tier Architecture
