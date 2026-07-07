

# AWS SAA Learning Journey 🚀

Hands-on preparation for the **AWS Certified Solutions Architect – Associate (SAA-C03)** exam — structured like a real engineering project, not just a notes folder: study log + working Infrastructure as Code + documented failures and tradeoffs.

![Status](https://img.shields.io/badge/status-in%20progress-yellow)
![AWS](https://img.shields.io/badge/AWS-SAA--C03-orange)
![IaC](https://img.shields.io/badge/IaC-Terraform-623CE4)

---

## 📖 About This Repo

This is not just a certification-notes dump. Each topic I study is paired with a **hands-on project built using Infrastructure as Code**, a documented architecture decision, and — where relevant — a writeup of what broke and how I fixed it. The goal is to walk into interviews able to *show*, not just *tell*.

---

## 📊 Progress Tracker

| Domain | Exam Weight | Status | Hands-on Project(s) |
|---|---|---|---|
| Domain 1: Design Secure Architectures | 30% | 🟡 In Progress | [01-vpc-multi-az](hands-on-projects/01-vpc-multi-az) |
| Domain 2: Design Resilient Architectures | 26% | ⬜ Not Started | - |
| Domain 3: Design High-Performing Architectures | 24% | ⬜ Not Started | - |
| Domain 4: Design Cost-Optimized Architectures | 20% | ⬜ Not Started | - |

**Legend:** ⬜ Not Started · 🟡 In Progress · ✅ Done · 🔁 Reviewed

---

## 📅 Study Log

| Date | Topic | Hours | Key Takeaway |
|---|---|---|---|
| 2026-07-07 | VPC subnets & routing | 2 | Public vs. private subnet routing depends on route table association with IGW/NAT, not subnet naming |

> Full log lives in [`study-log.md`](study-log.md) — updated after every study session.

---

## 🛠 Hands-on Projects

Each project includes: architecture diagram, IaC source, a written rationale for design decisions, and an estimated cost breakdown.

| Project | Services Used | Domain |
|---|---|---|
| [01 – VPC Multi-AZ](hands-on-projects/01-vpc-multi-az) | VPC, Subnets, IGW, NAT GW | Resilient |
| [02 – S3 + CloudFront Static Site](hands-on-projects/02-s3-cloudfront-static-site) | S3, CloudFront, ACM, Route 53 | High-Performing |
| [03 – Auto Scaling + ALB + RDS](hands-on-projects/03-autoscaling-alb-rds) | EC2, ASG, ALB, RDS Multi-AZ | Resilient |
| [04 – Serverless API](hands-on-projects/04-serverless-api-lambda-dynamodb) | Lambda, API Gateway, DynamoDB | Cost-Optimized |
| [05 – Disaster Recovery](hands-on-projects/05-disaster-recovery-multi-region) | Route 53 Failover, Cross-Region Replication | Secure/Resilient |

---

## 📁 Repo Structure

```
aws-saa-journey/
├── README.md
├── study-log.md
├── domains/                   # exam-domain-organized notes
│   ├── 01-secure-architectures/
│   ├── 02-resilient-architectures/
│   ├── 03-high-performing-architectures/
│   └── 04-cost-optimized-architectures/
├── hands-on-projects/         # real IaC projects, one per folder
├── diagrams/                  # architecture diagrams (draw.io/excalidraw exports)
├── cheat-sheets/              # quick-reference comparisons (S3 vs EBS vs EFS, etc.)
└── writeups/                  # "what broke and how I fixed it" postmortems
```

---

## 🧠 Cheat Sheets

Quick-reference comparisons live in [`cheat-sheets/`](cheat-sheets), e.g.:
- S3 vs EBS vs EFS
- SQS vs SNS vs EventBridge
- Security Groups vs NACLs
- RDS Multi-AZ vs Read Replicas

---

## 🔍 Writeups (Failures & Fixes)

The most valuable part of this repo. Real debugging notes, not polished tutorials:
- *(coming soon)* — Simulating an AZ failure in the multi-AZ VPC project
- *(coming soon)* — A misconfigured IAM policy and how least-privilege fixed it

---

## ⚙️ CI/CD

Every push to `hands-on-projects/**` triggers automated `terraform fmt` + `terraform validate` via GitHub Actions. See [`.github/workflows/validate-iac.yml`](.github/workflows/validate-iac.yml).

---

## 🎯 Exam Info

- **Exam:** AWS Certified Solutions Architect – Associate (SAA-C03)
- **Target date:** _add your target date here_
- **Study resources:** _add your course/book references here_

---

## 📬 Connect

If you're also prepping for SAA or have feedback on any of these projects, feel free to open an issue or discussion!
