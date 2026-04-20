# aws-iam-security-project
Implemented a secure IAM architecture following AWS best practices, including role-based access control, MFA enforcement, and secure resource access using IAM roles.

## 🚀 Features
- Created IAM users and groups with role-based access control (RBAC)
- Enforced Multi-Factor Authentication (MFA) for all users
- Applied least privilege access using AWS managed policies
- Configured IAM role for EC2 to securely access S3 (no credentials required)
- Enabled AWS CloudTrail for auditing and monitoring all account activity

## 🏗️ Architecture
Users → IAM Groups → Policies → IAM Roles → EC2 → S3 → CloudTrail
<img width="1536" height="1024" alt="iam best practices" src="https://github.com/user-attachments/assets/88e21454-c160-41de-8c87-3681980df55a" />
This architecture demonstrates secure access flow where IAM users are assigned to groups with defined policies, and EC2 instances assume IAM roles to access AWS resources without exposing credentials. CloudTrail logs all activity for auditing and security.
## 🔧 Services Used
- AWS IAM (Users, Groups, Roles, Policies)
- Amazon EC2
- Amazon S3
- AWS CloudTrail

## 📸 Screenshots

### 👥 IAM Users & Groups
<img width="1916" height="942" alt="IAM USERS" src="https://github.com/user-attachments/assets/2cd7cd7f-ca95-4ca1-b017-b62cd481c591" />

### 🔐 MFA Enabled
<img width="1920" height="936" alt="mfa" src="https://github.com/user-attachments/assets/0650bb4d-bcb4-4530-8df3-21eaa34814d6" />

### 🔗 EC2 Role Attachment
<img width="1910" height="950" alt="iam role" src="https://github.com/user-attachments/assets/c10656e8-61e3-4cdf-b9d3-54826e8b612b" />

### 🧪 Test Output
<img width="1554" height="909" alt="test output" src="https://github.com/user-attachments/assets/f69bfc71-3e6b-48e9-beb9-34647a72924b" />

### 🔍 CloudTrail Logging
<img width="1912" height="946" alt="cloudtrail" src="https://github.com/user-attachments/assets/200b22de-a7a1-4be1-af66-5d954d200cb4" />

## 🔐 Security Best Practices Implemented
- Root account secured with MFA
- IAM users instead of root usage
- Role-based access control (RBAC)
- Least privilege permissions
- No hardcoded credentials
- Audit logging enabled with CloudTrail

## - Testing
- Connected to EC2 instance using EC2 Instance Connect
- Executed the following command:
  aws s3 ls
- Successfully retrieved S3 bucket list without using access keys, confirming IAM role-based access

## 💼 Why This Project Matters
This project demonstrates core AWS security concepts required for real-world cloud environments, including IAM management, secure access control, and audit logging. It reflects practical knowledge expected from entry-level cloud engineers and solutions architects.

## 📌 Outcome
Built a secure, production-style IAM setup demonstrating real-world AWS security practices and access control mechanisms.
