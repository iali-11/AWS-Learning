# AWS Assignments

## 1) VPC & Networking

### Objective
- #### Creating a custom VPC with one public and one private subnet
- #### Setting up the correct routing for internet access 
- #### Deploying EC2 instances across them.

### Tasks
1. Create a custom VPC (One Public + Private Subnet)
2. Internet Access (IGW / NATGW) 
3. Route Tables (Public + Private)
4. Public EC2 Instance (Public IP) + Private EC2 instance (No IP) 
5. Security Groups (Public + Private)

## 2) Application Load Balancer

### Objective
- #### Deploy two EC2 instances behind an ALB.
- #### The ALB must handle all incoming traffic. 
- #### EC2 instances should not be accessible directly from the internet.

### Tasks
1. Two EC2 Instances (2 Different AZs)
2. Set Up the ALB (ALB in 2 Public Subnets)
3. Security Groups (HTTP Traffic)
4. Testing (ALB DNS name)
