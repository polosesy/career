# Yeongil Yu

**Senior Cloud Architect · SRE · DevOps Engineer**

📧 yeongil6012@gmail.com &nbsp;·&nbsp; 📱 +82-10-2669-6014 &nbsp;·&nbsp; 📍 Seoul, South Korea

LinkedIn: _[TBD]_ &nbsp;·&nbsp; GitHub: _[TBD]_

---

## Summary

8-year Cloud Infrastructure / DevOps / SRE engineer. Expanded across **QA → SCM, CI/CD → Cloud Architect → SRE/Observability**, leading AKS operations, Landing Zone design, **Brownfield observability (Prometheus / Grafana / Alloy + OTel) standardization**, Packer + Ansible OS golden image automation, and multi-tenant SaaS redesign on Azure. Holds **KCNA · CKS · CKAD · CKA + Azure Solutions Architect Expert**. Currently expanding into AI infrastructure and multi-cloud platform engineering.

---

## Core Skills / Tech Stack

| Domain | Stack |
|--------|-------|
| **Cloud** | Azure (Expert), NCP, AWS / GCP |
| **Containers** | Kubernetes (AKS, EKS, OpenShift), Docker, Helm |
| **IaC** | Terraform, Packer, Ansible (+ Molecule), ARM |
| **CI / CD** | Jenkins (shared library), GitLab CI, Azure DevOps, ArgoCD, GitHub Actions |
| **Observability** | Prometheus, Grafana, Grafana Alloy, OpenTelemetry, Loki, Tempo, Micrometer, JMX Exporter |
| **SRE Practices** | SLI / SLO, Error Budget Burn-Rate, RED + USE, Brownfield phased rollout, Runbook standardization, Incident postmortem, DR / BCP (Warm Standby, RTO / RPO, Region Failover) |
| **Languages** | PowerShell · Bash (hands-on automation) · Java / Spring (operated / instrumented) · TypeScript / Node.js · Python (AI-assisted development) |
| **AI Tooling** | Claude Code |

---

## Professional Experience

### 01. emro Co., Ltd. &nbsp;·&nbsp; _May 2025 – Present_

**Senior Cloud Architect, Cloud Architecture Part**

Built the Azure environment for the Caidentia SaaS platform and designed/implemented its architecture & governance per Best Practice (CAF / WAF). Subsequently drove architecture & operational maturity (multi-tenant redesign, observability standard, OS automation).

**Architecture / Governance (primary)**

- **Caidentia Azure SaaS platform build** — Best Practice (CAF / WAF) Landing Zone · Hub & Spoke topology, Management Group / subscription separation, per-environment boundaries (Prod / STG / Demo), Terraform-based IaC standardization.
- **Azure governance framework** — Azure Policy (deny / audit) · naming · tagging standards, RBAC delegation · least privilege · PIM (Just-in-Time) · Managed Identity, Defender for Cloud · NSG / firewall · Private Endpoint security baseline, cost governance (FinOps) · budget alerts.
- **Multi-tenant SaaS architecture redesign (To-Be design lead, team collaboration)** (3-Tier Shared → tenant isolation), Hub & Spoke + AFD + AGW domain routing, **shared service tier (common DB / Search / Storage / AI Gateway) standardization**.

**Architecture / Operational Maturity**

- **Caidentia AKS observability standard** — 5-tier dashboard structure, SLI/SLO + Error Budget Burn-Rate alerting, cardinality rules.
- **Spring Boot + Legacy Spring MVC/Tomcat unified instrumentation track** — converging Micrometer + OpenTelemetry + PrometheusMeterRegistry + JMX Exporter sidecar into a single **Grafana Alloy DaemonSet** emitting to Azure Managed Prometheus / Loki / Tempo. (Terraform Brownfield import, **11 runbooks** included)
- **Caidentia OS golden image automation** (Packer + Ansible + Jenkins, CAI-SO-01 control) — SSI (AC01–AC06) ↔ Ansible role audit mapping, Molecule unit tests, **GitLab CI (lint) + Jenkins (build/publish/approve) split**, async KR→US replication, nightly drift check.

---

### 02. Cloocus Inc. &nbsp;·&nbsp; _May 2022 – Apr 2025_

**Manager / Managed Services Center**

- **Korea Marine Transport Co. (KMTC)** — Operated Azure infrastructure and AKS clusters / Azure DevOps CI/CD pipelines. Executed a **zero-downtime AKS 1.20 → 1.28.9 Blue/Green upgrade**, and migrated an open-source CI/CD stack (Jenkins + ArgoCD) onto Azure DevOps, consolidating the management surface.
- **Krafton** — AKS-based RedisJson PoC. Validated technology/performance/limits/cost against PaaS Redis, deploying **1,000 RedisJson instance Pods** (Terraform + Helm).
- **Handok** — Legacy SAP Azure migration + Azure Landing Zone (Hub & Spoke). Helm / AKS / GitHub Actions.
- **Sungju DND (Singapore region)** — Azure Landing Zone for a global CRM SaaS deployment. Hub & Spoke, Azure Firewall + Private Endpoint security baseline, ELK unified logging.

---

### 03. Gunwoo Solutions &nbsp;·&nbsp; _Oct 2018 – Feb 2020_

**Associate Research Engineer / Infrastructure Team**

- **Hyundai 5th-generation Wide AVN project** — Maintained SW configuration management and build automation scripts for AVN units across **31 Hyundai / Kia vehicle models**.
- **Vlink-system project** — Consolidated per-OEM CI/CD environments. Developed a scenario/action-tailored build system + CLI-based build automation interface (Jenkins + Gerrit + Docker + Node.js).

---

### 04. Qspot &nbsp;·&nbsp; _Jul 2015 – Jul 2018_

**Associate Research Engineer / QA Team**

Automotive telematics SW verification.

- **Hyundai Genesis Telematics** (6th-gen premium)
- **Volkswagen OCU Telematics** (Golf)
- **GM Cadillac CTS Telematics** — including overseas field verification. Authored and executed SW test plans via design-based techniques, continuously improving the release process.

---

## Selected Projects

### Caidentia AKS Observability Standard & Phased Rollout
_emro · May 2025 – Present (in progress)_

📝 **Background** : Re-framed past TPS-drop incidents (HikariCP exhaustion / Logback synchronous I/O / SSE leak / Tomcat thread saturation) into an integrated observability system enabling "RCA within 2 minutes from dashboards alone"
🎯 **Challenge** : Single Whatap dependency + metric fragmentation → adopt an Azure managed-service (AMW/AMG) standard, zero operational downtime
🤹 **Role** : Self-initiated proposal and sole builder of the observability standard (Brownfield, rollout in progress)
✅ **Outcomes** :
- Master Plan (Four Golden Signals / RED+USE / SLI-SLO / Error Budget Burn-Rate / cardinality rules) standardized into a single document
- Phase 0 Terraform Brownfield import (AMG + Monitor Workspace + AAD/RBAC + Alloy DaemonSet)
- Phase 1 simultaneous instrumentation standard for Spring Boot + Legacy Spring MVC
- Phase 2 5-tier dashboards as JSON-as-Code → **dashboard applied to a new service within 30 minutes**
- Phase 3 Symptom-vs-Cause alerts + Notification Policy + 11 runbooks
- Phase 4 Loki + Tempo on AKS + Azure Blob design + OTel Java Agent + Tail Sampling
- **11 cumulative pitfall retrospectives** documented from operations

🔨 **Tech** : Azure AKS, Azure Managed Prometheus / Grafana, Grafana Alloy, Loki, Tempo, OpenTelemetry, Micrometer, JMX Exporter, Terraform, Spring 6, Slack + Azure Logic App

---

### Caidentia Ubuntu OS Golden Image Automation
_emro · 2025 – Present (in progress)_

📝 **Background** : OS golden image builds ran as manual procedures, risking skipped steps / review delays / weak audit trails
🎯 **Challenge** : Satisfy the CAI-SO-01 control + codify the build + retain the Cloud Security Part's manual approval gate (immutable image policy)
🤹 **Role** : Automation design and implementation (sole)
✅ **Outcomes** :
- 100% audit traceability between SSI checklist (AC01–AC06) ↔ Ansible tasks
- Introduced Molecule-based role unit testing
- **GitLab CI (lint + Molecule) + Jenkins (Packer build / Compute Gallery publish / security approval / smoke-test)** split
- KR (koreacentral) → US (eastus) async snapshot replication + automatic multi-region Image Version creation
- Nightly drift-check Jenkinsfile (Continuous Evaluation)
- Azure Control VM setup guide for WSL-unavailable environments + INCIDENTS / IMAGE-CAPTURE / SSI-mapping / Versioning docs

🔨 **Tech** : Packer, Ansible (+ Molecule), Jenkins (shared library), GitLab CI, Azure Compute Gallery, Azure Managed Identity, Ubuntu, SSI

---

### Caidentia Multi-tenant SaaS + AI Platform Architecture Redesign
_emro · 2025 – Present (in progress)_

📝 **Background** : 3-Tier Shared structure (shared DB/Search/Storage, mixed Demo/POC/Prod, 2 idle GPU RIs, no CI/CD)
🎯 **Challenge** : Meet SOC 2 Type II / ISO 27001 certification criteria + preserve sunk cost (GPU RI) + tenant isolation
🤹 **Role** : Architecture design and decision documentation (team collaboration)

🏗️ **Service architecture design** :
- **Network topology** — Hub & Spoke with per-environment Spokes (Prod / STG / Demo) separated, shared security/gateway consolidated in the Hub. External ingress via AFD → AGW two-tier, internal traffic closed via Private Endpoint + Private DNS.
- **Traffic / tenant routing** — AGW Host/Path routing for per-tenant domain branching (`shared.kdnc.com` pattern), tenant identification → backend pool mapping.
- **Workload tier** — AKS (application) + VMSS (GPU/model serving) hybrid, Managed Identity + RBAC least privilege, Flyway schema versioning.

🧩 **Shared service architecture** :
- Separated common tenant features into a **Shared Tier** — common RDB (schema/row-level isolation), common Search, common Object Storage, common AI Gateway standardized into a single tier.
- Defined per-tenant **data isolation boundaries** (logical isolation via tenant key on shared resources → staged migration path to physical isolation).
- Placed shared resources in the Hub/common Spoke, each environment Spoke accessing via Private Endpoint; reviewed single point of failure (SPOF) and cardinality impact of common components.

✅ **Outcomes** :
- 12 gaps identified and priority-mapped
- To-Be architecture documented on Hub & Spoke + Shared Tier separation
- AGW Host/Path multi-tenant domain routing design (`shared.kdnc.com` pattern)
- **Absorbed 2 GPU RIs** via common AI API Gateway + self-hosted model serving (avoiding sunk cost)
- Compliance Architecture Plan (SOC 2 / ISO 27001) mapping
- Azure OpenAI Architecture Report (Private Endpoint + internal firewall + token pool / cache design)

🔨 **Tech** : Azure AGW, AFD, AKS / VMSS, Private Endpoint, MI, Azure OpenAI, RBAC, Flyway, Jenkins, Hub & Spoke

---

### Caidentia DR (Disaster Recovery) Zone Design & Warm Standby
_emro · 2025 – Present (in progress)_

📝 **Background** : No DR Zone for region-level outage in the Caidentia operational environment → a recovery scheme for core resources (DB / Storage) was needed
🎯 **Challenge** : Meet **RTO 15 min / RPO 1 hr** + minimize DR always-on cost (Warm Standby) + work around Azure managed Failover's "not user-testable" limitation
🤹 **Role** : DR architecture design · Terraform codification · DR drill procedure (sole, guide standardization)
✅ **Outcomes** :
- **Cost-tiered Warm Standby design** — always-on (near-zero cost: VNet / Subnet / NAT Gateway) vs disaster-time Terraform manual provisioning (AGW / LB / Redis / VM)
- **PostgreSQL Flexible read replica + Virtual Endpoint** — pair-region-independent replication, failover-transparent endpoints (Primary auto-relay) (RTO 7 s / RPO 20 min)
- **RA-GRS (read-access geo-redundant) Blob Storage** — pair-region auto replication, Primary Endpoint auto-relay on failover (RTO 15 min / RPO 20 min)
- **DR drill procedure standardization** — worked around managed Failover (Key Vault, etc.) non-testability via "assume failover occurred + pre-provision in pair region," with a guide for adding a Storage read replica when the training Primary is Staging
- **Caidentia DR Terraform code** — codified disaster-time resources (AGW / LB / Redis / VM) for reproducible recovery

🔨 **Tech** : Azure (East US ↔ West US Region Pair, Failover), PostgreSQL Flexible Server (Virtual Endpoint, Read Replica), RA-GRS Blob Storage, Azure Key Vault, Application Gateway, Load Balancer, Redis, Terraform

---

### KMTC AKS Cluster Zero-Downtime Upgrade & CI/CD Consolidation
_Cloocus · Jun 2024 – Aug 2024_

📝 **Background** : AKS cluster EOL → zero-downtime version upgrade and redeploy needed (1.20 → 1.28.9)
🤹 **Role** : PM, implementation
✅ **Outcomes** :
- New AKS cluster Blue/Green deployment (downtime 0)
- Open-source CI/CD (Jenkins + ArgoCD) → Azure DevOps migration
- Management surface consolidated on the Azure platform

🔨 **Tech** : Azure, Kubernetes, Azure DevOps CI/CD, Jenkins, ArgoCD, Maven, Spring Boot, Docker

---

### Krafton AKS for RedisJson PoC
_Cloocus · Jun 2022 – Jul 2022_

📝 **Background** : Compare AKS-based RedisJson against PaaS Redis (technology/performance/limits/cost)
🤹 **Role** : Team member, implementation
✅ **Outcomes** : **Deployed 1,000 RedisJson instance Pods**, validated horizontal scaling for future game-server workloads
🔨 **Tech** : Azure cloud, AKS, Helm, PowerShell, GitHub Actions, Terraform

---

### Handok / Sungju DND Azure Landing Zone
_Cloocus · Jan 2023 – Oct 2023_

- **Handok** : Legacy SAP migration + Landing Zone (Hub & Spoke) for next-generation projects
- **Sungju DND** : Landing Zone for a global CRM SaaS deployment in the Singapore region (Hub & Spoke + Azure Firewall + Private Endpoint + ELK)

🔨 **Tech** : Azure (AGW, AKS, Hub & Spoke, Firewall, Private Endpoint), Helm, ELK, PowerShell, GitHub Actions

---

### OpenShift Container Platform (PaaS) on Air-Gapped Infrastructure
_KRRA / Cloud Service Development Specialist Track · Jul 2021 – Oct 2021_

📝 **Background** : Build an OpenShift Container Platform PaaS in an air-gapped (physical server) environment
✅ **Takeaway** : **A directly reusable asset for on-prem AI workload deployment patterns**

🔨 **Tech** : Git, CentOS, CoreOS, OpenShift, ESXi Host, Prometheus, Grafana, HAProxy

---

### VMware Private Cloud (mini-project)
_KRRA / Cloud Service Development Specialist Track · Apr 2021 – Jun 2021_

Built a VMware vSphere private cloud against a virtual customer scenario — vCenter, 3 ESXi hosts, 4 virtual servers, vMotion / DRS / HA / P2V migration.

---

### Vlink-system (Multi-OEM CI/CD Integration)
_Gunwoo Solutions · Jul 2019 – Jan 2020_

Consolidated per-OEM CI/CD environments into a single system. Scenario/action-level build granularity + CLI-based build automation interface.

🔨 **Tech** : Git, Gerrit, Jenkins, Jira, Collab, Docker, Node.js

---

## Certifications

| Certification | Issued | Issuer |
|---------------|--------|--------|
| Kubernetes and Cloud Native Associate (**KCNA**) | Jan 2026 | The Linux Foundation |
| Certified Kubernetes Security Specialist (**CKS**) | Mar 2024 | The Linux Foundation |
| Certified Kubernetes Application Developer (**CKAD**) | Feb 2024 | The Linux Foundation |
| Certified Kubernetes Administrator (**CKA**) | Sep 2022 | The Linux Foundation _(renewal status — verify)_ |
| Microsoft Certified: **Azure Solutions Architect Expert** (AZ-305) | Aug 2022 | Microsoft |
| Microsoft Certified: Azure Administrator Associate (AZ-104) | Aug 2022 | Microsoft |
| NAVER Cloud Platform Certified Associate | Oct 2020 | NAVER Cloud |
| ISTQB Certified Tester — Foundation Level (CTFL) | Nov 2016 | ISTQB |

---

## Education

**Joongbu University** &nbsp;·&nbsp; _Mar 2008 – Feb 2015_
B.S. in Game Science

**Korea Radio Promotion Association (KRRA)** — private training
- Kubernetes-based MSA Development Track &nbsp;·&nbsp; _Nov 2021 – Dec 2021_
- Cloud Service Development Specialist Track &nbsp;·&nbsp; _Apr 2021 – Oct 2021_

---

## Languages

| Language | Proficiency |
|----------|-------------|
| Korean | Native |
| English | Reading / Writing workable (AI-assisted), Speaking basic |

---

## About

I am an 8-year engineer who has expanded from **SW verification (QA) → CI/CD automation → Cloud Infrastructure → SRE/Observability**. From automotive telematics SW verification (GM/VW/Hyundai) → multi-OEM CI/CD integration on Jenkins/Gerrit/Docker → Azure AKS operations / Landing Zone design → currently establishing the observability standard in a Brownfield environment.

At **emro's Cloud Architecture Part**, I am establishing the SRE standard for the Caidentia operational environment from the ground up. Key deliverables include (1) an integrated observability standard for Spring Boot + Legacy Spring MVC on Azure AKS (Master Plan + Phase 0–4) and 11 runbooks, (2) Packer + Ansible + Jenkins Ubuntu OS golden image automation (CAI-SO-01 control, SSI AC01–AC06 auto-mapping, nightly drift check), (3) a 3-Tier Shared → multi-tenant SaaS redesign (SOC 2 / ISO 27001, shared service tier standardization, AGW domain routing, GPU RI absorption design), and (4) a Caidentia DR Zone design (Warm Standby, PostgreSQL Virtual Endpoint + RA-GRS, RTO 15 min / RPO 1 hr, Terraform codification).

In earlier roles at **Cloocus (May 2022 – Apr 2025)**, I handled the KMTC AKS zero-downtime version upgrade (1.20→1.28.9 Blue/Green), the Handok · Sungju DND Azure Landing Zone builds, and the Krafton AKS-based RedisJson 1000-Pod PoC.

My operating philosophy is **"phase exit criteria + cumulative pitfall retrospectives."** I believe that breaking every change into small units and always feeding pitfalls learned from failures into the next phase is what determines resilience in a Brownfield environment. **My future direction is AI infrastructure and multi-cloud (AWS/GCP) platform engineering — contributing deeply to observability, automation, and multi-deployment models (cloud / private cloud / on-prem) for large-scale AI workloads.**
