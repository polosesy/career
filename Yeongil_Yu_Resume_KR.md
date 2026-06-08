# 유영일 (책임)

**Senior Cloud Architect · SRE · DevOps Engineer**

📧 yeongil6012@gmail.com &nbsp;·&nbsp; 📱 010-2669-6014 &nbsp;·&nbsp; 📍 Seoul, South Korea

LinkedIn: _[TBD]_ &nbsp;·&nbsp; GitHub: _[TBD]_

---

## 한줄 소개

8년차 Cloud Infrastructure / DevOps / SRE 엔지니어. **QA → 형상관리,CI/CD → Cloud Architect → SRE/Observability** 로 영역을 확장하며 Azure 환경에서 AKS 운영, Landing Zone 설계, **옵저버빌리티(Prometheus / Grafana / Alloy + OTel) 표준 수립**, SSI 체크리스트 기반 OS 골든이미지 하드닝 스크립트 자동화, 멀티테넌트 SaaS 재설계를 주도해왔습니다. **KCNA · CKS · CKAD · CKA + Azure Solutions Architect Expert** 보유. 현재 AI 인프라와 멀티클라우드 플랫폼 엔지니어링으로 영역을 확장 중입니다.

---

## 핵심 역량 / 기술 스택

| 영역 | 스택 |
|------|------|
| **Cloud** | Azure (Expert), NCP, AWS / GCP |
| **Container** | Kubernetes (AKS, EKS, OpenShift), Docker, Helm |
| **IaC** | Terraform, ARM |
| **CI / CD** | Jenkins (shared library), GitLab CI, Azure DevOps, ArgoCD |
| **Observability** | Prometheus, Grafana, Grafana Alloy, OpenTelemetry, Loki, Tempo, Micrometer, JMX Exporter |
| **SRE 실무** | SLI / SLO, Error Budget Burn-Rate, RED + USE, Runbook 표준화, Incident Postmortem, DR / BCP (Warm Standby, RTO / RPO, Region Failover) |
| **언어** | PowerShell · Bash (자동화 사용) · Java / Spring (운영·계측 대상) · TypeScript / Node.js · Python (AI 보조 개발) |
| **AI 도구** | Claude Code |

---

## 경력

### 01. 주식회사 엠로 (emro) &nbsp;·&nbsp; _2025. 05. ~ 재직중_

**책임 / 클라우드아키텍처파트**

Caidentia SaaS 플랫폼의 Azure 환경을 구축하고, Best Practice(CAF / WAF) 기준으로 아키텍처·거버넌스를 설계·구축. 이후 아키텍처·운영 고도화(멀티테넌트 재설계, 옵저버빌리티 표준, OS 자동화)를 주도.

**아키텍처 / 거버넌스 (주 업무)**

- **Caidentia Azure SaaS 플랫폼 환경 구축** — Best Practice(CAF / WAF) 기준 Landing Zone · Hub & Spoke 토폴로지 / 구독 분리 구조, 환경별 경계(Prod / STG ), Terraform 기반 IaC 인프라 프로비저닝.
- **Azure 거버넌스 체계 설계·구축** — Azure Policy(deny / audit) · 네이밍 · 태깅 표준, RBAC 권한 위임 · 최소 권한 · PIM(Just-in-Time) · Managed Identity, Defender for Cloud · NSG / 방화벽 · Private Endpoint 보안 베이스라인.
- **FinOps 비용 최적화** — 예약·약정 할인(RI / Savings Plan), Rightsizing · SKU 조정, 비운영(Dev / Demo) 환경 스케줄 정지·축소, 미사용 리소스 정리 + 스토리지 / 로그 보존정책 최적화, 예산 알림 체계 → **월 운영비 약 55% 절감 (연환산 약 1.3억원 규모, 8개월간 지속 우하향)**.
- **멀티테넌트 SaaS 아키텍처 재설계 (To-Be 설계 주도, 팀 협업)** (3-Tier Shared → 테넌트 격리), Hub & Spoke + AFD + AGW 도메인 라우팅, **Shared 서비스 계층(공용 DB / Search / Storage / AI Gateway) 표준화** 설계.

**아키텍처 / 운영 고도화**

- **Caidentia AKS 옵저버빌리티 표준 수립** 5-Tier 대시보드 구조, SLI/SLO + Error Budget Burn-Rate 알림 체계 정의.
- **Spring Boot + Legacy Spring MVC/Tomcat 통합 계측 트랙** 설계 — Micrometer + OpenTelemetry + PrometheusMeterRegistry + JMX Exporter sidecar 를 **Grafana Alloy DaemonSet 한 곳으로 수렴**해 Azure Managed Prometheus / Loki / Tempo 로 전송. (Terraform import, **런북 11건** 포함)
- **Caidentia OS 골든이미지 자동화 (PoC, 운영 미적용)** (Packer + Ansible + Jenkins, CAI-SO-01 통제) — SSI(AC01~AC06) ↔ Ansible role 감사 매핑, Molecule 단위 테스트, **GitLab CI(lint) + Jenkins(빌드/게시/승인) 분담**, KR→US 비동기 복제·야간 드리프트 점검 설계 검증.

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
_엠로 · 2026. 05. ~ 진행중_

📝 **배경** : Caidentia 운영 환경이 단일 APM(Whatap)에 의존하고 메트릭이 단편화되어, Spring Boot + Legacy Spring MVC 혼재 워크로드 전반의 SLI/SLO 정의와 일관된 장애 원인 분석(RCA)이 어려운 상태 — 표준화된 옵저버빌리티 체계 부재.
🎯 **과제** : Whatap 단일 의존 + 메트릭 단편화 → Azure 매니지드 서비스(AMW/AMG) 기반 표준 도입, 운영 무중단
🤹 **역할** : 옵저버빌리티 표준 자발적 제안 및 단독 구축 (Brownfield, 운영 적용 진행중)
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

### Caidentia 멀티테넌트 SaaS + 단일 엔터프라이즈 SaaS
_엠로 · 2025. ~ 진행중_

📝 **배경** : 3-Tier 구조 (DB/Storage 공유, Demo/POC/Prod 혼재)
🎯 **과제** : SOC 2 Type II / ISO 27001 인증 기준 충족 + 테넌트 격리
🤹 **역할** : 아키텍처 설계 및 의사결정 문서화 (팀 협업)

🏗️ **서비스 아키텍처 설계 구성** :
- **네트워크 토폴로지** — Hub & Spoke 기반으로 환경별 Spoke(Prod / STG) 분리, Hub 에 공용 보안/게이트웨이 집약. 외부 진입은 AFD → AGW 2단 계층, 내부 통신은 Private Endpoint + Private DNS 로 폐쇄.
- **트래픽 / 테넌트 라우팅** — AGW Host/Path 라우팅으로 테넌트별 도메인 분기, 테넌트 식별 → 백엔드 풀 매핑.
- **워크로드 계층** — AKS(MSA) 워크로드 구성, 3Tier VMSS 구성, Managed Identity + RBAC 기반 최소 권한 관리.

🧩 **Shared 서비스 아키텍처 구성** :
- **Shared Tier 분리** — 테넌트 공통 기능(공용 RDB · Search · Object Storage · AI Gateway)을 단일 공유 계층으로 표준화.
- **테넌트 데이터 격리 경계** — 공유 자원 내 테넌트 키 기반 논리 격리에서 출발 → 단계적 물리 격리 전환 경로 설계.
- **배치 · 리스크 검토** — Shared 자원은 Hub/공용 Spoke 에 배치(Private Endpoint 접근), 공용 컴포넌트의 SPOF · 카디널리티 영향 사전 검토.

✅ **성과** :
- **현행 분석** — 기존 구조 Gap 12건 식별 및 우선순위 매핑
- **To-Be 아키텍처 문서화** — Hub & Spoke + Shared Tier 분리 기반 목표 아키텍처 설계서
- **멀티테넌트 라우팅 설계** — AGW Host/Path 기반 테넌트별 도메인 분기
- **컴플라이언스 매핑** — SOC 2 / ISO 27001 기준 Compliance Architecture Plan

🔨 **기술** : Azure AGW, AFD, AKS / VMSS, Private Endpoint, MI, Azure OpenAI, RBAC, Jenkins, Hub & Spoke

---

### Caidentia DR(재해복구) Zone 설계 및 Warm Standby 구성
_엠로 · 2025.08 ~ 2025.10_

📝 **배경** : Caidentia 운영 환경의 리전 단위 재해(Region Outage)에 대비한 DR Zone 부재 → 핵심 자원(DB / Storage) 복구 체계 필요
🎯 **과제** : **RTO 15분 / RPO 1시간** 충족 + DR 상시 유지 비용 최소화(Warm Standby) + Azure 관리형 Failover 의 "사용자 테스트 불가" 한계 우회
🤹 **역할** : DR 아키텍처 설계 · Terraform 코드화 · DR 훈련 절차 및 DR 훈련 시행 (가이드 표준화)
✅ **성과** :
- **비용 계층화 Warm Standby 설계** — 상시 유지(거의 무과금: VNet / Subnet / NAT Gateway) vs 재해 시 Terraform 수동 생성(AGW / LB / Redis / VM) 으로 자원 분리
- **PostgreSQL Flexible 읽기 복제본 + Virtual Endpoint** — Pair Region 비의존 복제, Failover 시 Endpoint 변경 무중단(Primary 자동 중계) (RTO 7초 / RPO 20분)
- **RA-GRS(읽기 전용 지역 중복) Blob Storage** — Pair Region 자동 복제, Failover 시 Primary Endpoint 메뉴얼 승격 (RTO 15분 / RPO 20분)
- **DR 훈련 절차 표준화** — 관리형 Failover(Key Vault 등) 테스트 불가 한계를 "Failover 발생 가정 + Pair Region 사전 구성"으로 우회, Staging-Primary 훈련 시 Storage 읽기 복제본 추가 구성 가이드
- **Caidentia DR Terraform 구성 코드** — 재해 시 생성 자원(AGW / LB / Redis / VM) 코드화로 복구 재현성 확보

🔨 **기술** : Azure (East US ↔ West US Region Pair, Failover), PostgreSQL Flexible Server (Virtual Endpoint, Read Replica), RA-GRS Blob Storage, Terraform

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
| Kubernetes and Cloud Native Associate (**KCNA**) | 2026. 01. | The Linux Foundation |
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
B.S. 게임학과 (학사 졸업)

**한국전파진흥협회 (KRRA)** — 사설 교육
- Kubernetes 기반 MSA 개발 과정 &nbsp;·&nbsp; _2021. 11. ~ 2021. 12._
- 클라우드 서비스 개발 전문가 과정 &nbsp;·&nbsp; _2021. 04. ~ 2021. 10._

---

## 외국어

| 언어 | 수준 |
|------|------|
| 한국어 | 원어민 |
| English | 읽기/쓰기 기본 가능 (AI 도구 활용), 회화는 기초 수준 |

---

## 자기소개

저는 **SW 검증(QA) → CI/CD 자동화 → Cloud Infrastructure → SRE/Observability** 로 영역을 확장해온 **8년차 엔지니어**입니다. 자동차 텔레매틱스 SW 검증(GM/VW/현대) → Jenkins/Gerrit/Docker 기반 멀티 OEM CI/CD 통합 시스템 구축 → Azure AKS 운영 / Landing Zone 설계 → 현재 Brownfield 환경의 옵저버빌리티 표준 수립을 담당하고 있습니다.

**엠로 클라우드아키텍처파트**에서는 Caidentia 운영 환경의 SRE 표준을 정립하고 있습니다. 대표적인 산출물로 (1) Azure AKS 위 Spring Boot + Legacy Spring MVC 통합 옵저버빌리티 표준(Master Plan + Phase 0~4) 및 런북 11건, (2) Packer + Ansible + Jenkins 기반 Ubuntu OS 골든이미지 자동화 (CAI-SO-01 통제, SSI AC01~AC06 자동 매핑, 야간 드리프트 점검), (3) 3-Tier Shared → Multi-tenant SaaS 재설계 (SOC2 / ISO 27001 대응, Shared 서비스 계층 표준화, AGW 도메인 라우팅, GPU RI 2대 흡수 설계), (4) Caidentia DR(재해복구) Zone 설계 (Warm Standby, PostgreSQL Virtual Endpoint + RA-GRS, RTO 15분 / RPO 1시간, Terraform 코드화) 가 있습니다.

이전 경력에서는 **클루커스(2022.05~2025.04)** 에서 고려해운 AKS 무중단 버전 업그레이드(1.20→1.28.9 Blue/Green), 한독 · 성주DND Azure Landing Zone 구축, 크래프톤 AKS 기반 RedisJson 1000-Pod PoC 등을 담당했습니다.

운영 철학은 **"Phase 별 종료 조건 + 함정 누적 회고"** 입니다. 모든 변경을 작은 단위로 끊고, 실패에서 배운 함정을 반드시 다음 Phase 에 반영하는 방식이 Brownfield 환경의 회복력을 결정한다고 믿습니다. **향후 방향은 AI 인프라와 멀티클라우드(AWS/GCP) 플랫폼 엔지니어링이며, 대규모 AI 워크로드를 위한 옵저버빌리티 / 자동화 / 멀티 배포 모델(cloud / private cloud / on-prem) 운영에 깊이 기여하고자 합니다.**
