# ☁️ cloud-security-ops

A serious security engineering toolkit for building, automating, and defending cloud infrastructure in **AWS** and **Azure**. This repo covers provisioning, hardening, threat detection, and incident workflows — with deep coverage of **AWS GuardDuty**, **Azure Sentinel**, and detection-as-code.

## 🎯 Why This Repo Exists

You don’t "secure" the cloud with checkboxes. You **engineer** secure defaults, **automate detection**, and **respond with context**. This repo reflects that philosophy.

## 📁 Structure Overview

| Folder        | Description |
|---------------|-------------|
| `aws/`         | Terraform, Lambda, and detection engineering for AWS |
| `guardduty/`   | Enablement, auto-remediation, findings breakdowns, labs |
| `azure/`       | Bicep, KQL, and automation for securing Azure workloads |
| `shared/`      | Cross-cloud IAM principles, policies, and SBOM tools |
| `labs/`        | Simulated misconfigurations and alerting scenarios |
| `docs/`        | Threat models, incident playbooks, and cloud security notes |

## 🔍 Spotlight: AWS GuardDuty Coverage

- `enable-guardduty.tf`: Enable across regions with centralized results
- `threat-id-mapping.md`: Translate GuardDuty finding types into attacker goals
- `auto-remediation-lambda.py`: Sample Lambda to isolate EC2 on `UnauthorizedAccess:EC2/SSHBruteForce`
- `eventbridge-to-sns.tf`: Wire findings into notification or SOAR pipelines
- `detect-key-leak-eventbridge.md`: Trigger alerts when access keys leak
- `guardduty-key-leak-lab/`: Simulate a static key leak and validate detection + response

## 🛡️ Other Highlights

### 🟧 AWS
- Hardened EC2, IAM, and S3 provisioning with security-by-default
- Automation of key rotation, root login detection, CloudTrail alerting
- Custom config rules and remediation flows

### 🟦 Azure
- Secure VMs and storage accounts via Bicep and policy-as-code
- Defender for Cloud integration
- Sentinel playbooks and workbook templates

### 🧰 Shared Tools
- `syft-scan.sh`: SBOM generation and scanning
- `iam-checks/`: Account hygiene for both cloud providers
- `policy/`: NIST-based tagging and password hardening

## 🧪 Labs Included

| Lab                              | Purpose |
|----------------------------------|---------|
| `misconfigured-s3-lab/`           | Trigger GuardDuty from a public bucket |
| `guardduty-key-leak-lab/`         | Detect compromised keys in action |
| `sentinel-alerting-lab/`          | Build detection rules and dashboards in Azure |

## 🧠 Philosophy

> Detection is only as good as your understanding of what you're watching.

This repo reflects real engineering beliefs:
- Every misconfiguration is a signal waiting to be used
- You can't automate what you can't see
- Detection-as-code and prevention-as-default win long term

## 🧠 Ideal Use Cases

- Harden AWS or Azure from scratch
- Build SOC-style detections in cloud-native tools
- Simulate and practice cloud IR workflows
- Educate yourself or others on multi-cloud defense

## 🚧 Roadmap

- [ ] Add threat detection matrix by cloud provider
- [ ] Build a GuardDuty + Macie + EventBridge orchestration demo
- [ ] CI pipeline to detect IaC drift, exposed secrets, and IAM deltas
- [ ] Terraform modules for secure-by-default account baselining

