Claude

# Production Platform & SRE Reference Platform [![CI/CD Pipeline](https://github.com/Anyah11/production-platform-blueprint/actions/workflows/deploy.yml/badge.svg)](https://github.com/Anyah11/production-platform-blueprint/actions/workflows/deploy.yml) [![Kubernetes](https://img.shields.io/badge/Kube
PASTED
Read and updated memory

This README is good. It’s specific, honest about its limits, and the timings and roadmap make it read like real engineering. I drafted two LinkedIn messages to your contact above. Before you send one, fix these:
Broken links are the most likely problem. The README links to docs/adr/... and docs/challenges-log.md, but my files were named docs/decisions/... and docs/challenges.md. If you renamed them in the repo, you’re fine. If not, click each link on GitHub and fix any that give a 404.
The service port conflicts with itself. One line says the ServiceMonitor uses port http (8080), while the port-forward is svc/demo-api-svc 8080:80. Open k8s/deployment.yaml and check the Service’s port. If it’s 8080, the command should be 8080:8080. A reader who copies a command that fails will lose trust in the rest.
Check that the README matches deploy.yml. It says “Go static checks,” while the earlier version said “Go tests.” Use whichever the workflow actually runs. “Zero-downtime rolling deployment” is also a claim an interviewer may probe. “Rolling deployment” is safer unless you tested it.
The title repeats itself. “Production Platform & SRE Reference Platform” says “platform” twice. Try “SRE Reference Platform on AWS EKS.”
Add the OIDC tightening to your roadmap. The limitations list doesn’t mention it, but it’s the first thing a security-minded reviewer will notice. One bullet is enough: “Restrict the trust policy to main and use a read-only role for pull requests.”
Teardown gotcha. If github_oidc.tf is in the same Terraform state, terraform destroy also removes the deployer role, so the pipeline can’t deploy until you apply again. A line in your challenges log covers that. Also check for leftover ECR images and CloudWatch log groups after destroying, since your manual checklist doesn’t list them.
I couldn’t open your repo, so I’m judging this from the README text, and I haven’t confirmed that the screenshots or ADR files exist.
Once the links work, replace [Name] in the message and send it. The first message ends with a specific question, which is more likely to get a reply than a general request for feedback. Also add this repo to your profile README’s Projects list and pin it on your GitHub profile.
Assignment #2: Customizing Your Professional Development (10%)
This assignment is designed to deepen your awareness of your own professional growth and allow you to build on the learning objectives you set in Assignment #1. Select one professional development option from the list below that aligns with the goals you have set and your communication style. Each option encourages you to reflect critically, make connections between theory and practice, and articulate your growing professional competencies.
Choose ONE option below:
· Option 1 - Learning Objectives Reflection: Submit a 750-word essay or a 6–10 minute reflective video (upload a URL link to an unlisted YouTube, Reel, or TikTok video). Reflect on the learning objectives from Assignment #1 by addressing the following:
o Analyze your progress on each objective, including examples, effective strategies, challenges, and adjustments.
o Give specific examples of new or improved skills you've applied in the workplace, explaining how they advanced your learning objectives and support your future academic or career goals.
o Show how academic learning has informed your work, and how your workplace experience has deepened academic understanding.
· Option 2 - Job Portfolio/Job Application Documents: Create a professional portfolio using one of the following formats: curated website (ex. Canva, Notion, Wix, GitHub), résumé, CV, or LinkedIn profile. Your portfolio should showcase your experience, skills, and accomplishments in a digital format suitable for job or graduate school applications. Aim to present yourself as a strong candidate by highlighting relevant work, academic achievements, and transferable skills.
I want to submit my gitbhub profile url since ive been doing a lot of project recently and I also told the,m can you help me update the profile
Read memory, ran a command, shared files
I rebuilt profile-README to fit Option 2, which asks for experience, skills, accomplishments, and academic achievements in a form that suits job or grad-school applications. These are the sections:
Education: University of Lethbridge, expected May 2027, with your two academic projects: the house price prediction (DASC 4850) and the code reviewer recommendation system (CPSC 4210).
Experience: AIRI Foundation, Settle Ease Canada, and the Saturday Python class.
Featured projects: the production platform on EKS first, then the OIDC project, then your other repos.
Skills: your stack grouped by category, plus a line on transferable skills (teaching, documentation, debugging).
Certifications and connect links: AWS Solutions Architect – Associate and your LinkedIn.
Fill in the Experience section
This is the weakest part right now, and it matters because the assignment is about workplace learning. I only know your job titles, so I left an HTML comment under each role. Open the file and replace each comment with the dates plus two short bullets: what you teach or build, who it’s for, and one concrete result (a number if you have one, like learners taught or a course you built). Delete the comments afterward. If you skip this, the roles will show only as titles.
Check these before submitting
Repo link: I assumed king-county-housing is your DASC 4850 project. If it isn’t, remove that link.
GPA: I left it out. Include it only if you want to, since a reader will see the number without context.
Repos: make sure everything linked is public, and give each of the three smaller repos a one-line description. A stub repo with no README looks worse than leaving it out.
Pin six repos on your profile, starting with the production platform and the OIDC project. Use “Customize your pins” on your profile page.
Profile fields: set your name, photo, and a short bio under Settings > Public profile, for example: CS student at U of Lethbridge | Cloud, DevOps & SRE | AWS · Terraform · Kubernetes · Go.
Repo name: the README only shows if the repo is named exactly Anyah11. Push it the same way as before:
bash
   git add README.md
   git commit -m "Update profile README as portfolio"
   git push
Submitting
The URL to hand in is https://github.com/Anyah11. Open it in a private window afterward to check what your instructor will see: the README renders, the images load, and the pinned repos appear. The streak card sometimes fails to load, so if it breaks, delete that line.
The assignment also asks you to connect academic learning to your work. Since your instructor will see a portfolio rather than an essay, add one sentence under each teaching role about something you learned in class that you used there (or the reverse).
Profile readme
Document
·MD


Claude is AI and can make mistakes.

Profile readme · MD
# Kelechi Anyanwu
 
Computer Science student at the **University of Lethbridge** (graduating May 2027), building toward a career in **cloud, DevOps, and SRE** roles. I build and document cloud infrastructure projects on AWS, and I teach what I learn.
 
## 🎓 Education
 
**University of Lethbridge**, Computer Science (expected May 2027)
 
Selected coursework and academic projects:
- **House price prediction (DASC 4850):** regression modelling on the King County housing dataset using Ridge regression ([repo](https://github.com/Anyah11/king-county-housing))
- **Code reviewer recommendation system (CPSC 4210, group project):** built on the OpenStack MSR 2016 dataset; I developed the recommender engine
## 💼 Experience
 
**Instructor & Developer**, AIRI Foundation, Lethbridge
<!-- Add dates and 2 bullets: what you teach/build, who it's for, one concrete result -->
 
**IT Instructor**, Settle Ease Canada, Lethbridge, AB
<!-- Add dates and 2 bullets -->
 
**Co-instructor**, Saturday Python class for children
<!-- Add dates and 1 bullet -->
 
## 🚀 Featured projects
 
### [Production Platform & SRE Reference Platform](https://github.com/Anyah11/production-platform-blueprint)
An end-to-end platform on AWS: Terraform provisions a multi-AZ VPC and an EKS cluster, a GitHub Actions pipeline builds a Go service and deploys it using short-lived OIDC credentials (no stored AWS keys), and Prometheus and Grafana monitor it. I tested the alerting by injecting 5xx errors and recorded the timeline. The repo includes decision records, a challenges log, and an incident-simulation write-up.
 
`Terraform` · `AWS EKS` · `GitHub Actions` · `OIDC` · `Go` · `Docker` · `Prometheus` · `Grafana`
 
### [GitHub Actions to AWS with OIDC](https://github.com/Anyah11/github-actions-oidc-aws)
A CI/CD workflow that authenticates to AWS with short-lived OIDC tokens instead of stored access keys. The IAM role is locked to one repo and branch with least-privilege permissions, and the README documents how I debugged a trust-policy mismatch by inspecting the token's claims.
 
`GitHub Actions` · `AWS IAM` · `STS` · `OIDC` · `SSM`
 
### More repositories
- [api-cloud-automation](https://github.com/Anyah11/api-cloud-automation)
- [pig-farm-manager](https://github.com/Anyah11/pig-farm-manager)
- [king-county-housing](https://github.com/Anyah11/king-county-housing)
## 🛠️ Skills
 
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
 
Claude finished the response
