# Assignment 2 – Cloud Service Alternatives Report

## 1. Identify Azure Services Used in the Course

- Azure DevOps
- Azure Blob Storage
- Azure Key Vault
- Azure Active Directory (SSO, IAM)
- Azure Monitor & Log Analytics
- Azure Policy
- Defender for Cloud
- Azure Sentinel (SIEM/SOAR)

## 2. Find the AWS & GCP Equivalents

  | Azure Service | AWS Equivalent(s) | GCP Equivalent(s) |
|---|---|---|
| **Azure DevOps** | AWS CodeCommit, CodeBuild, CodeDeploy, CodePipeline | Cloud Build, Cloud Source Repositories, Cloud Deploy |
| **Azure Blob Storage** | Amazon Simple Storage Service (S3) | Google Cloud Storage |
| **Azure Key Vault** | AWS Secrets Manager, AWS KMS (Key Management Service) | Secret Manager, Cloud KMS |
| **Azure Active Directory (SSO, IAM)** | AWS IAM, AWS IAM Identity Center (SSO) | Google Cloud IAM, Identity Platform |
| **Azure Monitor & Log Analytics** | Amazon CloudWatch, AWS X-Ray | Google Cloud Operations Suite (Stackdriver) |
| **Azure Policy** | AWS Config, AWS Organizations Service Control Policies (SCPs) | Organization Policy Service, Config Validator |
| **Defender for Cloud** | AWS Security Hub, Amazon GuardDuty, Amazon Inspector | Security Command Center, Event Threat Detection |
| **Azure Sentinel (SIEM/SOAR)** | AWS Security Hub + Amazon Detective + Amazon Security Lake | Chronicle Security Operations, Security Command Center |

## 3. Compare the Services

 ### 1. Azure DevOps 
   
  - **AWS Equivalent**: AWS CodeCommit, CodeBuild, CodeDeploy, CodePipeline

  - **GCP Equivalent**: Google Cloud Build, Cloud Source Repositories, and Cloud Deploy

**Overview**
  - Azure DevOps is an integrated suite offering source control, build pipelines (CI/CD), artifact management, and project tracking.

**Core Features**
 - Azure Repos (Git, TFVC)

 - Azure Pipelines (CI/CD)

 - Azure Artifacts (package feeds)

 - Azure Boards (work item tracking)

**Security & Compliance**
 - SOC 2, ISO 27001, GDPR compliance (Azure DevOps Services)

 - AWS Code services similarly fall under AWS shared compliance framework

 - GCP services inherit Google Cloud compliance certifications

**Pricing Model**
 - Azure: free tier (5 free users + limited parallel pipelines), then per-user and parallel jobs

 - AWS: CodeCommit incurs per-active user storage fees; CodePipeline / Build priced per execution-minute

 - GCP: Cloud Build pricing per build-minute; repositories have per-GB storage costs

**DevSecOps Integration**
 - Supports YAML pipelines, CLI (az devops), REST API, Terraform (azurerm_devops)

 - AWS: Terraform providers aws_codepipeline, aws_codebuild, etc. + AWS CLI/SDKs

 - GCP: gcloud CLI, Terraform providers (google_cloudbuild_trigger, etc.)

---

 ### 2.Azure Blob Storage
 
 - **AWS Equivalent** :- Amazon Simple Storage Service (S3)

 - **GCP Equivalent** :- Google Cloud Storage


  **Overview**
- Azure Blob Storage is Microsoft’s object storage solution for storing massive amounts of unstructured data such as documents, images, videos, and backups.

**Core Features**
- Tiered storage (Hot, Cool, Archive)
- REST-based API access
- Lifecycle management policies
- Data replication options (LRS, ZRS, GRS, RA-GRS)
- Integration with CDN for faster delivery

 **Security & Compliance**
- Data encryption at rest and in transit (AES-256, TLS 1.2+)
- Private endpoints and VNet integration
- Supports Azure RBAC and shared access signatures (SAS)
- Complies with SOC 2, ISO 27001, HIPAA, GDPR
- AWS S3 and GCP Storage have similar encryption and compliance certifications

**Pricing Model**
- **Azure**: Charged by storage tier (per GB/month), data retrieval, and API operations
- **AWS**: S3 pricing by storage class, retrieval, and request count
- **GCP**: Storage pricing per class, operations, and network egress

**DevSecOps Integration**
- **Azure**: Terraform provider (`azurerm_storage_account`, `azurerm_storage_blob`)
- **AWS**: Terraform (`aws_s3_bucket`), AWS CLI, SDKs
- **GCP**: Terraform (`google_storage_bucket`), `gsutil`, `gcloud` CLI

---

### 3.Azure Key Vault

 - **AWS Equivalent** :- AWS Secrets Manager, AWS Key Management Service (KMS)
 - **GCP Equivalent** :- Secret Manager, Cloud KMS

**Overview** 
 - Azure Key Vault securely stores and manages sensitive information such as API keys, passwords, certificates, and encryption keys.

**Core Features**
- Secure secret storage
- Key generation and lifecycle management
- Certificate management
- HSM (Hardware Security Module) support
- Access control with Azure AD


**Security & Compliance**
- FIPS 140-2 Level 2 HSM compliance
- Role-based access via Azure AD
- Audit logging via Azure Monitor
- AWS and GCP equivalents meet similar compliance standards (FIPS, SOC 2, ISO 27001)


**Pricing Model**
- **Azure**: Standard and premium tiers; billed per operation and per key/secret version
- **AWS**: Secrets Manager per secret/month + API calls; KMS per key/month + requests
- **GCP**: Secret Manager per secret/month; KMS per key version/month + requests

**DevSecOps Integration**
- **Azure**: Azure CLI, REST API, Terraform (`azurerm_key_vault`)
- **AWS**: Terraform (`aws_secretsmanager_secret`, `aws_kms_key`), AWS CLI
- **GCP**: Terraform (`google_secret_manager_secret`, `google_kms_key_ring`), `gcloud` CLI

---

### 4.Azure Active Directory (SSO, IAM)

- **AWS Equivalent** :- AWS Identity and Access Management (IAM), AWS IAM Identity Center (SSO)
  
- **GCP Equivalent** :- Google Cloud IAM, Identity Platform

**Overview**
- Azure AD is a cloud-based identity and access management service providing SSO, MFA, and identity governance for cloud and on-prem apps.

**Core Features**
- Single Sign-On (SAML, OIDC)
- Conditional Access policies
- MFA integration
- Role-based access control
- B2B and B2C identity services


**Security & Compliance**
- SOC 2, ISO 27001, FedRAMP, HIPAA, GDPR compliance
- AWS and GCP IAM services follow similar compliance frameworks
- Built-in monitoring for suspicious sign-ins


**Pricing Model**
- **Azure**: Free tier + Premium P1/P2 licenses for advanced features
- **AWS**: IAM is free; SSO charged per-user if using AWS IAM Identity Center with directory integration
- **GCP**: IAM free; Identity Platform billed per MAU

**DevSecOps Integration**
- **Azure**: Azure AD Graph API, Microsoft Graph API, Terraform (`azuread_user`, `azuread_application`)
- **AWS**: Terraform (`aws_iam_user`, `aws_iam_policy`), AWS CLI
- **GCP**: Terraform (`google_project_iam_*`), `gcloud` CLI

---

### 5.Azure Monitor & Log Analytics

 - **AWS Equivalent**:- Amazon CloudWatch, AWS X-Ray

 - **GCP Equivalent** :- Google Cloud Operations Suite** (formerly Stackdriver)

**Overview**
 - Azure Monitor collects, analyzes, and acts on telemetry from applications and infrastructure; Log Analytics provides query capabilities over collected logs.

**Core Features**
- Metrics and log collection
- Log Analytics with KQL (Kusto Query Language)
- Alerts and automated actions
- Application Insights for APM
- Integration with Azure Sentinel

**Security & Compliance**
- Data encryption in transit and at rest
- SOC 2, ISO 27001, HIPAA, GDPR compliance
- AWS and GCP equivalents maintain similar compliance
- Private link support for ingestion endpoints

**Pricing Model**
- **Azure**: Per GB ingested + retention beyond free 31 days
- **AWS**: CloudWatch per metric, log ingestion per GB, custom dashboards per month
- **GCP**: Logging per GB ingested, monitoring API calls free up to quota

**DevSecOps Integration**
- **Azure**: Azure CLI, REST API, Terraform (`azurerm_monitor_metric_alert`)
- **AWS**: Terraform (`aws_cloudwatch_metric_alarm`), AWS CLI
- **GCP**: Terraform (`google_logging_metric`, `google_monitoring_alert_policy`), `gcloud` CLI

---

### 6.Azure Policy

- **AWS Equivalent** :- AWS Config, AWS Organizations Service Control Policies (SCPs)
- **GCP Equivalent** :- Organization Policy Service, Config Validator

**Overview**
- Azure Policy enforces governance rules and evaluates compliance at scale across Azure resources.

**Core Features**
- Policy definition and assignment
- Compliance scanning and remediation
- Initiative groups for related policies
- Integration with ARM templates and Bicep

**Security & Compliance**
- Ensures adherence to compliance frameworks by enforcing resource configurations
- AWS Config and GCP Organization Policy provide similar governance enforcement
- Integration with audit logging for tracking

**Pricing Model**
- **Azure**: Policy evaluation free; remediation tasks may incur compute/storage charges
- **AWS**: Config priced per resource configuration item; SCP free within AWS Organizations
- **GCP**: Organization Policy free; Config Validator usage tied to Deployment Manager or Terraform

**DevSecOps Integration**
- **Azure**: Terraform (`azurerm_policy_definition`, `azurerm_policy_assignment`)
- **AWS**: Terraform (`aws_config_config_rule`), AWS CLI
- **GCP**: Terraform (`google_org_policy_policy`), `gcloud` CLI

---

### 7.Defender for Cloud

- **AWS Equivalent** :- AWS Security Hub, Amazon GuardDuty, Amazon Inspector

- **GCP Equivalent** :- ecurity Command Center, Event Threat Detection

**Overview**
- Defender for Cloud is a cloud security posture management (CSPM) and workload protection platform (CWPP) for hybrid and cloud-native workloads.

**Core Features**
- Continuous security assessment
- Threat detection and alerts
- Regulatory compliance dashboard
- Vulnerability management for VMs and containers
- Integration with Azure Policy and Sentinel

**Security & Compliance**
- Supports CIS, NIST, ISO 27001 compliance checks
- AWS and GCP equivalents offer similar CSPM and threat detection
- Data encrypted in transit and at rest

**Pricing Model**
- **Azure**: Free tier (security posture); Defender plans billed per resource type/month
- **AWS**: Security Hub per account/month; GuardDuty per GB log analyzed; Inspector per instance/container scan
- **GCP**: SCC pricing per tier; Event Threat Detection billed per analyzed log volume

**DevSecOps Integration**
- **Azure**: Terraform (`azurerm_security_center_contact`)
- **AWS**: Terraform (`aws_securityhub_account`), AWS CLI
- **GCP**: Terraform (`google_security_center_notification_config`), `gcloud` CLI

---

###  8.Azure Sentinel (SIEM/SOAR)

- **AWS Equivalent** :- AWS Security Hub, Amazon Detective, Amazon Security Lake

- **GCP Equivalent** :- Chronicle Security Operations, Security Command Center

**Overview**
- Azure Sentinel is a cloud-native SIEM and SOAR platform that collects security data, detects threats, and automates incident response.

**Core Features**
- Log ingestion from multiple sources
- KQL-based analytics
- AI-driven threat detection
- Automated response playbooks via Logic Apps
- Integration with Microsoft security ecosystem

**Security & Compliance**
- ISO 27001, SOC 2, FedRAMP compliance
- AWS and GCP SIEM solutions offer similar compliance coverage
- Data encrypted at rest/in transit; role-based access

**Pricing Model**
- **Azure**: Per GB ingested or commitment tier pricing
- **AWS**: Detective per GB/month; Security Lake storage costs; Security Hub charges per resource
- **GCP**: Chronicle flat-rate pricing or per data volume

**DevSecOps Integration**
- **Azure**: Terraform (`azurerm_sentinel_alert_rule`), Azure REST API
- **AWS**: Terraform (`aws_securityhub_insight`), AWS CLI
- **GCP**: Terraform (`google_scc_notification_config`), `gcloud` CLI


