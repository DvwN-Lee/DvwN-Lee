# Tech Stack 물체화 시각화 분석

**작성일**: 2026-03-23
**목적**: 14개 기술 스택을 물체로 시각화하여 AI Agent 동작 원리를 보여주는 방안 도출

---

## 1. 물체화 메타포 Top 3

### 1위: 연금술 실험실 (Alchemist's Laboratory)

**선정 이유**: 브라운 팔레트(`#0D0805`+`#D4A574`)가 연금술의 구리/금/갈색 톤과 완벽 일치. GitHub 프로필에서 전례 없는 독창성. "원소를 분석하고, 도구로 연성하고, 결과를 관측하고, 완성품을 생산한다"는 서사가 AI Agent REASON→ACT→OBSERVE→DEPLOY 사이클과 1:1 대응.

| 사이클 | 연금술 역할 | 기술 | 물체 | SVG 형태 |
|--------|-----------|------|------|---------|
| REASON | 원소 분석 | Gemini | 현자의 돌 (Philosopher's Stone) | 회전하는 다각형+글로우 |
| REASON | 연성 설계 | LangGraph | 연성진 (Transmutation Circle) | 중첩된 원+기호 |
| ACT | 도구 프로토콜 | MCP | 도가니 (Crucible) | 삼각형 컵+내부 빛 |
| ACT | 주요 용매 | Python | 삼각 플라스크 (Flask) | 삼각형+액체 수위 animate |
| ACT | 보조 용매 | TypeScript | 비커 (Beaker) | 직사각+눈금선 |
| ACT | 증류/추출 | FastAPI | 증류기 (Alembic) | 곡선 관+용기 |
| OBSERVE | 결과 추적 | LangFuse | 수정구슬 (Crystal Ball) | 원형+반사 하이라이트 |
| OBSERVE | 열량 측정 | Prometheus | 영원의 불꽃 (Eternal Flame) | 불꽃+흔들림 |
| OBSERVE | 성분 분석 | Grafana | 마법 거울 (Scrying Mirror) | 타원형+프레임 |
| DEPLOY | 포장/밀봉 | Docker | 밀봉 약병 (Sealed Vial) | 원통+코르크 |
| DEPLOY | 대량 생산 | Kubernetes | 원소 주기율표 (Periodic Table) | 육각형 격자 |
| DEPLOY | 제조 공정 | Terraform | 룬 석판 (Rune Tablet) | 직사각+문양 |
| DEPLOY | 자동 배포 | ArgoCD | 마법 깃펜 (Enchanted Quill) | 깃털펜+잉크 흐름 |
| DEPLOY | 도구 제작 | Go | 연금술 망치 (Alchemist's Hammer) | 작은 망치 실루엣 |

**평가**: 시각적 임팩트 5/5, AI Agent 적합성 4/5, 전문성 유지 3/5, 독창성 5/5, 브라운 궁합 5/5

---

### 2위: 시계 기어 (Clockwork Mechanism)

**선정 이유**: "정밀 엔지니어링" 이미지. 기어의 물리적 맞물림이 기술 간 의존 관계를 직관적으로 표현. `<animateTransform type="rotate">`로 연쇄 회전 구현 가능. 빈티지 시계 심미성이 브라운/골드 테마와 부합.

| 사이클 | 시계 역할 | 기술 | 물체 | SVG 형태 |
|--------|---------|------|------|---------|
| REASON | 동력원 | Gemini | 메인 스프링 (Mainspring) | 나선형+펄스 |
| REASON | 조속기 | LangGraph | 이스케이프먼트 (Escapement) | 앵커+작은 기어 |
| ACT | 동력 전달 | MCP | 크라운 휠 (Crown Wheel) | 톱니 원형 회전 |
| ACT | 주 동력 | Python | 대형 기어 (Main Gear) | 큰 톱니바퀴, 느린 회전 |
| ACT | 변속 | TypeScript | 중형 기어 (Second Wheel) | 중간 톱니바퀴 |
| ACT | 출력 | FastAPI | 소형 기어 (Pinion) | 작은 톱니바퀴, 빠른 회전 |
| OBSERVE | 표시 | LangFuse | 문자판 (Clock Face) | 원형+숫자 |
| OBSERVE | 박자 | Prometheus | 진자 (Pendulum) | 좌우 진동 |
| OBSERVE | 지시 | Grafana | 시침/분침 (Hands) | 바늘 회전 |
| DEPLOY | 보호 | Docker | 케이스 (Watch Case) | 외곽 원형 |
| DEPLOY | 축 시스템 | Kubernetes | 기어 트레인 (Gear Train) | 연결된 기어들 |
| DEPLOY | 고정 | Terraform | 중심축 (Arbor) | 수직 원통 |
| DEPLOY | 자동감김 | ArgoCD | 자동 감김장치 (Auto-winder) | 회전 로터 |
| DEPLOY | 마찰 감소 | Go | 보석 베어링 (Jewel Bearing) | 빨간 작은 원 |

**평가**: 시각적 임팩트 5/5, AI Agent 적합성 4/5, 전문성 유지 5/5, 독창성 4/5, 브라운 궁합 4/5

---

### 3위: 회로 기판 (Circuit Board / PCB)

**선정 이유**: 가장 직관적인 "엔지니어" 이미지. PCB 트레이스(배선)가 데이터 흐름을 자연스럽게 표현. 다크 브라운 기판 + 카라멜 트레이스 조합이 실제 PCB와 유사.

| 사이클 | 회로 역할 | 기술 | 물체 | SVG 형태 |
|--------|---------|------|------|---------|
| REASON | 연산 | Gemini | CPU | 정사각+핀 |
| REASON | 가속 | LangGraph | GPU | 큰 직사각 칩 |
| ACT | 인터페이스 | MCP | I/O 컨트롤러 | 직사각+다중 포트 |
| ACT | 런타임 | Python | RAM 모듈 | 긴 직사각 |
| ACT | 펌웨어 | TypeScript | EEPROM | 작은 칩 |
| ACT | 통신 | FastAPI | 버스 브리지 | 연결 허브 |
| OBSERVE | 상태 표시 | LangFuse | LED 어레이 | 깜빡이는 원형들 |
| OBSERVE | 센싱 | Prometheus | 센서 IC | 작은 정사각 |
| OBSERVE | 출력 | Grafana | LCD 모듈 | 직사각 스크린 |
| DEPLOY | 격리 | Docker | CPU 소켓 | 핀홀 격자 |
| DEPLOY | 전력 분배 | Kubernetes | VRM 모듈 | 인덕터+캐패시터 |
| DEPLOY | 구성 | Terraform | 점퍼/딥스위치 | 핀 쌍 |
| DEPLOY | 펌웨어 플래시 | ArgoCD | BIOS 칩 | 라벨 칩 |
| DEPLOY | 연결 | Go | PCB 트레이스 | 직각 라인+전류 흐름 |

**평가**: 시각적 임팩트 4/5, AI Agent 적합성 4/5, 전문성 유지 5/5, 독창성 3/5, 브라운 궁합 3/5

---

## 2. 유기적 연결 레이아웃 Top 3

### 1위: 카드 그리드 + 연결선 (현재 agent-flow.svg 패턴)

```
[REASON] ──→ [ACT] ──→ [OBSERVE]
   ↑                        │
   └────── AGENT LOOP ──────┘
         ══════════════
            [DEPLOY]
```

- 정보 전달력 최고 (9/10)
- DEPLOY가 하단 바로 "기반" 의미 명확
- 공간 효율 85%

### 2위: 순환 다이어그램 (삼각 사이클)

```
         REASON
        /      \
    OBSERVE    ACT
        \      /
         DEPLOY
```

- R→A→O 사이클 표현 최강 (9/10)
- 세 그룹이 대등하게 배치
- 공간 효율 70%

### 3위: 궤도형 Globe (현재 techstack-globe.svg)

- 시각적 임팩트 최고 (10/10)
- 궤도 공전 애니메이션이 "살아있는 시스템" 전달
- 정보 전달력 약함 (5/10)

---

## 3. SVG 기법 가이드

### 사용 가능한 기법 (GitHub 동작 확인)

| 기법 | 태그 | 효과 |
|------|------|------|
| 속성 애니메이션 | `<animate>` | opacity, fill, stroke-dashoffset, r, cx, cy 변화 |
| 변환 애니메이션 | `<animateTransform>` | rotate, scale, translate |
| 경로 이동 | `<animateMotion>` | SVG path 따라 요소 이동 |
| 상태 변경 | `<set>` | 시점별 속성 즉시 변경 |
| 글로우/블러 | `<filter>` + `feGaussianBlur` | 발광 효과 |
| 그라디언트 | `<linearGradient>`, `<radialGradient>` | 색상 전환 |
| 클리핑 | `<clipPath>` | 영역 잘라내기 |
| 마스킹 | `<mask>` | 투명도 마스크 |
| 패턴 | `<pattern>` | 반복 배경 (도트 그리드, 격자) |
| 재사용 | `<use>` | 심볼 반복 사용 |

### 핵심 애니메이션 패턴

**데이터 흐름 (dash-offset + dot):**
```xml
<line stroke="#6B4226" stroke-dasharray="6,4">
  <animate attributeName="stroke-dashoffset" from="10" to="0" dur="1s" repeatCount="indefinite"/>
</line>
<circle r="3" fill="#D4A574" filter="url(#glow)">
  <animateMotion dur="2s" repeatCount="indefinite" path="M0,0 L200,0"/>
</circle>
```

**호흡 효과 (breathing):**
```xml
<circle stroke="#6B4226">
  <animate attributeName="stroke-opacity" values="0.7;1;0.7" dur="4s" repeatCount="indefinite"/>
  <animateTransform type="scale" values="1;1.02;1" dur="4s" repeatCount="indefinite" additive="sum"/>
</circle>
```

**파동 효과 (ripple):**
```xml
<circle r="30" fill="none" stroke="#D4A574" opacity="0">
  <animate attributeName="r" values="30;80" dur="3s" repeatCount="indefinite"/>
  <animate attributeName="opacity" values="0.6;0" dur="3s" repeatCount="indefinite"/>
</circle>
```

**자연스러운 루프**: 여러 애니메이션의 `dur`을 서로소(소수)로 설정하면 전체 반복 주기가 매우 길어져 자연스러움. (예: 7s, 11s, 13s → 반복 주기 1001초)

---

## 4. 메타포 x 레이아웃 x 기법 조합 추천

### 조합 A: 연금술 실험실 + 카드 그리드 + 데이터 흐름

```
┌─ 분석실 ─┐    ┌─ 작업대 ─┐    ┌─ 관측대 ─┐
│ 현자의 돌 │───→│ 도가니   │───→│ 수정구슬 │
│ 연성진   │    │ 플라스크 │    │ 불꽃    │
│          │◀───│ 비커    │◀───│ 거울    │
│          │    │ 증류기   │    │         │
└──────────┘    └──────────┘    └─────────┘
═════════════════════════════════════════════
  보관대: 약병 · 주기율표 · 석판 · 깃펜 · 망치
```

- 물체들이 "연금술 과정"으로 연결
- 데이터 흐름 dot이 "에너지/물질 이동"으로 표현
- 가장 정보 전달력이 높으면서도 독창적

### 조합 B: 시계 기어 + 원형 레이아웃 + 회전 애니메이션

```
         ┌─ 문자판 ─┐
   ┌─────┤  시침분침  ├─────┐
   │진자  │  진자     │ 센서│
   │      └────┬─────┘     │
   │     ┌─────┤─────┐     │
 스프링──┤ Main │ Sub │──크라운
   │     │ Gear │ Gear│     │
   │     └─────┴─────┘     │
   └──────── 케이스 ────────┘
        기어트레인 · 축 · 로터
```

- 기어 맞물림으로 기술 의존성 표현
- `<animateTransform type="rotate">`로 연쇄 회전
- 시각적 임팩트와 전문성 모두 높음

### 조합 C: 회로 기판 + 카드 그리드 + 전류 흐름

```
┌──── PCB Board ────────────────────┐
│  ┌──CPU──┐  ─trace─  ┌──I/O──┐   │
│  │Gemini │ ═══════→ │ MCP   │   │
│  │LGraph │  RAM Py   │ TS    │   │
│  └───────┘  EEPROM   │FastAPI│   │
│      │      BusBr    └───────┘   │
│  ┌──LED──┐                       │
│  │LangF  │  ──trace──  VRM      │
│  │Sensor │  Socket Jumper BIOS  │
│  │LCD    │                      │
│  └───────┘                      │
└──────────────────────────────────┘
```

- PCB 트레이스를 따라 전류(데이터) 흐름 애니메이션
- 가장 공학적이고 전문적

---

## 5. 최종 권고

| 순위 | 조합 | 독창성 | 전문성 | 구현 난이도 | 브라운 궁합 |
|:---:|------|:-----:|:-----:|:---------:|:---------:|
| **1** | 연금술 + 카드 그리드 | 5/5 | 3/5 | 중 | 5/5 |
| **2** | 시계 기어 + 원형 | 4/5 | 5/5 | 고 | 4/5 |
| **3** | 회로 기판 + 카드 그리드 | 3/5 | 5/5 | 중 | 3/5 |

**핵심 고려사항**:
- 연금술: 독창성과 브라운 테마 궁합이 압도적이나, 과도하게 판타지적이면 전문성 희석 위험 → 절제된 미니멀 디자인 필수
- 시계 기어: 전문성 이미지 최고이나, 맞물린 기어의 SVG 구현이 가장 복잡
- 회로 기판: 가장 안전하고 직관적이나, 독창성은 상대적으로 낮음

**GitHub 프로필 전례 조사 결과**: 기술 스택을 물체 메타포로 시각화한 GitHub 프로필은 현재까지 사실상 존재하지 않음. 어떤 메타포를 선택하든 높은 독창성이 보장됨.
