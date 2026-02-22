# Assignment 2 - Application Load Balancer

### 1) Created a custom VPC
- Two Public/Private subnets in two different Availability Zones.
- Public Route Table with Destinations of the Loacl VPC and Internet Gateway.
- Private Route Table with destinations of Local VPC and NAT Gateway.
- Route Tables associated to relevant Subnets.
<img width="1182" height="473" alt="Screenshot 2026-02-21 at 14 04 34" src="https://github.com/user-attachments/assets/edf92cd1-ebaf-4946-acaa-8835b52cc739" />

## 2) Created Security Group for Application Load Balancer
<img width="1593" height="392" alt="Screenshot 2026-02-21 at 12 52 30" src="https://github.com/user-attachments/assets/d9d25da0-3174-4ef7-a4ad-23a4c2059002" />

## 3) Assigned correct Inbound and Outbound traffic
- Allowing HTTP Traffic into ALB, while allowing all traffic out.
<img width="1593" height="555" alt="Screenshot 2026-02-21 at 12 54 03" src="https://github.com/user-attachments/assets/92503fbe-de87-42f7-a06c-858cdaab8898" />

## 4)Created 1st EC2 instance
<img width="960" height="611" alt="Screenshot 2026-02-21 at 14 06 09" src="https://github.com/user-attachments/assets/929fd182-57fd-4832-bcf3-90f5ce59da23" />

## 5) Assigned correct VPC within a private subnet.
- Auto-assign public IP disabled.
<img width="905" height="316" alt="Screenshot 2026-02-21 at 14 06 48" src="https://github.com/user-attachments/assets/698761e3-6c41-4165-a15f-778b16a94a43" />

## 6) Create Security Group for the 1st EC2 instance
- Allowed HTTP traffic only from the ALBs Security Group, referencing the ALB SG.
<img width="905" height="533" alt="Screenshot 2026-02-21 at 14 07 29" src="https://github.com/user-attachments/assets/410af816-2f44-4511-b664-c199ab3a1560" />

## 7) Installed simple web server for internet access
- Different content than the 2nd instance for ALB testing
<img width="905" height="514" alt="Screenshot 2026-02-21 at 14 08 56" src="https://github.com/user-attachments/assets/9e5455dc-260c-495e-ab12-f407d10fa2cb" />

## 8) Launch 2nd EC2 instance
<img width="905" height="638" alt="Screenshot 2026-02-21 at 14 10 08" src="https://github.com/user-attachments/assets/476dfaa5-c86a-4aef-9a0c-2650dcf956d6" />

## 9) Assign correct VPC in another private Subnet within a different AZ
- Auto-assign public IP disabled
<img width="905" height="523" alt="Screenshot 2026-02-21 at 14 11 36" src="https://github.com/user-attachments/assets/bae8bd2b-670f-4519-b491-1425a0d3af14" />

## 10) Create SG for 2nd EC2 instance
- Also referencing ALB SG
<img width="905" height="523" alt="Screenshot 2026-02-21 at 14 12 22" src="https://github.com/user-attachments/assets/34cf618e-2241-4fc1-bf45-1ce1e1c08ef6" />

## 11) Install simple web server for internet access on 2nd EC2 instance
- Different content than the 1st instance for ALB testing
<img width="905" height="439" alt="Screenshot 2026-02-21 at 14 12 52" src="https://github.com/user-attachments/assets/f37fd563-ea39-451d-8451-99095b98450b" />

## 12) Create Target Group for ALB
- Assigned HTTP protocol on port 80
- Register both EC2 instances
- Configure a health check on the root path /
<img width="1593" height="826" alt="Screenshot 2026-02-21 at 12 33 11" src="https://github.com/user-attachments/assets/66160e11-a18d-4f0b-ba7a-6fa373ae1cf5" />

<img width="1593" height="853" alt="Screenshot 2026-02-21 at 12 49 51" src="https://github.com/user-attachments/assets/1b7e23d4-dc9c-4edb-bdc9-74fcb67bda78" />

## 13) Creating the Application Load Balancer
<img width="1593" height="705" alt="Screenshot 2026-02-21 at 12 50 20" src="https://github.com/user-attachments/assets/a5aaddaf-2c32-429e-bd6f-42d2754823f7" />

## 14) Assign ALB Security Group created earlier to the ALB
<img width="1186" height="200" alt="Screenshot 2026-02-22 at 14 05 40" src="https://github.com/user-attachments/assets/44a2eb0b-b73b-49d0-a894-0e45be1fb464" />

## 15) Assign HTTP listener and Target Group created to ALB 
<img width="1648" height="637" alt="Screenshot 2026-02-21 at 12 57 29" src="https://github.com/user-attachments/assets/f54af1a8-cd4d-4bb7-a5e4-7e4f797c6974" />

## 16) ALB Now Created!
<img width="1648" height="843" alt="Screenshot 2026-02-21 at 12 58 47" src="https://github.com/user-attachments/assets/21fe7eae-41d9-467b-aba2-221f63fa265d" />

## 17) EC2 instance registered are both healthy
<img width="1186" height="456" alt="Screenshot 2026-02-21 at 14 14 42" src="https://github.com/user-attachments/assets/6d23c3b4-a6db-4f29-bc2d-a4ac7a4d5da9" />

# 18) Visit ALB DNS name
- When page is refereshed, traffic alternates between both instances
<img width="1186" height="456" alt="Screenshot 2026-02-21 at 14 15 51" src="https://github.com/user-attachments/assets/8da1f1a6-53b2-41f8-a805-9acade0ecde3" />

<img width="1186" height="456" alt="Screenshot 2026-02-21 at 14 15 56" src="https://github.com/user-attachments/assets/7b81b985-487b-43ee-ac94-57517ab6558a" />
