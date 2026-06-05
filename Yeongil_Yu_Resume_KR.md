# 유영일 (책임)

**Senior Cloud Architect · SRE · DevOps Engineer**

📧 yeongil6012@gmail.com &nbsp;·&nbsp; 📱 010-2669-6014 &nbsp;·&nbsp; 📍 Seoul, South Korea

LinkedIn: _[TBD]_ &nbsp;·&nbsp; GitHub: _[TBD]_

---

## 한줄 소개

8년차 Cloud Infrastructure / DevOps / SRE 엔지니어. **QA → CI/CD → Cloud Architect → SRE/Observability** 로 영역을 확장하며 Azure 환경에서 AKS 운영, Landing Zone 설계, **Brownfield 옵저버빌리티(Prometheus / Grafana / Alloy + OTel) 표준 수립**, Packer + Ansible 기반 OS 골든이미지 자동화, 멀티테넌트 SaaS 재설계를 주도해왔습니다. **CKS · CKAD · CKA + Azure Solutions Architect Expert** 보유. 현재 AI 인프라와 멀티클라우드 플랫폼 엔지니어링으로 영역을 확장 중입니다.

---

## 핵심 역량 / 기술 스택

| 영역 | 스택 |
|------|------|
| **Cloud** | Azure (Expert) — AKS, AGW, AFD, AMW, AMG, Compute Gallery, Managed Identity, Private Endpoint, OpenAI · AWS / GCP (학습 중) |
| **Container** | Kubernetes (AKS, EKS, OpenShift), Docker, Helm |
| **IaC** | Terraform, Packer, Ansible (+ Molecule), ARM / Bicep |
| **CI / CD** | Jenkins (shared library), GitLab CI, Azure DevOps, ArgoCD, GitHub Actions |
| **Observability** | Prometheus, Grafana, Grafana Alloy, OpenTelemetry, Loki, Tempo, Micrometer, JMX Exporter, ELK |
| **SRE 실무** | SLI / SLO, Error Budget Burn-Rate, RED + USE, Brownfield Phase 운영, Runbook 표준화, Incident Postmortem |
| **언어** | Java / Spring (운영 대상), PowerShell, Bash, TypeScript / Node.js, Python (학습 중) |
| **AI 도구** | Claude Code (사내 생산성 PoC 활용) |

---

## 경력

### 01. 주식회사 엠로 (emro) &nbsp;·&nbsp; _2025. 05. ~ 재직중_

**책임 / 클라우드아키텍처파트**

Caidentia SaaS 플랫폼의 SRE 및 옵저버빌리티 표준을 처음부터 정립. 모든 항목 **단독 수행 또는 기술 리드**.

- **Caidentia AKS 옵저버빌리티 표준 수립** (Master Plan + Phase 0~4) — 5-Tier 대시보드 구조, SLI/SLO + Error Budget Burn-Rate 알림 체계, 카디널리티 룰 정립. **Brownfield 환경에서 무중단으로 단계별 적용**.
- **Spring Boot + Legacy Spring MVC/Tomcat 통합 계측 트랙** 설계 — Micrometer + OpenTelemetry + PrometheusMeterRegistry + JMX Exporter sidecar 를 **Grafana Alloy DaemonSet 한 곳으로 수렴**해 Azure Managed Prometheus / Loki / Tempo 로 전송.
- **Terraform 기반 옵저버빌리티 IaC** (Azure Managed Grafana + Monitor Workspace Brownfield import, AAD/RBAC, Alloy, kube-state-metrics, node-exporter) + **런북 11건** 정립.
- **Caidentia OS 골든이미지 자동화** (Packer + Ansible + Jenkins, CAI-SO-01 통제) — SSI(AC01~AC06) ↔ Ansible role 감사 매핑, Molecule 단위 테스트, **GitLab CI(lint) + Jenkins(빌드/게시/승인) 분담**, KR→US 비동기 복제, 야간 드리프트 점검.
- **멀티테넌트 SaaS 아키텍처 재설계** (3-Tier Shared → 테넌트 격리) — SOC 2 / ISO 27001 / 개인정보보호법 대응, Hub & Spoke + AGW 도메인 라우팅, **기존 GPU RI(2대/3년) 를 Self-hosted 모델 서빙으로 흡수**.
- **Azure Unified Dashboard PoC** (사내 AI 활용 생산성 사례) — Claude Code 활용 **19 커밋 / 약 19,800 LoC** TypeScript 풀스택 모노레포 (Azure Resource Graph / Monitor / Cost Management + ReactFlow 2D / Three.js 3D 토폴로지 + OBO 인증).
- **AI 인프라 운영 가이드 8건+** (Azure OpenAI / Self-hosted LLM SSE / AFD-AGW X-Forwarded / Azure Files SMB / NSG Deny-All / Docker 디스크 / DNS 전파 등) 정립.

---

### 02. 클루커스 (Cloocus) &nbsp;·&nbsp; _2022. 05. ~ 2025. 04._

**Manager / Managed Services Center**

- **고려해운 (KMTC)** — Azure Infra 및 AKS 클러스터 운영 / Azure DevOps CI/CD 파이프라인 운영. **AKS 1.20 → 1.28.9 무중단 Blue/Green 업그레이드** 수행, 오픈소스 CI/CD (Jenkins + ArgoCD) → Azure DevOps 이관으로 관리 포인트 통합.
- **크래프톤 (Krafton)** — AKS 기반 RedisJson PoC. PaaS Redis 대비 기술/성능/제한/비용 비교 검증, **1,000 RedisJson 인스턴스(Pod) 배포** (Terraform + Helm).
- **한독 (Handok)** — 레거시 SAP Azure 마이그레이션 + Azure Landing Zone (Hub & Spoke) 구축. Helm / AKS / GitHub Actions.
- **성주DND (싱가포르 리전)** — 글로벌 CRM SaaS 배포용 Azure Landing Zone 구축. Hub & Spoke, Azure Firewall + Private Endpoint 보안 표준, ELK 통합 로그.

---

### 03. 건우솔루션 &nbsp;·&nbsp; _2018. 10. ~ 2020. 02._

**주임연구원 / 인프라팀**

- **현대 5세대 Wide AVN 프로젝트** — 현대/기아 **31개 차종 AVN 장비**에 대한 SW 형상 관리 및 빌드 자동화 스크립트 유지 관리.
- **Vlink-system 프로젝트** — 다양한 OEM 별 CI/CD 환경 통합. 시나리오/액션별 맞춤형 빌드 시스템 + CLI 기반 빌드 자동화 인터페이스 개발 (Jenkins + Gerrit + Docker + Node.js).

---

### 04. 큐스팟 (Qspot) &nbsp;·&nbsp; _2015. 07. ~ 2018. 07._

**주임연구원 / QA팀**

자동차 텔레매틱스 SW 검증.

- **현대 고급형 6세대 Genesis Telematics**
- **폭스바겐(Volkswagen) OCU Telematics** (Golf)
- **GM Cadillac CTS Telematics** — 해외 현지 필드 검증 포함. 설계 기법 기반 SW 테스트 계획 수립/수행, 릴리즈 프로세스 지속 개선.

---

## 주요 프로젝트 (별도 노출)

### Caidentia AKS 옵저버빌리티 표준 수립 및 Phase 별 구축
_엠로 · 2025. 05. ~ 진행중_

📝 **배경** : 과거 TPS 드랍 사고(HikariCP 부족 / Logback 동기 I/O / SSE 누수 / Tomcat 스레드 점유)를 "대시보드만 보고 2분 내 RCA" 할 수 있는 통합 옵저버빌리티 체계로 재정립
🎯 **과제** : Whatap 단일 의존 + 메트릭 단편화 → Azure 매니지드 서비스(AMW/AMG) 기반 표준 도입, 운영 무중단
🤹 **역할** : 표준 수립 PM 겸 단독 구축자
✅ **성과** :
- Master Plan(Four Golden Signals / RED+USE / SLI-SLO / Error Budget Burn-Rate / 카디널리티 룰) 1문서 표준화
- Phase 0 Terraform Brownfield import (AMG + Monitor Workspace + AAD/RBAC + Alloy DaemonSet)
- Phase 1 Spring Boot + Legacy Spring MVC 동시 계측 표준 정립
- Phase 2 5-Tier 대시보드 JSON-as-Code → 신규 서비스 **30분 내 대시보드 적용**
- Phase 3 Symptom-vs-Cause 알림 + Notification Policy + 런북 11건
- Phase 4 Loki + Tempo on AKS + Azure Blob 설계 + OTel Java Agent + Tail Sampling
- 운영 중 발견한 **함정 11건 누적 회고 문서화**

🔨 **기술** : Azure AKS, Azure Managed Prometheus / Grafana, Grafana Alloy, Loki, Tempo, OpenTelemetry, Micrometer, JMX Exporter, Terraform, Spring 6, Slack + Azure Logic App

---

### Caidentia Ubuntu OS 골든이미지 자동화
_엠로 · 2025. ~ 진행중_

📝 **배경** : OS 골든이미지 빌드가 수동 절차로 운영되어 절차 누락 / 검토 지연 / 감사 추적 부실 위험
🎯 **과제** : CAI-SO-01 통제 만족 + 빌드 코드화 + 클라우드서비스보안파트 수동 승인 게이트 유지 (불변 이미지 정책)
🤹 **역할** : 자동화 설계 및 구현 (단독)
✅ **성과** :
- SSI 체크리스트(AC01~AC06) ↔ Ansible task 감사 트레이서빌리티 100%
- Molecule 기반 Role 단위 테스트 도입
- **GitLab CI (lint + Molecule) + Jenkins (Packer 빌드 / Compute Gallery 게시 / 보안 승인 / smoke-test)** 분담
- KR(koreacentral) → US(eastus) 비동기 스냅샷 복제 + 멀티 리전 Image Version 자동 생성
- 야간 드리프트 점검 Jenkinsfile (Continuous Evaluation)
- WSL 불가 환경 대응 Azure Control VM 셋업 가이드 + INCIDENTS / IMAGE-CAPTURE / SSI-mapping / Versioning 문서

🔨 **기술** : Packer, Ansible (+ Molecule), Jenkins (shared library), GitLab CI, Azure Compute Gallery, Azure Managed Identity, Ubuntu, SSI

---

### Caidentia 멀티테넌트 SaaS + AI 플랫폼 아키텍처 재설계
_엠로 · 2025. ~ 진행중_

📝 **배경** : 3-Tier Shared 구조 (DB/Search/Storage 공유, Demo/POC/Prod 혼재, GPU RI 2대 미활용, CI/CD 없음)
🎯 **과제** : SOC 2 Type II / ISO 27001 / 개인정보보호법 인증 기준 충족 + 매몰비용 (GPU RI) 보존 + 테넌트 격리
🤹 **역할** : 아키텍처 설계 및 의사결정 문서화 (팀 협업)
✅ **성과** :
- 12개 Gap 식별 및 우선순위 매핑
- Hub & Spoke 기반 Spoke 환경 분리 (Prod / STG / Demo) 설계
- AGW Host/Path 라우팅으로 멀티테넌트 도메인 라우팅 (`shared.kdnc.com` 패턴)
- AI 공용 API Gateway + Self-hosted 모델 서빙으로 **GPU RI 2대 흡수** (매몰비용 회피)
- Compliance Architecture Plan (SOC 2 / ISO 27001 / 개인정보보호법) 매핑
- Azure OpenAI Architecture Report (Private Endpoint + 사내 방화벽 + 토큰 풀 / 캐시 설계)

🔨 **기술** : Azure AGW, AFD, AKS / VMSS, Private Endpoint, MI, Azure OpenAI, RBAC, Flyway, Jenkins, Hub & Spoke

---

### Azure Unified Dashboard — AI(Claude Code) 활용 풀스택 운영 플랫폼
_엠로 / 클라우드아키텍처파트 · 2026. ~ 진행중_

📝 **배경** : 사내 Azure 운영자가 여러 포털을 오가던 비효율을 단일 창구로 통합
🎯 **과제** : AI 코딩 도구(Claude Code) 의 실제 생산성 검증 + 엔터프라이즈 표준 (OBO + MSAL + Azure SDK) 준수
🤹 **역할** : 단독 설계 및 구현
✅ **성과** :
- **19 커밋만에 약 19,800 LoC** 풀스택 모노레포 (TypeScript 73 + React/TSX 33 + CSS 12 = 118 파일)
- 21개 API 엔드포인트 / 21개 서비스 모듈 / 8개 프론트엔드 페이지
- 실시간 인프라 토폴로지 (ReactFlow 2D + Three.js 3D), 의존성 자동 추론
- Azure Resource Graph / Monitor / Cost Management / Traffic Analytics / NSG Flow Log / App Insights 등 7개 데이터 소스 통합
- OBO(On-Behalf-Of) 인증 + 데모 Mock 데이터 이중 모드
- 사내 "AI 활용 생산성 향상 Usecase" 공식 등록

🔨 **기술** : TypeScript 5.7, Next.js 16, React 19, Express, Azure MSAL (OBO), Azure SDK (identity, arm-resourcegraph, storage-blob), ReactFlow, Three.js, D3.js, ELK.js, Zod, Claude Code

---

### 고려해운 AKS 클러스터 무중단 버전 업그레이드 및 CI/CD 통합
_클루커스 · 2024. 06. ~ 2024. 08._

📝 **배경** : AKS 클러스터 EOL 도래로 무중단 버전 업그레이드 및 배포 필요 (1.20 → 1.28.9)
🤹 **역할** : PM, 구축 이행
✅ **성과** :
- 신규 AKS 클러스터 Blue/Green 배포 (downtime 0)
- 오픈소스 CI/CD (Jenkins + ArgoCD) → Azure DevOps 이관
- Azure 플랫폼으로 관리 포인트 통합

🔨 **기술** : Azure, Kubernetes, Azure DevOps CI/CD, Jenkins, ArgoCD, Maven, Spring Boot, Docker

---

### 크래프톤 AKS for RedisJson PoC
_클루커스 · 2022. 06. ~ 2022. 07._

📝 **배경** : PaaS형 Redis 대비 AKS 기반 RedisJson 의 기술/성능/제한/비용 비교 검증
🤹 **역할** : 팀원, 구축 이행
✅ **성과** : **1,000개의 RedisJson 인스턴스 (Pod) 배포**, 향후 게임 서버 워크로드를 위한 수평 확장 검증
🔨 **기술** : Azure cloud, AKS, Helm, Powershell, GitHub Actions, Terraform

---

### 한독 / 성주DND Azure Landing Zone 구축
_클루커스 · 2023. 01. ~ 2023. 10._

- **한독** : 레거시 SAP 마이그레이션 + 차세대 프로젝트용 Landing Zone (Hub & Spoke)
- **성주DND** : 글로벌 CRM SaaS 싱가포르 리전 배포용 Landing Zone (Hub & Spoke + Azure Firewall + Private Endpoint + ELK)

🔨 **기술** : Azure (AGW, AKS, Hub & Spoke, Firewall, Private Endpoint), Helm, ELK, PowerShell, GitHub Actions

---

### OpenShift Container Platform (PaaS) 폐쇄망 구축
_전파진흥협회 / 클라우드 서비스 개발 전문가 과정 · 2021. 07. ~ 2021. 10._

📝 **배경** : 폐쇄망 (물리 서버) 환경에서 OpenShift Container Platform PaaS 구축
✅ **시사점** : **on-prem AI 워크로드 배포 패턴에 직접 활용 가능한 자산**

🔨 **기술** : Git, CentOS, CoreOS, OpenShift, ESXi Host, Prometheus, Grafana, HAProxy

---

### VMware Private Cloud 구축 (미니 프로젝트)
_전파진흥협회 / 클라우드 서비스 개발 전문가 과정 · 2021. 04. ~ 2021. 06._

가상 고객 시나리오 기반 VMware vSphere 프라이빗 클라우드 구축 — vCenter, ESXi 호스트 3대, 가상 서버 4대, vMotion / DRS / HA / P2V 마이그레이션.

---

### Vlink-system (멀티 OEM CI/CD 통합)
_건우솔루션 · 2019. 07. ~ 2020. 01._

다양한 OEM 별 CI/CD 환경을 단일 시스템에 통합. 시나리오/액션별 빌드 세분화 + CLI 기반 빌드 자동화 인터페이스.

🔨 **기술** : Git, Gerrit, Jenkins, Jira, Collab, Docker, Node.js

---

## 자격증

| 자격증 | 취득 | 발급기관 |
|--------|------|----------|
| Certified Kubernetes Security Specialist (**CKS**) | 2024. 03. | The Linux Foundation |
| Certified Kubernetes Application Developer (**CKAD**) | 2024. 02. | The Linux Foundation |
| Certified Kubernetes Administrator (**CKA**) | 2022. 09. | The Linux Foundation _(갱신 상태 — 확인 필요)_ |
| Microsoft Certified: **Azure Solutions Architect Expert** (AZ-305) | 2022. 08. | Microsoft |
| Microsoft Certified: Azure Administrator Associate (AZ-104) | 2022. 08. | Microsoft |
| NAVER Cloud Platform Certified Associate | 2020. 10. | NAVER Cloud |
| ISTQB Certified Tester — Foundation Level (CTFL) | 2016. 11. | ISTQB |

---

## 학력 / 교육

**중부대학교** &nbsp;·&nbsp; _2008. 03. ~ 2015. 02._
B.S. 미디어소프트웨어 (학사 졸업)

**한국전파진흥협회 (KRRA)** — 사설 교육
- Kubernetes 기반 MSA 개발 과정 &nbsp;·&nbsp; _2021. 11. ~ 2021. 12._
- 클라우드 서비스 개발 전문가 과정 &nbsp;·&nbsp; _2021. 04. ~ 2021. 10._

---

## 외국어

| 언어 | 수준 |
|------|------|
| 한국어 | 원어민 |
| English | 비즈니스 — 읽기/쓰기 능숙, 회화 일상 가능 |

---

## 자기소개

저는 **SW 검증(QA) → CI/CD 자동화 → Cloud Infrastructure → SRE/Observability** 로 영역을 확장해온 **8년차 엔지니어**입니다. 자동차 텔레매틱스 SW 검증(GM/VW/현대) → Jenkins/Gerrit/Docker 기반 멀티 OEM CI/CD 통합 시스템 구축 → Azure AKS 운영 / Landing Zone 설계 → 현재 Brownfield 환경의 옵저버빌리티 표준 수립을 담당하고 있습니다.

**엠로 클라우드아키텍처파트**에서는 Caidentia 운영 환경의 SRE 표준을 처음부터 정립하고 있습니다. 대표적인 산출물로 (1) Azure AKS 위 Spring Boot + Legacy Spring MVC 통합 옵저버빌리티 표준(Master Plan + Phase 0~4) 및 런북 11건, (2) Packer + Ansible + Jenkins 기반 Ubuntu OS 골든이미지 자동화 (CAI-SO-01 통제, SSI AC01~AC06 자동 매핑, KR→US 멀티 리전 복제, 야간 드리프트 점검), (3) 3-Tier Shared → Multi-tenant SaaS 재설계 (SOC2 / ISO 27001 / 개인정보보호법 대응, AGW 도메인 라우팅, GPU RI 2대 흡수 설계), (4) AI(Claude Code) 활용 사내 운영 플랫폼 PoC (Azure Unified Dashboard, 19 커밋 / 약 19,800 LoC 풀스택) 가 있습니다.

이전 경력에서는 **클루커스(2022.05~2025.04)** 에서 고려해운 AKS 무중단 버전 업그레이드(1.20→1.28.9 Blue/Green), 한독 · 성주DND Azure Landing Zone 구축, 크래프톤 AKS 기반 RedisJson 1000-Pod PoC, OpenShift 폐쇄망 구축 등을 담당했습니다.

운영 철학은 **"Phase 별 종료 조건 + 함정 누적 회고"** 입니다. 모든 변경을 작은 단위로 끊고, 실패에서 배운 함정을 반드시 다음 Phase 에 반영하는 방식이 Brownfield 환경의 회복력을 결정한다고 믿습니다. **향후 방향은 AI 인프라와 멀티클라우드(AWS/GCP) 플랫폼 엔지니어링이며, 대규모 AI 워크로드를 위한 옵저버빌리티 / 자동화 / 멀티 배포 모델(cloud / private cloud / on-prem) 운영에 깊이 기여하고자 합니다.**
