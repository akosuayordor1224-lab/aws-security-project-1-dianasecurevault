# aws-security-project-1-dianasecurevault
AWS IAM+S3 project implementing Least Privilege access for HR, Interns &amp; Admins.  Built with Free Tier. Demonstrates S3 bucket polices, IAM groups,and security best practice
# DianaSecureVault - AWS IAM Role-Based Access Project

## Problem Statement
Companies risk data leaks when interns, HR, and admins have the same file access. 
Example: Intern accidentally deletes CEO's payslip PDF = compliance violation + lawsuit.

## Solution Architecture
Used AWS IAM + S3 to enforce **Least Privilege Access** across 3 departments:

| IAM Group | Access Level | Policy File | Business Rule |
| --- | --- | --- | --- |
| HR-Team | Read payslip PDFs only | `hr-policy.json` | Prevents HR from accessing /admin/ or /submissions/ |
| Interns | Upload to /submissions only | `intern-policy.json` | Prevents delete/download of sensitive files |
| Admins | Full bucket access | `admin-policy.json` | Full control for Diana |

## AWS Services Used
- **Amazon S3** — Secure, scalable object storage for company files
- **AWS IAM** — Identity & Access Management, Groups, Custom Policies
- **AWS Security Model** — Default Deny, Principle of Least Privilege
- **AWS Well-Architected Framework** — Security Pillar implementation

## Project Cost
₦0/month — Built entirely on AWS Free Tier using S3 Standard + IAM (always free)## Project Cost

**Total Cost: ₦0 / $0.00 USD**

This project uses 100% AWS Free Tier services:
| Service | Free Tier Limit | Used in Project | Cost |
| --- | --- | --- | --- |
| Amazon S3 | 5GB storage | <1MB for JSON policies | $0 |
| AWS IAM | Unlimited users/groups/policies | 3 policies, 3 groups | $0 |
| Data Transfer | 1GB out/month | 0GB | $0 |

**Key Skill Demonstrated:** Building secure cloud architecture with zero billing risk. Critical for FinTech and startup roles in Lagos.

## Skills Demonstrated
1. Writing JSON IAM Policies for granular permissions
2. Implementing Role-Based Access Control (RBAC) 
3. S3 Bucket Security & Resource-Based Policies
4. AWS Default Deny security model
5. Translating business requirements into cloud architecture

## Architecture Diagram
