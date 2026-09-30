# AWS Infrastructure-as-Code (IaC) Portfolio

Welcome to my cloud engineering portfolio. This repository showcases production-grade, modular AWS infrastructure provisioning and incident troubleshooting using **Terraform** and **AWS CloudShell**.

## 🛠️ Project Ecosystem

### Project 1: Automated Infrastructure Scripting
* **Objective:** Establish foundational multi-tier networking blocks utilizing infrastructure-as-code automation.
* **Core Tasks:** Provisioned isolated Virtual Private Clouds (VPCs), custom subnets, and state definitions.

### Project 2: Production-Grade Modular AWS Architecture Layouts
* **Objective:** Design a reusable, scalable root-and-module infrastructure strategy separating Development and Production logic.
* **Architecture Directory Structure:**
  ```text
  terraform-modular-aws/
  ├── modules/
  │   ├── vpc/             # Dynamic isolated network topology
  │   ├── security_groups/ # Layer 4 stateful firewall matrices
  │   ├── ec2/             # Web application tier hosting engine
  │   └── s3/              # Unique object storage bucket components
  └── environments/
      └── dev/             # Live validated target workspace environment
  ```
* **Key Achievements:** 
  * Successfully deployed modular infrastructure directly into the **AWS Hyderabad region (`ap-south-2`)**.
  * Dynamically queried regional architecture parameters using `data "aws_ami"` filters.
  * Implemented strict micro-instance constraints (`t3.micro`) to satisfy cloud-native cost control optimization.

### Project 3: Technical Incident Response & Validation Troubleshooting Labs
* **Objective:** Debug faulty configuration deployments mimicking real-world platform down incidents.
* **Scenario:** An unmapped subnet deployment threw a fatal parsing error blocking team operations.
* **Resolution Workflow:** 
  1. Ran native `terraform validate` sequences to isolate a `Missing required argument` compiler block.
  2. Diagnosed missing root network context linkages (`vpc_id`).
  3. Patched and mapped resource dependencies using tight semantic declarations to achieve a successful verification state: `Success! The configuration is valid.`

---

## 💻 Tech Stack & Tools Used
* **Cloud Platform:** Amazon Web Services (AWS)
* **Infrastructure-as-Code:** Terraform v1.5.7
* **Environments:** AWS CloudShell, Docker Container Runtime
* **OS Distribution Ecosystem:** Amazon Linux 2023, Ubuntu Server LTS

---

## 📈 Deployment Verification
All modules are fully validated, executed within real-world AWS accounts, and completely torn down via safe lifecycle destruction pipelines (`terraform destroy`) to ensure zero-cost infrastructure hygiene.
