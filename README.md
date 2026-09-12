### George Koufie

---

## 🚀 About Me
Cloud & DevOps engineer with a systems administration foundation — identity management, large-scale endpoint deployment, on-call incident response — now specializing in AWS infrastructure engineering: Terraform, CI/CD, Kubernetes, and event-driven security automation.

I build and ship real infrastructure using **Claude Code and agentic AI workflows** as a daily engineering practice, not a side experiment — pairing AI-accelerated development with hands-on verification of every result.

💼 [LinkedIn](https://www.linkedin.com/in/george-koufie) - 🎥 [YouTube](https://www.youtube.com/@cloudcapecoast) - 🌐 [Portfolio](https://georgekoufie.online)

---

## 🔭 Work & Collaboration
**I'm currently working on:**
- Real AWS infrastructure across IAM-enforced security automation, incident response, and agent/AI governance patterns.

**I'm looking to collaborate on:**
- Open-source DevOps tooling, cloud automation, and CI/CD pipelines.

**I'm looking for help with:**
- Multi-cloud architecture and infrastructure automation projects.

**🌱 I'm currently learning:**
- GitOps at scale (Argo CD), and AI agent infrastructure governance patterns.

**💬 Ask me about:**
- AWS, Terraform, Kubernetes, CI/CD, IAM security design, and using Claude Code to build real infrastructure.

**📫 How to reach me:**
- 📧 gkoufie224@gmail.com

**👨‍💻 All of my projects are available at:**
- 🔗 [GitHub Portfolio](https://github.com/gkoufie1?tab=repositories) - 🌐 [georgekoufie.online](https://georgekoufie.online)

---

## 🏆 Featured Projects

### 1. AWS 503 Incident Response Lab
**Description:** A self-directed lab reproducing a real production symptom — an ALB returning 503s on specific endpoints — behind a Cloudflare-proxied domain. Deliberately broke it four distinct ways and captured each one's real diagnostic signature (502 connection refusal vs. 503 zero capacity vs. 504 security-group timeout vs. an application bug invisible to health checks). Built, diagnosed, and torn down in one session.
**Tech Stack:** Terraform, ALB, Target Groups, Cloudflare, CloudWatch
**Repo:** [sre-503-incident-lab](https://github.com/gkoufie1/sre-503-incident-lab)

### 2. AI Agent Governance Guardrail
**Description:** A Bedrock-hosted Claude agent that decides which tools to call — with every call enforced by AWS IAM, not application code. Proved it with a real red-team test: a simulated prompt-injected instruction pushed the agent toward two out-of-scope actions, and both were denied by IAM, with an independent audit trail confirming the denial happened at the infrastructure layer.
**Tech Stack:** Bedrock, Lambda, IAM, DynamoDB
**Repo:** [ai-agent-governance-guardrail](https://github.com/gkoufie1/ai-agent-governance-guardrail)

### 3. Event-Driven Security Guardrail
**Description:** An event-driven AWS security remediation pipeline that auto-detects and revokes risky infrastructure changes in real time via Lambda, with every attempt logged to a DynamoDB audit table. Validated the IAM-enforced access boundary through live and negative testing — confirming denial on out-of-scope resources, not just the happy path.
**Tech Stack:** EventBridge, Lambda, DynamoDB, IAM, Python
**Repo:** [aws-eventdriven-security-guardrail](https://github.com/gkoufie1/aws-eventdriven-security-guardrail)

### 4. Firmware CI/CD & Release Infrastructure
**Description:** A real Jenkins pipeline that builds TianoCore EDK2's OVMF — the actual open-source UEFI firmware real cloud providers use as VM BIOS — and boot-validates it in QEMU. Getting from a clean clone to a booting firmware image meant finding and fixing six real bugs, including a deprecated toolchain tag every online tutorial still references.
**Tech Stack:** Jenkins, EDK2/UEFI, QEMU, Git
**Repo:** [firmware-cicd-release-infra](https://github.com/gkoufie1/firmware-cicd-release-infra)

### 5. DevOps Incident Response Lab
**Description:** A hands-on Linux/AWS lab simulating five production incident types — disk full, broken service, networking failure, SSH failure, high CPU — with real simulation scripts, Ansible health-check automation, and diagnostic runbooks for each.
**Tech Stack:** Linux, AWS EC2, Bash, Ansible, Prometheus
**Repo:** [devops-incident-response-project](https://github.com/gkoufie1/devops-incident-response-project)

### 6. StoreTrack — Full CI/CD Pipeline with Jenkins & Kubernetes
**Description:** A React/Vite/Express/MongoDB inventory app with a full Jenkins pipeline — lint, test, SonarQube quality gate, Docker build, Kubernetes rollout.
**Tech Stack:** React, Vite, Express, MongoDB, Docker, Jenkins, Kubernetes, SonarQube
**Repo:** [cicd-jenkins-store](https://github.com/gkoufie1/cicd-jenkins-store)

More real, verified projects — including a Kubernetes-based local LLM serving pipeline, an AI API gateway with real rate limiting and cost enforcement, and a FedRAMP/NIST-aligned landing zone — are on the [full portfolio](https://georgekoufie.online).

---

## 🧰 Skills
**Programming & Scripting:** `Python` • `Bash` • `JavaScript`

**Cloud & DevOps:** `AWS` • `Azure` • `Docker` • `Kubernetes` • `Jenkins` • `Terraform` • `GitHub Actions` • `Ansible` • `Linux`

**AWS Services:** `IAM` • `Lambda` • `API Gateway` • `DynamoDB` • `Cognito` • `EventBridge` • `Bedrock` • `CloudWatch` • `CloudTrail`

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
