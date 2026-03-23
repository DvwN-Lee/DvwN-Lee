# GitHub Profile Redesign — Design Document

**작성일**: 2026-03-06
**상태**: 분석 완료 / 구현 보류
**관련 문서**:
- [`2026-03-05-korean-ai-agent-job-market-analysis.md`](./2026-03-05-korean-ai-agent-job-market-analysis.md)
- [`2026-03-05-company-ai-hiring-deep-dive.md`](./2026-03-05-company-ai-hiring-deep-dive.md)

---

## 1. 현황 분석

### 1.1 현재 README 문제점

| 항목 | 현재 상태 | 문제점 |
|------|----------|--------|
| 직함 | Cloud Platform Engineer \| DevOps Engineer | AI 엔지니어 포지셔닝 전혀 없음 |
| 소개 | K8s/IaC/DevOps 자동화 중심 | AI Agent/LLM 관련 내용 없음 |
| 기술 스택 | 인프라 도구만 나열 | Python/LangChain/PyTorch 등 AI 스택 없음 |
| 동적 요소 | 없음 (정적 배지만) | Typing SVG, 스네이크 애니메이션 없음 |
| GitHub Stats | 통계 위젯 있음 | Streak, Top Langs 없음 |
| 전략성 | 없음 | 취업 키워드 반영 안됨 |

### 1.2 레퍼런스 분석 (boshyxd 스타일)

채택 가능한 요소:
- `capsule-render` waving 헤더 (현재도 사용 중)
- `readme-typing-svg` — JetBrains Mono, 멀티라인 순환 텍스트
- `Platane/snk` GitHub 기여 스네이크 애니메이션
- `github-readme-streak-stats` — 연속 기여일 위젯
- 깔끔한 2단 테이블 레이아웃

---

## 2. 포지셔닝 전략

### 2.1 세 가지 옵션

| 옵션 | 설명 | 장점 | 단점 |
|------|------|------|------|
| **A: 완전 AI 피벗** | DevOps 스택 최소화, AI/LLM 전면 | 명확한 포지셔닝 | 실제 경험과 괴리 가능성 |
| **B: DevOps + AI 하이브리드** | 인프라 강점 유지 + AI 역량 추가 | 현재 경험 솔직하게 반영 | 어중간해 보일 수 있음 |
| **C: AI-Agent 메인, DevOps 백그라운드** ✅ | 헤더·소개는 AI, 기술 스택에 인프라 포함 | 한국 취업 시장 최적화 | — |

### 2.2 Option C 선택 근거 (시장 데이터 기반)

한국 AI 채용 시장 분석 결과, **인프라 경험이 AI Agent 엔지니어 채용의 실질적 차별화 요소**임이 확인됨:

- **현대오토에버** JD: A2A + MCP + Kubernetes 동시 요구 → DevOps 배경 직접 적용
- **KT**: AI 연봉 상한 폐지, MS/석사 신입에 2년 경력 인정, B2G 인프라 경험 가산점
- **LG CNS**: LLMOps 파이프라인 운영 + K8s 클러스터 관리 동시 요구
- 순수 AI 역할(Samsung Research, LG AI Research, SKT)은 MS/PhD + 논문 실적 사실상 필수

**결론**: AI-Agent Engineer로 포지셔닝하되, K8s/Terraform/DevOps 백그라운드를 *차별화 강점*으로 명시.

### 2.3 타깃 기업 티어 (DevOps→AI 전환 기준)

```
높은 접근성 (즉시 지원 가능)
├── 현대오토에버 — MCP/A2A + 인프라 경험 명시 요구
├── KT — sLLM 전략, B2B/B2G, 연봉 상한 폐지
└── LG CNS — LLMOps + K8s 동시 요구

중간 접근성 (LangChain/RAG 프로젝트 추가 후)
├── 토스 — ML 플랫폼, Kubeflow/MLflow, 재현 가능한 실험 중시
├── 카카오페이 — 금융 AI, 실용적 스택
└── Upstage / Wrtn — 스타트업, 풀스택 AI 엔지니어

낮은 접근성 (MS/PhD + 논문 사실상 필수)
├── Samsung Research — Gauss LLM
├── LG AI Research — EXAONE
├── SKT — A.X K1 (519B MoE)
└── Naver — HyperCLOVA X THINK
```

---

## 3. 비주얼 디자인

### 3.1 스타일: Monochrome Minimal (권장)

- `capsule-render` 그라디언트 웨이빙 헤더 (현재와 동일 유지)
- `readme-typing-svg` — JetBrains Mono, `58A6FF` (GitHub 블루), 22px
- shields.io `for-the-badge` 스타일 — 현재 스타일 유지
- GitHub Dark 테마 Stats 위젯

### 3.2 구조 설계

```
[Header] capsule-render waving
[Typing SVG] AI Agent Engineer | LangChain | RAG | MCP | ...
[Introduction] Korean, AI-Agent 포지셔닝
[🤖 AI & LLM Stack]
  └── Languages & Backend (Python, Go, FastAPI)
  └── LLM & ML (PyTorch, HuggingFace, OpenAI)
  └── AI Agent Framework (LangChain, LangGraph, MCP)
  └── LLMOps & Vector DB (RAG, MLflow, ChromaDB, vLLM)
[🏗️ Cloud & Infrastructure] (기존 스택 유지, 섹션 격하)
  └── Container & Orchestration (K8s, Docker, Helm)
  └── IaC & GitOps (Terraform, Ansible, ArgoCD, GH Actions)
  └── Monitoring & Observability (Prometheus, Grafana, Loki)
[📊 GitHub Stats] Stats + Top Langs + Streak
[🔭 Featured Projects] 기존 2개 프로젝트 (설명 AI 관련으로 리프레이밍)
[🎯 Current Focus] AI Agent / MCP / LLMOps / AI Infra
[🐍 Contribution Snake Animation]
[📬 Contact]
[Footer] capsule-render waving
```

---

## 4. 기술 스택 배지 설계

### 4.1 AI/LLM Stack (신규 추가)

```html
<!-- Languages & Backend -->
Python-3776AB | Go-00ADD8 | FastAPI-009688

<!-- LLM & ML -->
PyTorch-EE4C2C | HuggingFace-FFD21E | OpenAI-412991

<!-- AI Agent Framework -->
LangChain-1C3C3C | LangGraph-1C3C3C | MCP-D4A574 (anthropic logo)

<!-- LLMOps & Vector DB -->
RAG-4A90D9 | MLflow-0194E2 | ChromaDB-FF6B35 | vLLM-7C3AED
```

### 4.2 Infrastructure (기존 유지, 섹션 격하)

```html
<!-- Container & Orchestration -->
Kubernetes-326CE5 | Docker-2496ED | Helm-0F1689

<!-- IaC & GitOps -->
Terraform-7B42BC | Ansible-EE0000 | ArgoCD-EF7B4D | GitHub_Actions-2088FF

<!-- Monitoring -->
Prometheus-E6522C | Grafana-F46800 | Loki-F46800
```

### 4.3 제거 항목 (정리 대상)

- `CloudStack`, `containerd`, `MetalLB`, `Cilium` — 너무 세부적, 노이즈
- `Jenkins`, `GitLab` — ArgoCD/GitHub Actions로 대표
- `AlertManager`, `k6` — Current Focus 텍스트로 언급 대체
- `Django`, `MySQL`, `CSS3`, `HTML5`, `JavaScript` — AI 프로필과 무관

---

## 5. 동적 요소

### 5.1 Typing SVG

```
URL: https://readme-typing-svg.demolab.com
Font: JetBrains+Mono
Weight: 600, Size: 22
Color: 58A6FF (GitHub Blue)
Lines:
  - "AI Agent Engineer 🤖"
  - "LangChain | LangGraph | RAG"
  - "MCP | LLMOps | MLOps"
  - "Cloud Native AI Infrastructure"
```

### 5.2 GitHub 스네이크 애니메이션

워크플로 파일: `.github/workflows/snake.yml`

```yaml
# 핵심 설정
uses: Platane/snk/svg-only@v3
outputs:
  - dist/github-contribution-grid-snake.svg
  - dist/github-contribution-grid-snake-dark.svg?palette=github-dark
target_branch: output  # raw.githubusercontent.com/DvwN-Lee/DvwN-Lee/output/...
```

**활성화 방법**: GitHub Push 후 Actions 탭에서 "Generate Snake Animation" 수동 실행 1회 필요.

### 5.3 GitHub Stats 위젯 (3종)

```html
<!-- Stats + Top Languages (나란히) -->
github-readme-stats: theme=github_dark, hide_border=true
github-readme-stats/top-langs: layout=compact, langs_count=7

<!-- Streak Stats (별도 행) -->
github-readme-streak-stats: theme=github-dark-blue, hide_border=true
```

---

## 6. 헤더 텍스트 변경

| 위치 | 현재 | 변경안 |
|------|------|--------|
| capsule-render `desc` | `Cloud%20Platform%20Engineer%20%7C%20DevOps%20Engineer` | `AI%20Agent%20Engineer%20%7C%20LLMOps%20Engineer` |
| Introduction 핵심 키워드 | Kubernetes Orchestration, IaC, DevOps Automation | LLM 기반 AI Agent, RAG 파이프라인, MCP, 클라우드 네이티브 AI 인프라 |
| Current Focus | Security & Compliance, Performance, Network | AI Agent Dev, MCP Ecosystem, LLMOps Pipeline, AI Infrastructure |

---

## 7. 구현 시 참고 사항

### 7.1 우선순위

1. **헤더 + Typing SVG + Introduction 교체** — 포지셔닝 즉시 변경
2. **AI Stack 테이블 추가** — 상단 배치, Infrastructure 섹션은 하단으로 이동
3. **Stats 위젯 추가** — 이미 기반 있음, 테마 통일
4. **스네이크 워크플로 추가** — GitHub Actions 설정 1회 필요
5. **기존 스택 정리** — 불필요한 배지 제거

### 7.2 한국 AI 취업 키워드 (JD 최빈 키워드 Top 10)

```
1위  Python          (전체 JD 94%)
2위  LangChain       (AI Agent JD 78%)
3위  RAG             (AI Agent JD 71%, YoY +2,047%)
4위  LLM             (플랫폼 추출 기준 699건)
5위  FastAPI         (백엔드 AI 서비스 62%)
6위  Docker/K8s      (AI 인프라 JD 58%)
7위  PyTorch         (ML 엔지니어 JD 67%)
8위  LangGraph       (2025 신흥 강세)
9위  MCP             (2025 킬러 키워드, 현대오토에버 명시)
10위 HuggingFace     (모델 허브, 파인튜닝 JD)
```

### 7.3 주의: 과장 없이 작성

현재 실제 프로젝트(Monitoring-v2, k8s-cicd-automation)는 DevOps 프로젝트입니다.
AI 스택 배지 추가 시 **실제 사용 경험이 있는 항목만** 포함할 것을 권장합니다.
AI 관련 사이드 프로젝트 완성 후 Featured Projects 섹션도 업데이트 예정.

---

## 8. 기존 분석 문서 링크

| 문서 | 내용 |
|------|------|
| [`korean-ai-agent-job-market-analysis.md`](./2026-03-05-korean-ai-agent-job-market-analysis.md) | 채용 플랫폼 통계, JD 기술 스택 Top 20, 연봉 테이블, 커리어 전환 경로 |
| [`company-ai-hiring-deep-dive.md`](./2026-03-05-company-ai-hiring-deep-dive.md) | 토스/삼성/LG/현대/카카오/네이버/SKT/KT 회사별 AI 채용 심층 분석 |
