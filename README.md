# Awesome-IAM-Policy-Access-Analysis

# Top IAM Policy & Access Analysis Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Permissions Analysis, Least Privilege Enforcement & Self-Hosted CIEM*  
**Last updated: October 2026**

This repository tracks notable **commercial IAM policy and access analysis platforms** and **open-source projects** that identify excessive permissions, detect unused access, and enforce least privilege across cloud and SaaS environments — from agentless CIEM platforms to policy-as-code analyzers.

**Examples** include AWS IAM Access Analyzer, Ermetic (Tenable), Wiz, Palo Alto Prisma Cloud, Orca Security, Britive, Sonrai Security, Check Point CloudGuard, PingSafe, and Microsoft Entra Permissions Management (the category leaders).

**Open-source emphasis**: IAM policy and access analysis is a growing open-source domain. **Cloudsplaining** leads as the de facto open-source AWS IAM analyzer with policy prioritization and risk scoring . **PMapper** brings graph-based privilege escalation detection for AWS IAM . **aws-iam-analyzer** provides an open-source alternative to Access Analyzer for on-premises environments and private AWS accounts . **Custodian** delivers policy-as-code for cloud governance . **Parliament** and **policy_sentry** handle IAM linting and least-privilege policy generation . **IAMSpy** enables continuous monitoring with attack path analysis and visualizations . **PMapper** and **Cloudsplaining** remain the core open-source CIEM toolset . This section is heavily expanded.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[AWS IAM Access Analyzer](https://aws.amazon.com/iam/access-analyzer/)**  
  **AWS's native IAM analysis service** — identifies resources shared with external entities and validates IAM policies . **Policy validation for grammar and best practices** . **Unused access findings** — identifies roles, users, and permissions not used in the last 90 days . **Custom policy checks** in CI/CD pipelines . **Best for AWS-native IAM analysis** .

- **[Ermetic (Tenable)](https://www.tenable.com/)**  
  **Cloud infrastructure entitlement management (CIEM) platform** — agentless analysis of multi-cloud permissions . **Detection of excessive permissions and privilege escalation paths** . **Best for multi-cloud entitlement management** .

- **[Wiz](https://www.wiz.io/)**  
  **CNAPP with CIEM capabilities** — graph-based attack path analysis including identity risks . **Effective permissions analysis across cloud providers** . **Best for unified cloud security with identity context** .

- **[Palo Alto Prisma Cloud](https://www.paloaltonetworks.com/prisma/cloud)**  
  **Comprehensive CNAPP with CIEM** — permissions analysis and least privilege enforcement . **Best for large enterprises** .

- **[Orca Security](https://orca.security/)**  
  **Agentless CNAPP with identity analysis** — detects excessive permissions and lateral movement paths . **Best for agentless cloud security** .

- **[Britive](https://www.britive.com/)**  
  **Cloud privileged access management** — just-in-time access and entitlement management . **Best for cloud PAM** .

- **[Sonrai Security](https://sonrai.com/)**  
  **Cloud permissions and identity management** — CIEM with identity graph analysis . **Best for cloud identity governance** .

- **[Check Point CloudGuard](https://www.checkpoint.com/)**  
  **Cloud security with CIEM** — posture management and entitlement analysis . **Best for Check Point ecosystem users** .

- **[PingSafe](https://www.pingsafe.com/)**  
  **Cloud security with IAM analysis** (acquired by SentinelOne) — agentless posture and permissions assessment . **Best for cloud security posture** .

- **[Microsoft Entra Permissions Management](https://www.microsoft.com/en-us/security/business/identity-access/microsoft-entra-permissions-management)**  
  **Microsoft's CIEM solution** — permissions analysis across AWS, Azure, and GCP . **Best for Microsoft-centric multi-cloud identity** .

## Open-Source GitHub Projects

### IAM Policy Analyzers

- **[Cloudsplaining](https://github.com/salesforce/cloudsplaining)**  
  **The de facto open-source AWS IAM security assessment tool**, BSD-3-Clause licensed with **2,900+ GitHub stars** . **Identifies violations of least privilege** in IAM policies and prioritizes them by risk . **Scans all AWS accounts, IAM users, groups, roles, and policies** — custom policies, inline policies, and AWS-managed policies . **Generates a security assessment report** with clickable HTML reports . **Policy prioritization** with risk scoring to focus remediation on highest-impact findings . **The most widely adopted open-source IAM analyzer** — used by security teams worldwide . **Best for AWS IAM policy analysis** .

- **[PMapper (Principal Mapper)](https://github.com/nccgroup/PMapper)**  
  **Rapidly identify and visualize AWS IAM privilege escalation and resource exposure**, GPL-3.0 licensed with **1,700+ GitHub stars** . **Creates a graph of IAM principals (users and roles) and their access to AWS resources** . **Offline graph queries** for exploring relationships and identifying privilege escalation paths . **Preset queries** for common questions like "Who can access S3 buckets?" and "Which principals can become admin?" . **Interactive visualization** via query command . **The reference tool for AWS IAM privilege escalation analysis** . **Best for identifying privilege escalation paths** .

- **[aws-iam-analyzer](https://github.com/awslabs/aws-iam-analyzer)**  
  **Open-source alternative to AWS IAM Access Analyzer**, Apache-2.0 licensed . **Detects resources shared with external entities** — S3 buckets, IAM roles, KMS keys, Lambda functions, SQS queues, Secrets Manager secrets . **Local analysis without external dependencies** — runs on-premises or in AWS accounts without Access Analyzer . **Transitive access analysis** — detects resource sharing with entities that can access other shared resources . **Findings in JSON format** with wildcard analysis (resource policies, ACLs, service principals, principals with wildcard access) . **Infrastructure-as-Code policy support** — analyze policies without deploying to AWS, with fixed tokens for variables . **Best for private AWS accounts and IaC validation** .

### Least Privilege & Policy Generation

- **[Policy Sentry](https://github.com/salesforce/policy_sentry)**  
  **IAM Least Privilege Policy Generator**, BSD-3-Clause licensed with **2,000+ GitHub stars** . **Reverse-engineers and creates IAM policies** from API calls or CloudTrail activity . **Escalation templates** for identifying privilege escalation risks . **Access Advisor and CloudTrail audit modes** — generate least-privilege policies from actual usage . **Query mode** for exploring IAM permissions . **Best for least privilege policy generation** .

- **[Parliament](https://github.com/duo-labs/parliament)**  
  **AWS IAM linting library**, BSD-3-Clause licensed with **1,200+ GitHub stars** . **Offline linting of IAM policies, S3 bucket policies, resource policies, and service control policies** . **Automatic policy checking** with configurable severity levels . **CI/CD integration** for policy validation before deployment . **Best for IAM policy linting** .

- **[Custodian](https://github.com/cloud-custodian/cloud-custodian)**  
  **Rules engine for cloud security, cost optimization, and governance**, Apache-2.0 licensed with **5,000+ GitHub stars** . **Policy-as-code for AWS, Azure, and GCP** . **Real-time remediation and enforcement** . **Best for cloud governance automation** .

### Attack Path & Graph Analysis

- **[IAMSpy](https://github.com/WithSecureLabs/IAMSpy)**  
  **Continuous IAM monitoring and analysis platform**, Apache-2.0 licensed . **Collects IAM configuration using AWS APIs** — users, groups, roles, policies, S3 bucket policies, KMS key policies . **Generates visualizations** (HTML) of collected data . **Detects privilege escalation issues** with GraphML output for yEd and Neo4j . **Maintains state between runs** — notifies about new issues, deleted issues, and unchanged issues . **Best for continuous IAM monitoring** .

- **[Cartography](https://github.com/cartography-cncf/cartography)**  
  **Graph-based cloud infrastructure security analysis**, Apache-2.0 licensed with **3,000+ GitHub stars** . **Consolidates infrastructure assets and relationships into a Neo4j graph** . **Query-based security analysis** — identify relationships and attack paths . **Supports AWS, Azure, GCP, and more** . **Best for graph-based cloud security analysis** .

- **[Repokid](https://github.com/Netflix/repokid)**  
  **AWS least privilege tool from Netflix**, Apache-2.0 licensed . **Removes unused IAM permissions based on access advisor data** . **Scheduled execution for continuous least privilege enforcement** . **Best for automated least privilege enforcement** .

### Additional Strong Open-Source Options

- **Cloudsplaining** — The de facto open-source AWS IAM analyzer .
- **PMapper** — Privilege escalation path analysis .
- **aws-iam-analyzer** — Open-source Access Analyzer alternative .
- **Policy Sentry** — Least privilege policy generation .
- **Parliament** — IAM linting library .
- **Custodian** — Cloud governance rules engine .
- **Cartography** — Graph-based cloud security analysis .
- **Repokid** — Automated least privilege enforcement from Netflix .
- **Aardvark** — Netflix's multi-account AWS IAM-based privilege de-escalation .
- **CloudTracker** — CloudTrail log analysis for identifying unused IAM permissions .

**Frameworks for building custom IAM policy and access analysis solutions**: Combine **Cloudsplaining** for comprehensive AWS IAM policy analysis and risk prioritization . Use **PMapper** for privilege escalation path detection and graph visualization . Deploy **aws-iam-analyzer** for open-source Access Analyzer functionality in private accounts . Integrate **Policy Sentry** for least privilege policy generation from CloudTrail activity . Choose **Parliament** for IAM linting in CI/CD pipelines . Use **Custodian** for policy-as-code governance . Integrate **IAMSpy** for continuous IAM monitoring and attack path analysis . Choose **Repokid** for automated least privilege enforcement . Note that true enterprise CIEM with multi-cloud entitlement graphs, just-in-time access workflows, and vendor-supported SLAs (Ermetic, Wiz, Britive) remains primarily commercial territory; open-source stacks provide strong policy analysis, privilege escalation detection, and least privilege enforcement foundations that require integration for complete IAM access analysis.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- IAM analysis platforms handle sensitive access configuration data. Self-hosted solutions require proper security hardening, access controls, and compliance with data privacy regulations.
- **IAM analysis tools require read-only credentials** — never grant write access to analysis tools. Use dedicated service accounts with least-privilege policies for scanning .
- **Policy analysis is not a one-time activity** — permissions drift continuously. Cloudsplaining, IAMSpy, and Repokid support scheduled execution for continuous monitoring .
- **License considerations**: Cloudsplaining uses BSD-3-Clause , PMapper uses GPL-3.0 , aws-iam-analyzer uses Apache-2.0 , Policy Sentry uses BSD-3-Clause , Parliament uses BSD-3-Clause , and Custodian uses Apache-2.0 . Verify licensing against your use case before committing.
- The open-source ecosystem provides strong policy analysis, privilege escalation detection, and least privilege enforcement foundations, but **multi-cloud entitlement graphs, just-in-time access workflows, and vendor-supported SLAs** remain primarily commercial offerings.

---

**Made for security engineers, cloud architects, and organizations seeking IAM policy and access analysis sovereignty.**  
Let's make IAM policy and access analysis more open, transparent, and least-privilege oriented.
