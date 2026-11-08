# Hi, I'm Kelechi 👋

Computer Science student at the **University of Lethbridge** (graduating May 2027), building toward a career in **cloud, DevOps, and SRE** roles. I build and document cloud infrastructure projects on AWS, and I teach what I learn.

## 🎓 Education

**University of Lethbridge**, Computer Science (expected May 2027)

- **House price prediction (DASC 4850):** Ridge regression on the King County housing dataset ([repo](https://github.com/Anyah11/king-county-housing))
- **Code reviewer recommendation system (CPSC 4210, group project):** developed the recommender engine using the OpenStack MSR 2016 dataset

## 💼 Experience

**Digital Media Support (Web Development), Applied Studies Placement**, LPIRG (Lethbridge Public Interest Research Group), Fall 2026
*Roots of Growth, a campus gardens and reconciliation project. Faculty-supervised placement for course credit (DGTR 4980).*

- Support the Roots of Growth website and web-based application as part of a two-person digital team
- Redesigning the project's reference campus map, marking active and intermittent garden sites and preparing design variations for supervisor review
- Writing a succession document so the next student can pick up the website and app

**Instructor & Developer**, AIRI Foundation, Lethbridge
<!-- Add dates and 2 bullets from your resume -->

**IT Instructor**, Settle Ease Canada, Lethbridge, AB
<!-- Add dates and 2 bullets from your resume -->

**Co-instructor**, Saturday Python class for children
<!-- Add dates and 1 bullet from your resume -->

## 🚀 Featured projects

### [Production Platform & SRE Reference Platform](https://github.com/Anyah11/production-platform-blueprint)
An end-to-end platform on AWS. Terraform provisions a multi-AZ VPC and an EKS cluster, a GitHub Actions pipeline builds a Go service and deploys it using short-lived OIDC credentials (no stored AWS keys), and Prometheus and Grafana monitor it. I tested the alerting by injecting 5xx errors: the alert fired about 1 minute 20 seconds after traffic began. The repo includes decision records, a challenges log, and an incident-simulation write-up.

`Terraform` · `AWS EKS` · `GitHub Actions` · `OIDC` · `Go` · `Docker` · `Prometheus` · `Grafana`

### [GitHub Actions to AWS with OIDC](https://github.com/Anyah11/github-actions-oidc-aws)
A CI/CD workflow that authenticates to AWS with short-lived OIDC tokens instead of stored access keys. The IAM role's trust policy is restricted to one repo and branch, and the README documents how I debugged a trust-policy mismatch by decoding the token's claims.

`GitHub Actions` · `AWS IAM` · `STS` · `OIDC` · `SSM`

### [AWS VPC with Terraform remote state](https://github.com/Anyah11/aws-vpc-terraform-remote-state)
An AWS VPC defined in Terraform with remote state.

`Terraform` · `AWS`

### More repositories
- [api-cloud-automation](https://github.com/Anyah11/api-cloud-automation)
- [pig-farm-manager](https://github.com/Anyah11/pig-farm-manager)
- [king-county-housing](https://github.com/Anyah11/king-county-housing)

## 🛠️ Tech stack

**Cloud and IaC**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazon-aws)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat&logo=terraform&logoColor=white)
![HashiCorp Vault](https://img.shields.io/badge/Vault-000000?style=flat&logo=vault&logoColor=white)

**Containers and CI/CD**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=github-actions&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat&logo=jenkins&logoColor=white)

**Observability**

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)
![Datadog](https://img.shields.io/badge/Datadog-632CA6?style=flat&logo=datadog&logoColor=white)

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat&logo=gnubash&logoColor=white)

**Transferable skills:** teaching and explaining technical topics to different audiences, technical documentation (decision records, runbooks, troubleshooting logs), and systematic debugging.

## 📜 Certifications

- AWS Certified Solutions Architect – Associate

## 📫 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin)](https://linkedin.com/in/kcee)

## 📊 GitHub

![Followers](https://img.shields.io/github/followers/Anyah11?style=flat&logo=github&label=Followers)

![Kelechi's contribution streak](https://streak-stats.demolab.com/?user=Anyah11&theme=radical&hide_border=true)
