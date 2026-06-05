# Yeongil Yu

**Senior Cloud Architect | SRE | DevOps Engineer**

📧 yeongil6012@gmail.com &nbsp;·&nbsp; 📱 +82-10-2669-6014 &nbsp;·&nbsp; 📍 Seoul, South Korea

LinkedIn: _[TBD — update English profile]_ &nbsp;·&nbsp; GitHub: _[TBD]_

---

## Summary

Cloud Infrastructure, DevOps, and SRE engineer with 8+ years spanning automotive software QA, multi-OEM CI/CD platforms, Azure AKS operations, Landing Zone architecture, and Brownfield observability standardization. Currently establishing the SRE and observability standard for the Caidentia SaaS platform at emro. Triple-certified Kubernetes practitioner (CKS / CKAD / CKA) and Microsoft Azure Solutions Architect Expert. Actively expanding into AI infrastructure, MLOps, and multi-cloud platform engineering.

---

## Core Skills

| Domain | Stack |
|--------|-------|
| **Cloud** | Azure (Expert) — AKS, AGW, AFD, AMW, AMG, Compute Gallery, Managed Identity, Private Endpoint, OpenAI · AWS / GCP (learning) |
| **Containers** | Kubernetes (AKS, EKS, OpenShift), Docker, Helm |
| **IaC** | Terraform, Packer, Ansible (+ Molecule), ARM / Bicep |
| **CI / CD** | Jenkins (shared library), GitLab CI, Azure DevOps, ArgoCD, GitHub Actions |
| **Observability** | Prometheus, Grafana, Grafana Alloy, OpenTelemetry, Loki, Tempo, Micrometer, JMX Exporter, ELK |
| **SRE Practices** | SLI / SLO, Error Budget Burn-Rate alerting, RED + USE, Brownfield phased rollout, Runbook standardization, Incident postmortem |
| **Languages** | Java / Spring (operated workload), PowerShell, Bash, TypeScript / Node.js, Python (learning) |
| **AI Tooling** | Claude Code (used for in-house productivity PoC delivery) |

---

## Professional Experience

### emro Co., Ltd. &nbsp;·&nbsp; _May 2025 – Present_

**Senior Cloud Architect, Cloud Architecture Part**

Establishing the SRE and observability standard for the Caidentia SaaS platform on Azure AKS. Single contributor or technical lead on every initiative below.

- Authored the **Caidentia AKS Observability Master Plan** (5-tier dashboard hierarchy, SLI / SLO / Error Budget Burn-Rate alerting, RED + USE, cardinality rules) and drove its **Phase 0–4 rollout end-to-end in a Brownfield environment with zero operational downtime**.
- Designed dual instrumentation tracks for **Spring Boot** (Micrometer + OpenTelemetry) and **Legacy Spring MVC on Tomcat** (PrometheusMeterRegistry + JMX Exporter sidecar), unifying both behind a single **Grafana Alloy DaemonSet** emitting to Azure Managed Prometheus, Loki, and Tempo.
- Codified the observability infrastructure with **Terraform** (Brownfield import of Azure Managed Grafana + Monitor Workspace, AAD / RBAC, Alloy, kube-state-metrics, node-exporter); standardized **11 runbooks** tied to all critical alerts (HikariCPPending, TomcatThreadSaturation, LogbackErrorStorm, SSEEmitterLeak, SLOBurnRateFast, etc.).
- Built the **Caidentia OS golden image automation** (Packer + Ansible + Jenkins) implementing the CAI-SO-01 security control. Mapped the Samsung Security Index (AC01–AC06) to Ansible roles with full audit traceability, added Molecule unit tests, and split GitLab CI (lint + Molecule) from Jenkins (Packer build, Compute Gallery publish, security approval gate, smoke test). Designed asynchronous **KR → US snapshot replication** for multi-region image versioning and a nightly drift-check job for continuous evaluation.
- Redesigned the **Caidentia multi-tenant SaaS architecture** (3-tier shared → tenant-isolated) targeting **SOC 2 Type II, ISO 27001, and Korean privacy law** compliance. Designed Hub & Spoke environment separation, AGW host/path-based tenant routing, an AI shared API gateway absorbing the pre-committed GPU RI (×2, 3-year) into self-hosted model serving, and RBAC + Managed Identity authentication.
- Delivered the **Azure Unified Dashboard** — an internal Azure operations platform PoC built with Claude Code as a pair-programming assistant. **19 commits / ~19,800 LoC** TypeScript full-stack monorepo (118 source files, 21 API endpoints, 8 frontend pages) integrating Azure Resource Graph, Monitor, Cost Management, Traffic Analytics, NSG Flow Log, and App Insights with ReactFlow 2D + Three.js 3D topology views and OBO authentication. Registered as an official internal **"AI Productivity Use Case"** report.
- Authored **8+ AI infrastructure operations guides** for Azure OpenAI / Self-hosted LLM workloads — SSE streaming timeouts across AGW, AFD ↔ AGW X-Forwarded header redirect loops, Azure Files SMB `mfsymlinks` mounting, NSG Deny-All impact analysis, and more. Converted recurring incidents into reusable institutional knowledge.

---

### Cloocus Inc. &nbsp;·&nbsp; _May 2022 – Apr 2025_

**Manager, Managed Services Center**

Customer-facing Azure platform engineer delivering cloud-native solutions across enterprise customers in Korea.

- **Korea Marine Transport Co. (KMTC)** — Operated Azure infrastructure and AKS clusters; owned DevOps CI/CD pipelines on Azure DevOps. Executed a **zero-downtime AKS cluster version upgrade (1.20 → 1.28.9)** via Blue/Green rollout and migrated an open-source CI/CD stack (Jenkins + ArgoCD) onto Azure DevOps, consolidating the management surface on the Azure platform.
- **Krafton** — Designed and validated an AKS-based RedisJson PoC against PaaS Redis (cost / performance / technical limits). Provisioned **1,000 RedisJson instance Pods** using Terraform + Helm to verify horizontal capacity for an upcoming game-server workload.
- **Handok** — Migrated legacy SAP to Azure and built an Azure Landing Zone (Hub & Spoke) preparing the customer for next-generation initiatives. Delivered with Helm, AKS, and GitHub Actions–based deployment.
- **Sungju DND** (Singapore region) — Built a global Azure Landing Zone in `southeastasia` for a CRM SaaS deployment with Hub & Spoke topology, Azure Firewall + Private Endpoint security baseline, and ELK-based unified logging.

---

### Gunwoo Solutions &nbsp;·&nbsp; _Oct 2018 – Feb 2020_

**Associate Research Engineer, Infrastructure Team**

- **Hyundai 5th-generation Wide AVN** — Owned software configuration management and build automation for AVN units across **31 Hyundai / Kia vehicle models**.
- **Vlink-system** — Built a unified CI/CD platform that consolidated per-OEM build environments into a single scenario- and action-driven CLI interface using Jenkins + Gerrit + Docker + Node.js.

---

### Qspot &nbsp;·&nbsp; _Jul 2015 – Jul 2018_

**Associate Research Engineer, QA Team**

Automotive telematics SW verification for global OEMs.

- **Hyundai Genesis Telematics** (6th-gen premium)
- **Volkswagen OCU Telematics** (Golf)
- **GM Cadillac CTS Telematics** — including overseas field verification. Authored test plans via design-based techniques and continuously improved the release process.

---

## Additional Projects

### OpenShift Container Platform on Air-Gapped Infrastructure
_KRRA Cloud Service Specialist Track &nbsp;·&nbsp; Jul 2021 – Oct 2021_

Built an OpenShift Container Platform PaaS on physical servers in a closed-network (air-gapped) environment. Integrated Prometheus, Grafana, HAProxy for observability and ingress on CentOS / CoreOS. **Directly relevant to on-prem AI workload deployment patterns.**

### VMware Private Cloud (mini-project)
_KRRA Cloud Service Specialist Track &nbsp;·&nbsp; Apr 2021 – Jun 2021_

Built a VMware vSphere private cloud against a customer scenario — vCenter, three ESXi hosts running four virtualized servers with vMotion, DRS, HA, and P2V migration.

---

## Certifications

| Certification | Issued | Issuer |
|---------------|--------|--------|
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
B.S. in Media Software

**Korea Radio Promotion Association (KRRA)**
- Kubernetes-based MSA Development Track &nbsp;·&nbsp; _Nov 2021 – Dec 2021_
- Cloud Service Development Specialist Track &nbsp;·&nbsp; _Apr 2021 – Oct 2021_

---

## Languages

| Language | Proficiency |
|----------|-------------|
| Korean | Native |
| English | Business — Reading / Writing proficient, Speaking conversational |
