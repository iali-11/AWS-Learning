# Assignment 1 - VPC & Networking

## 1) Created my custom VPC
<img width="1211" height="437" alt="Screenshot 2026-02-17 at 11 41 40" src="https://github.com/user-attachments/assets/f7a96b4c-b7ae-46fa-85d1-46ac41e53dc8" />

## 2) Created Public Subnet within my custom VPC
   
<img width="1211" height="598" alt="Screenshot 2026-02-17 at 11 43 35" src="https://github.com/user-attachments/assets/fb380cb6-3822-4a99-b263-38bf0517fc99" />

## 3) Created Private Subnet within my custom VPC

<img width="1211" height="598" alt="Screenshot 2026-02-17 at 11 44 38" src="https://github.com/user-attachments/assets/451b9b74-5c24-4c85-abf8-80ef8e97b8c8" />

## 4) Created and attached custom Internet Gateway to custom VPC

<img width="1211" height="404" alt="Screenshot 2026-02-17 at 11 45 40" src="https://github.com/user-attachments/assets/d66a8abb-ceb1-4ee0-9c77-f5053a976b13" />

## 5) Allocated an Elastic IP

<img width="1211" height="404" alt="Screenshot 2026-02-17 at 11 46 01" src="https://github.com/user-attachments/assets/7c0dc7c5-3181-4844-9cdd-2609d4a181e6" />

## 6) Created custom NAT Gateway within Public Subnet, and Delegated Elastic IP to it

<img width="1211" height="363" alt="Screenshot 2026-02-17 at 11 46 53" src="https://github.com/user-attachments/assets/ddf6cde3-15bb-4d5f-81eb-149a1dd4e90b" />

## 7) Updated Private Route Table to target Local VPC and NAT Gateway

<img width="1211" height="562" alt="Screenshot 2026-02-17 at 11 49 01" src="https://github.com/user-attachments/assets/50e9adf5-49ed-498f-b308-0eaca7323ad5" />

## 8) Created a Public Route Table, and created targets to reach local VPC and Internet Gateway

<img width="1211" height="562" alt="Screenshot 2026-02-17 at 11 50 37" src="https://github.com/user-attachments/assets/432a79d8-0ae8-49e2-a493-3b6db52adecc" />

## 9) Edited Subnet association to reach correct route tables for Public and Private

<img width="1211" height="360" alt="Screenshot 2026-02-17 at 11 52 05" src="https://github.com/user-attachments/assets/7ba15c98-eacf-4ab8-ba33-4dff19c01e70" />

<img width="1211" height="412" alt="Screenshot 2026-02-17 at 11 52 24" src="https://github.com/user-attachments/assets/c39356ce-50e7-4174-910d-0008d5d87f41" />

## 10) Created a Key Pair for EC2 instances

<img width="637" height="610" alt="Screenshot 2026-02-17 at 11 54 43" src="https://github.com/user-attachments/assets/9e0e750a-d146-46a7-9e6c-a8fd6a0b2e7d" />

## 11) Assigned correct VPC and Subnet to Public EC2 instance
- Enabled Auto-assign IP to allow Address access.

<img width="637" height="272" alt="Screenshot 2026-02-17 at 11 55 38" src="https://github.com/user-attachments/assets/7f62f2b8-a0a1-49a2-a95b-166adf821139" />

## 12) Created  custom Security Groups for Public EC2 instance
- Allowing SSH/HTTP access from my IP only.

<img width="915" height="675" alt="Screenshot 2026-02-17 at 11 57 18" src="https://github.com/user-attachments/assets/9526f20f-f713-43d4-b399-91b563d7fa5c" />

## 13) Assigned correct VPC and Public Subnet when creating Private EC2 instance
- Disabled Auto-assign IP address.

<img width="915" height="278" alt="Screenshot 2026-02-17 at 12 11 16" src="https://github.com/user-attachments/assets/d1943bbc-617f-4d07-982d-33aa2f7051d7" />

## 14) Created custom Security Groups for Private EC2 Instance
- Referenced Public Security Groups to ensure internal access from Public EC2 instance.

<img width="915" height="677" alt="Screenshot 2026-02-17 at 12 12 49" src="https://github.com/user-attachments/assets/7ebc04f4-b9de-4629-98ec-019683dea832" />

## 15) Both Public and Private EC2 instances running

<img width="1193" height="711" alt="Screenshot 2026-02-17 at 12 13 39" src="https://github.com/user-attachments/assets/c3ea4918-c007-4dfc-a060-425b2efb8524" />

<img width="1193" height="711" alt="Screenshot 2026-02-17 at 12 13 49" src="https://github.com/user-attachments/assets/ed15c3c1-e1ed-4081-b603-8e1fa5b423ab" />

## 16) Public IP Error 
- When trying to access public IP, It came up with an error message saying the address was invalid.
- I quickly realised when creating the EC2 instance, I forgot to install a web server using user-data.
<img width="808" height="575" alt="Screenshot 2026-02-17 at 12 20 46" src="https://github.com/user-attachments/assets/55712b6a-7272-4d86-a9cf-bf1b162e6483" />

## 17) Installing User-data
- SSH into the Public EC2 instance and installed simple web server.
<img width="915" height="482" alt="Screenshot 2026-02-17 at 12 08 53" src="https://github.com/user-attachments/assets/ffca3b73-516f-4d06-b4c0-c78bfbf329f0" />

## 18) Address Page successfully working!

<img width="915" height="675" alt="Screenshot 2026-02-17 at 12 06 54" src="https://github.com/user-attachments/assets/c0393d2b-ca84-4fe9-a13d-02366efb0cb0" />