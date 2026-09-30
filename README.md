### George Koufie

---

## 🚀 About Me
Cloud & DevOps engineer with a systems administration foundation — identity management, large-scale endpoint deployment, on-call incident response — building on **both AWS and Azure**: Terraform, CI/CD, Kubernetes, event-driven security automation, and measured disaster-recovery drills.


💼 [LinkedIn](https://www.linkedin.com/in/george-koufie) - 🎥 [YouTube](https://www.youtube.com/@cloudcapecoast) - 🌐 [Portfolio](https://georgekoufie.online)

---

## 🔭 Work & Collaboration
**I'm currently working on:**
- Measured disaster-recovery drills on both clouds, with RTO/RPO targets committed before each run and results published, misses included.

**I'm looking to collaborate on:**
- Open-source DevOps tooling, cloud automation, and CI/CD pipelines.

**I'm looking for help with:**
- Multi-cloud architecture and infrastructure automation projects.

**🌱 I'm currently learning:**
- Disaster recovery planning at scale across many applications, on AWS and Azure, and AI agent infrastructure governance patterns.

**💬 Ask me about:**
- AWS, Azure, Terraform, Kubernetes, CI/CD, DR drills, IAM security design, and using Claude Code to build real infrastructure.

**📫 How to reach me:**
- 📧 gkoufie224@gmail.com

**👨‍💻 All of my projects are available at:**
- 🔗 [GitHub Portfolio](https://github.com/gkoufie1?tab=repositories) - 🌐 [georgekoufie.online](https://georgekoufie.online)

---

## 🏆 Featured Projects

### 1. Azure Disaster Recovery Drills
**Description:** Two measured DR drills between West US and Central US, with targets committed before each run. An Azure Site Recovery VM failover (RTO 2m34s vs a 15-minute target, met; RPO 304 s vs a 5-minute target, missed by 4 s and diagnosed) and an Azure SQL failover group under a live write load (forced failover RTO 12.9 s vs a 60 s target, met; 21 rows lost vs a 5 s target, met). Built with Terraform, torn down and verified after each. The raw logs, including the failed measurement attempts, are in the repo.
**Tech Stack:** Azure Site Recovery, Azure SQL failover groups, Terraform, Azure CLI/REST, Python
**Repo:** [azure-dr-drill](https://github.com/gkoufie1/azure-dr-drill)

### 2. GitOps on EKS with a Measured DR Drill
**Description:** A GitOps-deployed service on EKS Fargate, backed by Aurora with IAM authentication, and a real disaster-recovery drill: the database was killed mid-traffic and restored, and recovery time was measured against a target set beforehand. Target RTO 2 minutes, measured 39.032 seconds, met. Torn down and independently verified at $0.
**Tech Stack:** EKS Fargate, Argo CD, Aurora, Terraform/Terragrunt, GitHub Actions (OIDC)
**Repo:** [eks-gitops-dr-drill](https://github.com/gkoufie1/eks-gitops-dr-drill)

### 3. AWS 503 Incident Response Lab
**Description:** A self-directed lab reproducing a real production symptom — an ALB returning 503s on specific endpoints — behind a Cloudflare-proxied domain. Deliberately broke it four distinct ways and captured each one's real diagnostic signature (502 connection refusal vs. 503 zero capacity vs. 504 security-group timeout vs. an application bug invisible to health checks). Built, diagnosed, and torn down in one session.
**Tech Stack:** Terraform, ALB, Target Groups, Cloudflare, CloudWatch
**Repo:** [sre-503-incident-lab](https://github.com/gkoufie1/sre-503-incident-lab)

### 4. AI Agent Governance Guardrail
**Description:** A Bedrock-hosted Claude agent that decides which tools to call — with every call enforced by AWS IAM, not application code. Proved it with a real red-team test: a simulated prompt-injected instruction pushed the agent toward two out-of-scope actions, and both were denied by IAM, with an independent audit trail confirming the denial happened at the infrastructure layer.
**Tech Stack:** Bedrock, Lambda, IAM, DynamoDB
**Repo:** [ai-agent-governance-guardrail](https://github.com/gkoufie1/ai-agent-governance-guardrail)

### 5. Event-Driven Security Guardrail
**Description:** An event-driven AWS security remediation pipeline that auto-detects and revokes risky infrastructure changes in real time via Lambda, with every attempt logged to a DynamoDB audit table. Validated the IAM-enforced access boundary through live and negative testing — confirming denial on out-of-scope resources, not just the happy path.
**Tech Stack:** EventBridge, Lambda, DynamoDB, IAM, Python
**Repo:** [aws-eventdriven-security-guardrail](https://github.com/gkoufie1/aws-eventdriven-security-guardrail)

### 6. Firmware CI/CD & Release Infrastructure
**Description:** A real Jenkins pipeline that builds TianoCore EDK2's OVMF — the actual open-source UEFI firmware real cloud providers use as VM BIOS — and boot-validates it in QEMU. Getting from a clean clone to a booting firmware image meant finding and fixing six real bugs, including a deprecated toolchain tag every online tutorial still references.
**Tech Stack:** Jenkins, EDK2/UEFI, QEMU, Git
**Repo:** [firmware-cicd-release-infra](https://github.com/gkoufie1/firmware-cicd-release-infra)

### 7. DevOps Incident Response Lab
**Description:** A hands-on Linux/AWS lab simulating five production incident types — disk full, broken service, networking failure, SSH failure, high CPU — with real simulation scripts, Ansible health-check automation, and diagnostic runbooks for each.
**Tech Stack:** Linux, AWS EC2, Bash, Ansible, Prometheus
**Repo:** [devops-incident-response-project](https://github.com/gkoufie1/devops-incident-response-project)

### 8. StoreTrack — Full CI/CD Pipeline with Jenkins & Kubernetes
**Description:** A React/Vite/Express/MongoDB inventory app with a full Jenkins pipeline — lint, test, SonarQube quality gate, Docker build, Kubernetes rollout.
**Tech Stack:** React, Vite, Express, MongoDB, Docker, Jenkins, Kubernetes, SonarQube
**Repo:** [cicd-jenkins-store](https://github.com/gkoufie1/cicd-jenkins-store)

### 9. Enterprise API Onboarding Platform (Azure API Management)
**Description:** A shared Azure API Management platform where onboarding a new API never touches the gateway itself — separate Terraform state for the platform (owns the one APIM instance) versus per-API onboarding (reads platform outputs, can't create, replace, or delete APIM). Verified the real Entra ID auth chain end-to-end: real app registrations, real client-credentials tokens, and a call through the live gateway confirmed by checking for the backend's own CORS headers in the response — proof the request actually reached it, not a synthetic 200 from the gateway. Applied, tested, and fully torn down the same session.
**Tech Stack:** Azure API Management, Terraform, Entra ID, GitHub OIDC
**Repo:** [cloud-api-workflow](https://github.com/gkoufie1/cloud-api-workflow)

### 10. VMware Provisioning Lab
**Description:** A nested VMware ESXi 8.0U3e lab (free license) with two VMs and a verified Ansible playbook. Diagnosed a real Hyper-V/VT-x conflict blocking nested virtualization, then confirmed — with the exact same API error appearing across four separate operations — that the free ESXi license blocks VM cloning, OVF deployment, raw datastore file copy, and even power/reconfigure on existing VMs via the API, while Terraform's `vsphere` provider crashes outright reading a VM (it assumes vCenter's tagging API, which doesn't exist on a standalone host). Pivoted the automation to what the host actually supports: `govc` for read-only inventory, Ansible over SSH for real configuration — hardened SSH, installed node_exporter, and deployed a Python health-check tool on a systemd timer, with its own verification and confirmed idempotency.
**Tech Stack:** VMware ESXi, VMware Workstation, govc, Ansible, Python, Terraform
**Repo:** [vmware-provisioning-lab](https://github.com/gkoufie1/vmware-provisioning-lab)

More real, verified projects — including a Kubernetes-based local LLM serving pipeline, an AI API gateway with real rate limiting and cost enforcement, and a FedRAMP/NIST-aligned landing zone — are on the [full portfolio](https://georgekoufie.online).

---

## 🧰 Skills
**Programming & Scripting:** `Python` • `Bash` • `JavaScript`

**Cloud & DevOps:** `AWS` • `Azure` • `VMware` • `Docker` • `Kubernetes` • `Jenkins` • `Terraform` • `GitHub Actions` • `Ansible` • `Linux`

**AWS Services:** `IAM` • `Lambda` • `API Gateway` • `DynamoDB` • `Cognito` • `EventBridge` • `Bedrock` • `CloudWatch` • `CloudTrail`

**Azure Services:** `Site Recovery` • `SQL Database failover groups` • `Recovery Services vault` • `API Management` • `Entra ID` • `Key Vault` • `Application Insights`

**Virtualization:** `VMware ESXi` • `VMware Workstation` • `govc` • `Nested Virtualization`

**CI/CD & Automation:** `Infrastructure as Code` • `CI/CD Pipelines` • `Agentic AI Workflows (Claude Code)`

**Monitoring & Logging:** `Prometheus` • `Grafana` • `Splunk`

**Databases:** `DynamoDB` • `MongoDB` • `PostgreSQL` • `MySQL`

---

## 📊 GitHub Stats
![George's GitHub stats](https://github-readme-stats.vercel.app/api?username=gkoufie1&show_icons=true&theme=radical)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=gkoufie1&layout=compact&theme=radical)

![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=gkoufie1&theme=radical)

---

## 💬 Connect with Me
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/george-koufie)
[![YouTube](https://img.shields.io/badge/-YouTube-FF0000?style=flat&logo=youtube)](https://www.youtube.com/@cloudcapecoast)
[![Email](https://img.shields.io/badge/-Email-D14836?style=flat&logo=gmail)](mailto:gkoufie224@gmail.com)

---

*"Build it real, verify it live, document what actually happened."*
