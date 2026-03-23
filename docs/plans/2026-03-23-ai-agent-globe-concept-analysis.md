# AI Agent 컨셉 기반 Tech Stack Globe 재구성 분석

**작성일**: 2026-03-23
**목적**: 행성/궤도 시각화를 AI Agent 아키텍처 관점으로 재구성

---

## 1. 현재 구조의 문제

현재 궤도 분류는 **기술 유형별 분류**(AI Core / Languages / Infrastructure)로, 일반적인 개발자 프로필과 차별점이 없음.

```
현재:
  Inner  → AI CORE (LangGraph, MCP, Gemini, LangFuse)
  Middle → LANGUAGES (Python, TypeScript, Go, FastAPI)
  Outer  → INFRASTRUCTURE (K8s, Docker, Terraform, ArgoCD, Prometheus, Grafana)
```

이 구조는 "어떤 기술을 아는지"를 보여주지만, **"AI Agent Engineer로서 무엇을 하는지"**는 보여주지 않음.

---

## 2. AI Agent 아키텍처 기반 재구성

### 2.1 AI Agent의 동작 원리

```
                    ┌─────────────┐
                    │   Observe   │ ← 결과 관측/추적
                    └──────┬──────┘
                           │
┌──────────┐    ┌──────────▼──────────┐    ┌──────────┐
│  Reason  │───▶│     Agent Core      │───▶│   Act    │
│ (Think)  │◀───│  (Orchestration)    │◀───│ (Tools)  │
└──────────┘    └──────────┬──────────┘    └──────────┘
                           │
                    ┌──────▼──────┐
                    │   Deploy    │ ← 프로덕션 배포/운영
                    └─────────────┘
```

AI Agent는 **Reason → Act → Observe** 루프를 반복하며, 이 전체가 **Deploy** 인프라 위에서 실행됨.

### 2.2 궤도 재분류안

| 궤도 | AI Agent 역할 | 기술 스택 | 의미 |
|------|-------------|----------|------|
| **중심** | Agent Core | — | 오케스트레이션 허브 |
| **1궤도** | **Reason** (추론) | Gemini, LangGraph | Agent의 두뇌 — LLM 추론 + 워크플로 계획 |
| **2궤도** | **Act** (실행) | MCP, Python, TypeScript, FastAPI | Agent의 손 — Tool Calling, API 연동, 코드 실행 |
| **3궤도** | **Observe** (관측) | LangFuse, Prometheus, Grafana | Agent의 눈 — 추적, 메트릭, 대시보드 |
| **4궤도** | **Deploy** (배포) | K8s, Docker, Terraform, ArgoCD, Go | Agent의 발 — 프로덕션 인프라, 컨테이너, IaC |

---

## 3. 궤도별 상세 설계

### 3.1 중심 — Agent Core

```
기존: "AI Agent Engineer" 텍스트
개선안:
  - "Agent Core" 또는 유지
  - 중심 원에 뇌/프로세서 아이콘 추가 가능
  - 글로우 효과 유지 (허브 강조)
```

### 3.2 1궤도 — Reason (추론)

Agent가 "생각하는" 레이어. LLM 호출, 계획 수립, 의사결정.

| 기술 | 역할 |
|------|------|
| **Gemini** | LLM Provider — 자연어 이해, 추론, 응답 생성 |
| **LangGraph** | Workflow Orchestration — StateGraph 기반 멀티스텝 계획 |

- 2개 아이템 → 가장 빠르게 회전 (핵심 루프)
- 궤도 라벨: `REASON`

### 3.3 2궤도 — Act (실행)

Agent가 "행동하는" 레이어. 외부 세계와 상호작용.

| 기술 | 역할 |
|------|------|
| **MCP** | Tool Protocol — 외부 도구 연결 표준 (DART API, KRX 등) |
| **Python** | Primary Runtime — Agent 로직, 데이터 처리 |
| **TypeScript** | MCP Server 개발 — gemini_mcp 등 도구 구현 |
| **FastAPI** | API Layer — Agent 엔드포인트, 웹훅, REST 인터페이스 |

- 4개 아이템 → 중간 속도
- 궤도 라벨: `ACT`

### 3.4 3궤도 — Observe (관측)

Agent의 동작을 추적하고 모니터링하는 레이어.

| 기술 | 역할 |
|------|------|
| **LangFuse** | LLM Tracing — Agent 호출 추적, 비용 모니터링, 프롬프트 관리 |
| **Prometheus** | Metrics — TTFT, TPS, TPOT, 레이턴시 계측 (obLLMa) |
| **Grafana** | Dashboard — LLM 서빙 메트릭 시각화, 알림 |

- 3개 아이템 → 중간-느린 속도
- 궤도 라벨: `OBSERVE`

### 3.5 4궤도 — Deploy (배포)

Agent를 프로덕션에 배포하고 운영하는 인프라 레이어.

| 기술 | 역할 |
|------|------|
| **Docker** | Containerization — Agent 서비스 컨테이너화 |
| **Kubernetes** | Orchestration — Agent 클러스터 운영, 스케일링 |
| **Terraform** | IaC — 인프라 프로비저닝 자동화 |
| **ArgoCD** | GitOps — Agent 서비스 배포 자동화 |
| **Go** | Infrastructure Tooling — CLI 도구, 모니터링 서비스 (Monitoring-v3) |

- 5개 아이템 → 가장 느리게 회전 (안정적 기반)
- 궤도 라벨: `DEPLOY`

---

## 4. 시각적 표현 전략

### 4.1 궤도별 회전 방향

```
REASON  → 시계 방향 (빠름, 20s) — 끊임없는 사고
ACT     → 반시계 방향 (중간, 35s) — 실행과 반응
OBSERVE → 시계 방향 (중간, 45s) — 지속적 감시
DEPLOY  → 반시계 방향 (느림, 60s) — 안정적 기반
```

교차 회전으로 시각적 역동성 + 각 레이어의 독립성 표현.

### 4.2 궤도별 색상 전략

브라운 베이스 유지하되, 각 궤도에 기능적 색상 힌트 추가:

| 궤도 | 라벨 색상 | 의미 |
|------|----------|------|
| REASON | `#E8C49A` (밝은 골드) | 지성, 사고 |
| ACT | `#D4A574` (카라멜) | 실행, 행동 |
| OBSERVE | `#C8956C` (코퍼) | 관찰, 분석 |
| DEPLOY | `#8B6914` (다크 골드) | 기반, 안정 |

아이콘은 공식 브랜드 색상 유지 (이전 구현과 동일).

### 4.3 궤도 라벨 표현

기존 `AI CORE / LANGUAGES / INFRASTRUCTURE` 대신:

```
REASON · OBSERVE · ACT · DEPLOY
```

각 라벨은 궤도 상단에 배치, letter-spacing으로 시각적 리듬 부여.

---

## 5. 기존 대비 개선 효과

| 항목 | 기존 (기술 유형별) | 개선 (Agent 역할별) |
|------|------------------|-------------------|
| 메시지 | "이 기술들을 압니다" | **"Agent를 이렇게 만들고 운영합니다"** |
| 차별화 | 일반 개발자 프로필 | **AI Agent Engineer 고유 시각화** |
| 서사 | 기술 나열 | **Reason→Act→Observe→Deploy 생명주기** |
| 면접 대화 | "기술 스택이 뭔가요?" | **"Agent 시스템을 어떻게 설계하나요?"** |

---

## 6. 기술 재배치 요약

```
변경 전:                          변경 후:
Inner  [LangGraph MCP             Orbit 1 REASON [Gemini LangGraph]
        Gemini LangFuse]
                                  Orbit 2 ACT    [MCP Python TypeScript FastAPI]
Middle [Python TypeScript
        Go FastAPI]               Orbit 3 OBSERVE [LangFuse Prometheus Grafana]

Outer  [K8s Docker Terraform      Orbit 4 DEPLOY [Docker K8s Terraform ArgoCD Go]
        ArgoCD Prometheus
        Grafana]
```

### 이동 항목

| 기술 | 기존 궤도 | 변경 궤도 | 이유 |
|------|----------|----------|------|
| Gemini | Inner (AI Core) | **Orbit 1 (Reason)** | LLM = Agent의 추론 엔진 |
| LangGraph | Inner (AI Core) | **Orbit 1 (Reason)** | 워크플로 계획/오케스트레이션 |
| MCP | Inner (AI Core) | **Orbit 2 (Act)** | Tool Calling = Agent의 실행 수단 |
| LangFuse | Inner (AI Core) | **Orbit 3 (Observe)** | 추적 = 관측 레이어 |
| Prometheus | Outer (Infra) | **Orbit 3 (Observe)** | 메트릭 = 관측 레이어 |
| Grafana | Outer (Infra) | **Orbit 3 (Observe)** | 대시보드 = 관측 레이어 |
| Go | Middle (Languages) | **Orbit 4 (Deploy)** | Monitoring-v3 인프라 도구 언어 |
| Python | Middle (Languages) | **Orbit 2 (Act)** | Agent 실행 런타임 |
| TypeScript | Middle (Languages) | **Orbit 2 (Act)** | MCP 서버 구현 언어 |
| FastAPI | Middle (Languages) | **Orbit 2 (Act)** | Agent API 레이어 |

---

## 7. 구현 시 고려사항

### 7.1 아이템 수 균형

```
Orbit 1 (REASON):  2개 — 작지만 핵심 (가장 빠른 회전으로 존재감)
Orbit 2 (ACT):     4개 — Agent의 핵심 도구
Orbit 3 (OBSERVE): 3개 — 관측 스택
Orbit 4 (DEPLOY):  5개 — 인프라 (가장 넓은 궤도)
총 14개 유지
```

### 7.2 궤도 반경 조정

4개 궤도로 변경되므로 반경 재계산 필요:

```
Orbit 1 (REASON):  rx=85,  ry=34  — 중심에 가깝게
Orbit 2 (ACT):     rx=155, ry=63  — 중간
Orbit 3 (OBSERVE): rx=225, ry=92  — 중간-외곽
Orbit 4 (DEPLOY):  rx=310, ry=128 — 최외곽
```

### 7.3 SVG viewBox

4궤도로 늘어나면 세로 공간 필요 증가:
- 현재: 800x420
- 권장: 800x460 (세로 여유 확보)
