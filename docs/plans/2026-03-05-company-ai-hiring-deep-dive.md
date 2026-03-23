# 주요 기업 AI-Agent/LLM 채용 심층 분석

**작성일:** 2026년 3월 5일
**목적:** GitHub 프로필 타겟 기업 선정을 위한 기업별 AI 채용 현황 심층 분석
**조사 방법:** 3개 독립 서브에이전트 병렬 리서치 후 통합

---

## 목차

1. [토스 (Viva Republica) 그룹](#1-토스-viva-republica-그룹)
2. [삼성전자 / 삼성리서치](#2-삼성전자--삼성리서치)
3. [LG전자 / LG AI연구원](#3-lg전자--lg-ai연구원)
4. [현대차그룹](#4-현대차그룹)
5. [카카오그룹](#5-카카오그룹)
6. [네이버 / 네이버클라우드](#6-네이버--네이버클라우드)
7. [SK텔레콤](#7-sk텔레콤)
8. [KT](#8-kt)
9. [전체 기업 연봉 비교](#9-전체-기업-연봉-비교)
10. [GitHub 프로필 타겟 기업 전략](#10-github-프로필-타겟-기업-전략)

---

## 1. 토스 (Viva Republica) 그룹

### AI 채용공고 현황

| 회사 | 직무명 | 경력 | 핵심 기술스택 |
|------|--------|------|--------------|
| 토스 본사 | ML Engineer (LLM Model) | 경력 | LLM fine-tuning, RAG, LLMOps, H100 GPU 클러스터 |
| 토스 본사 | ML Engineer (추천) | 경력 | PyTorch, Feature Store, Kubernetes |
| 토스 본사 | ML Engineer (MLOps) | 경력 | Kubeflow, Airflow, Triton, MLFlow |
| 토스 본사 | Ads ML Engineer | **신입** | CTR/CVR 예측, 딥러닝, 광고 최적화 |
| 토스뱅크 | ML Engineer (General) | 경력 | Vector DB, LLM 서빙, Feature Store |
| 토스뱅크 | ML Engineer (Product) | 경력 | LLM, 챗봇, OCR, AI 업무자동화 |
| 토스뱅크 | MLOps Engineer | 경력 | MLFlow, Kubeflow, ScyllaDB, Triton, LLMOps |
| 토스증권 | ML Engineer (LLM/Platform) | 경력 | Triton, H100 GPU 클러스터, ONNX, LLMOps |

**채용 페이지:** [toss.im/career/jobs](https://toss.im/career/jobs)

### AI 팀 조직 구조

```
데이터 Division
├── Silo (제품팀 단위)
│   ├── 토스증권 AI Silo — 투자 정보 개인화, LLM 요약/번역
│   ├── Ads Silo — CTR/CVR 예측, 광고 최적화
│   └── Commerce Silo — 커머스 추천·타겟팅
├── DA Chapter / DS+MLE Chapter
├── Data Platform Team (TUBA — 사내 A/B 테스트 플랫폼)
├── ML Platform Team (Feature Store, LLM 플랫폼, 모니터링)
└── AI 에반젤리스트 (10여명, 본업 병행 AI 문화 확산)
```

### 내부 AI 기술스택

| 분류 | 기술 |
|------|------|
| ML 프레임워크 | PyTorch, TensorFlow |
| 모델 서빙 | Triton Inference Server, BentoML, torchserve, ONNX |
| ML 플랫폼 | Kubeflow, MLFlow, Airflow, Argo Workflow/CD, Jupyterhub |
| Feature Store | ScyllaDB (Cassandra 계열), Vector DB |
| GPU 인프라 | **H100 기반 고성능 GPU 클러스터** |
| 컨테이너 | Kubernetes (K8s) |
| 데이터 | Apache Spark, Kafka, Hadoop, Kudu, Elasticsearch |
| LLM 전략 | 자체 사전학습 없이 오픈소스 LLM fine-tuning |
| 외부 LLM | ChatGPT Enterprise 전사 도입 (2025.07), AWS Bedrock |
| MCP | Spring-AI 기반 Swagger MCP 서버 (토스페이먼츠 PG 업계 최초, 2025.06) |

### 최근 AI 서비스

| 서비스 | 출시 | 내용 |
|--------|------|------|
| **AI어닝콜** | 2025.05 | 해외 기업 어닝콜 실시간 번역 (4만 건 학습 자체 금융 특화 모델), 누적 120만 명 |
| **AI시그널** | 2025.11 | 실시간 시장 분석 + 주가 변동 원인 추론 (국내 증권사 최초 인지형 AI) |
| **AI 에이전트 금융상담** | 2025.12 | 문맥 기반 LLM + 음성인식 복합 상담 (혁신금융서비스 지정) |
| **AWS Bedrock 업무자동화** | 2025.12 | Code Review, Text-to-SQL, 마케팅·법률 검토 자동화 (혁신금융서비스 4건) |
| **토스페이먼츠 MCP 서버** | 2025.06 | 결제 연동 자연어 처리 (기존 1~2주 → 10분), NPM 배포 |

### 채용 전형

```
서류 → 코딩테스트(LeetCode Medium 수준 2문제) → 직무 인터뷰 1차(1h)
→ 직무 인터뷰 2차(기술면접 1h + ML 시스템설계 1h) → 컬처핏 → 레퍼런스 체크 → 처우협의
```

**특이사항**: 전 직장 연봉 최대 1.5배 적용 (블라인드 후기), 2~3주 내 합격 통보

### 연봉 및 처우

| 구분 | 범위 |
|------|------|
| 신입 | 5,500 ~ 6,500만 원 |
| 주니어 3~5년 | 7,000 ~ 9,000만 원 |
| 미드레벨 5~8년 | 9,000만 ~ 1억 2,000만 원 |
| 시니어 8년+ | 1억 3,000만 원+ |
| 전체 평균 | 약 1억 2,600만 원 (캐치 기준) |

복지: 유연근무제, 만 3년 리프레시 유급휴가 1개월, 점심·저녁 식사 제공

---

## 2. 삼성전자 / 삼성리서치

### 조직 구조

| 조직 | 역할 |
|------|------|
| **삼성리서치** | DX 사업부 산하 유일한 선행 연구소, 전 세계 15개 연구소 + 4개 글로벌 AI센터, 임직원 1만여 명 |
| **MX사업부 Language AI팀** | 갤럭시 AI (온디바이스 AI 개발 주도, 갤럭시 S25 개인화 에이전트) |
| **DS부문 AI센터** | 반도체 설계·공정 자동화 AI |

### AI 전략

- **삼성 가우스(Gauss)**: Gauss 2.3, Gauss 2.3 Think, Gauss O Flash 라인업
- **에이전트 빌더(Agent Builder)**: 가우스 기반 노코드 사내 에이전트 제작 플랫폼
- **갤럭시 AI / One UI 7**: 갤럭시 S25 개인화 AI 에이전트 탑재, 2025년 말 4억 대 목표
- **전략 전환(2025.02)**: 이재용 회장 지시로 외부 AI(Google Gemini 등) 적극 도입 — 폐쇄형 → 개방형

### 채용 포지션

| 포지션 | 조직 | 경력 요건 | 기술스택 |
|--------|------|-----------|---------|
| AI/NLP 연구원 (Talent Pool) | 삼성리서치 | 석사 이상 (박사 우대) | LLM Pre/Post-training, Transformer, PyTorch |
| On-Device AI 엔지니어 | MX사업부 | 3년 이상 | LLM 경량화, NPU 최적화, On-Device inference |
| AI 에이전트 개발 | 삼성리서치 | 5년 이상 | 에이전트 빌더, 가우스 LLM, 노코드 플랫폼 |

**채용 방식**: 공개 JD 보다 **상시 Talent Pool 등록** 방식 주로 활용, 챌린지 연계 채용 병행

### 연봉

| 구분 | 수치 |
|------|------|
| 신입 초봉 | 약 5,300만 원 |
| 전체 평균 | 약 1억 3,011만 원 |
| 삼성리서치 아메리카 (SRA) | 2억 5,700만 ~ 3억 5,900만 원 |
| 박사급 AI 연구원 글로벌 초봉 | 약 3억 8,000만 원 |

---

## 3. LG전자 / LG AI연구원

### 조직 구조

LG AI연구원 (2020년 설립, 약 300명) — LG경영개발원 산하
- 본원: 서울 마곡 LG Science Park
- 글로벌 AI센터: 미국 앤아버(Ann Arbor), CSAI 이홍락 주도

| 랩 | 연구 분야 |
|----|---------|
| EXAONE Lab | LLM Pre/Post-training, Agent 특화 모델 |
| Language Intelligence Lab | STT/TTS, 대화 AI |
| Computer Vision Lab | ViT, Diffusion, 멀티모달 |
| Materials Intelligence Lab | 소재 AI |
| Robotics Lab | Embodied AI, Robot LLM |

### EXAONE 모델 현황

| 모델 | 출시 | 특징 |
|------|------|------|
| EXAONE 3.0 | 2024.08 | 오픈소스 공개 (arXiv:2408.03541) |
| EXAONE 3.5 | 2024.12 | 2.4B/7.8B/32B 3종 오픈소스, 코딩·수학 강화 |
| EXAONE Deep | 2025.03 | DeepSeek-R1 수준 추론 모델 (arXiv:2503.12524) |
| **EXAONE 4.0** | 출시 예정 | **128K 컨텍스트, MCP+Function Calling 지원, Agent 특화** |

### 채용 포지션

| 포지션 | 경력/학력 | 핵심 기술 | 우대사항 |
|--------|-----------|---------|---------|
| Research Scientist (EXAONE Lab) | 신입/경력, 석사 이상 | LLM Pre-training, Post-training, LMM | 10B+ LLM 학습 경험, NeurIPS/ICML/ACL 1저자 |
| Research Scientist (Global AI Center) | 경력, 석사 이상 | 최신 LLM 아키텍처, 멀티모달 | 해외 탑스쿨 박사 우대 |
| Research Scientist (Robotics) | 박사 또는 경력 2년+ | Robot LLM, Embodied AI | 논문 실적 |
| Summer Internship (EXAONE Lab) | 해외대 석/박사 재학 | LLM Research | 항공권 지원, 2025.6~8 |

**채용 절차**: 서류 → 코딩테스트+포트폴리오 → 1차 직무 인터뷰 → AI Fit Check → 최종 인터뷰(온사이트)

### 연봉

| 구분 | 수치 |
|------|------|
| 신입 초봉 | 약 5,300만 원 (LG그룹 기준) |
| LG전자 평균 | 약 1억 1,700만 원 |

---

## 4. 현대차그룹

### 조직 구조

| 조직 | 역할 |
|------|------|
| **현대오토에버 인공지능기술실** | 전사 AI 기술 리드, AI Agent 플랫폼, 업무자동화 |
| **포티투닷(42dot)** | 자율주행 AI(Atria AI) + 차량 Agentic AI(Gleo AI) + 자체 LLM |
| **현대차 AIR Lab** | 음성UX, NLP, 컴퓨터비전, 데이터 엔지니어링 |
| **현대모비스 전장사업부** | On-Device LLM, 차량 AI 시스템 통합 |

### 채용 포지션 (상세)

**현대오토에버**

| 포지션 | 경력 | 핵심 요건 |
|--------|------|---------|
| AI Agent 엔지니어 | 5년 이상 | Agent Orchestration, LangChain/LangGraph/CrewAI, MLOps 파이프라인 연계 |
| AI Tech PM/PL | 5년 이상 | AI 프로젝트 기술 기획 및 리드 |

**현대오토에버 AI Agent 엔지니어 우대사항 (핵심)**:
- **A2A(Agent-to-Agent) + MCP(Model Context Protocol) 프로토콜 활용 에이전트 개발 경험**
- 지식그래프(Knowledge Graph), 온톨로지 개발 경험
- 클라우드(AWS/Azure/GCP) AI/ML 서비스 개발 및 배포 경험

**포티투닷(42dot)**

| 포지션 | 유형 | 대상 |
|--------|------|------|
| LLM AI 에이전트 엔지니어 | 채용연계 인턴 | 학사 이상 (차량용 Agentic AI) |
| LLM AI 모델 엔지니어 | 채용연계 인턴 | 학사 이상 (Atria AI/Gleo AI) |
| LLM Research Intern | 상시 인턴 | 석사 2학차 이상 |

자체 LLM 개발 중 (현대차·기아 SDV 차량 탑재 예정, AI 챗봇 'Baker' 기반)

**현대모비스**

| 포지션 | 핵심 기술 | 입사 |
|--------|---------|------|
| 자율주행로직 생성형AI/딥러닝 | **On-Device LLM, LLM 소형화·최적화** | 2026년 상반기 |
| 생성형 AI서비스 연구/개발 | LLM, RAG, 멀티모달 AI | 2026년 4월 |

### 현대차그룹 AI 전략

**SDV(Software-Defined Vehicle) 전환이 핵심 드라이버**:
- 현대오토에버: 전사 AI 자동화 + MCP/A2A 기반 에이전트 플랫폼
- 포티투닷: Atria AI(자율주행) + Gleo AI(차량 Agentic AI) 동시 개발
- 현대모비스: On-Device LLM → 차량 ECU 통합

### 연봉

| 기업 | 평균 연봉 | 초봉 |
|------|---------|------|
| 현대오토에버 | 약 1억 364만 원 | 약 5,113만 원 |
| 포티투닷(42dot) | 비공개 | 비공개 |

---

## 5. 카카오그룹

### 조직 개편 (2024년)

카카오브레인 → 2024.10 디케이테크인 흡수합병으로 법인 소멸
AI 핵심 연구 → **카나나(Kanana)** 조직으로 통합 (2024.06 신설)
- 카나나 알파: R&D 담당
- 씨엑스알랩(CXR Lab): 헬스케어 AI 분사

### 카나나(Kanana) 모델 현황

| 모델 | 출시 | 특징 |
|------|------|------|
| Kanana-1.5-8b | 2025.05 | 8B 이하 한국어 리더보드 1위, Apache 2.0 |
| Kanana-1.5-15.7b-a3b (MoE) | 2025.07 | **국내 최초 오픈소스 MoE 모델** |
| **Kanana-2** | 2025.12 | **Tool Calling 3배 향상, 에이전틱 AI 특화** |
| Kanana-2-155b-a17b | 개발 중 | 수천억 파라미터 초거대 모델 |

기술: MLA(Multi-head Latent Attention) + MoE 아키텍처, 8비트 학습, 6개 언어(한/영/일/중/태/베)

### 계열사별 AI 채용

| 계열사 | 직무명 | 경력 | 핵심 기술스택 |
|--------|--------|------|--------------|
| **카카오 (카나나 알파)** | LLM 개발자 | 2년+ | PyTorch, 에이전트 시스템, NLP |
| **카카오** | ML Engineer (LLM/Search) | 3~10년 | LLM, RAG, 검색 시스템 |
| **카카오** | MLOps Engineer | 경력 | Kubernetes, LLM DevOps, CI/CD |
| **카카오페이** | AI 엔지니어 (AI 플랫폼) | **5년+** | LLM, RAG, VectorDB, Elasticsearch, Embedding, **Agent** |
| **카카오그룹 전체** | AI 네이티브 신입 공채 | **신입** (2026.01 입사) | 전 직군 (테크/서비스/비즈/디자인) |

**카카오 JD 특이 문구**: *"LangGraph, LangChain 등 단순 오픈소스 사용자는 제외"* — 내부 구조 이해 및 커스터마이징 능력 필수

### 2025 그룹 단위 신입 공채 (창사 이래 최초)

- 참여 계열사: 카카오, 카카오게임즈, 카카오모빌리티, 카카오뱅크, 카카오엔터테인먼트, 카카오페이
- 키워드: 'AI 네이티브' — 정규돈 CTO "연차보다 AI 활용 역량이 핵심"

### 연봉

| 계열사 | 평균 연봉 |
|--------|---------|
| 카카오 본사 | 약 1억 200만 원 (남성 1억 1,400만 원) |
| 카카오뱅크 | 약 1억 706만 원 |
| 카카오페이 | 약 8,800만 원 (초봉 5,309만 원) |

---

## 6. 네이버 / 네이버클라우드

### 조직 구조

| 조직 | 역할 |
|------|------|
| **NAVER Corp.** | 서치 플랫폼 및 AI 연구 총괄 |
| **네이버클라우드** | HyperCLOVA X 개발 주체, AI Agent 서비스 운영 |
| **NAVER LABS** | 로봇, 자율주행, Vision AI |
| **CLOVA Studio** | 기업용 AI 개발 플랫폼 (SFT/RLHF/Function Calling 제공) |

### HyperCLOVA X 기술 스택

| 항목 | 상세 |
|------|------|
| 아키텍처 | Transformer Decoder + **RoPE + GQA(Grouped-Query Attention)** + Flash Attention |
| 학습 | bf16 + 3D Parallelism (텐서/파이프라인/데이터 병렬화) |
| 정렬 기법 | SFT → RLHF (PPO 기반, Bradley-Terry 랭킹 손실) |
| THINK (추론 특화) | 140B 파라미터, 오픈소스 공개, 한국어 추론 1위 (2025.06) |
| Agent | **MCP 기반 멀티에이전트, Tool Calling/Handoff** |

### 채용 포지션

| 직무명 | 경력 | 핵심 기술 |
|--------|------|---------|
| AI Agent 개발 엔지니어 | 3년+ | Python/Java/Kotlin/Golang, Kubernetes, Docker, 대화형 AI |
| HyperCLOVA X 학습 시스템 | 3년+ | PyTorch, HuggingFace, GPU 분산학습, LLM 학습 최적화 |
| HyperCLOVA X Post-training | 연구 경험자 | RLHF, Alignment, Reasoning, Function Calling |
| Foundation Model 연구자 | 석박사 우대 | IR/NLP/Vision, TensorFlow/PyTorch |

**AI Agent 개발 엔지니어 우대**: HyperCLOVA X 기반 대화형 서비스 개발, AI 학술 논문 보유

### 연봉

| 구분 | 수치 |
|------|------|
| 네이버 본사 평균 | 약 1억 2,900만 원 (2024년 사업보고서) |
| 개발직군 초봉 | 약 7,000만 원 |
| 성과급 | 최대 연봉 50%, 평균 약 20% |
| 개인업무지원금 | 연 360만 원 |
| 근무제 | Connected Work (출퇴근 자율) |

---

## 7. SK텔레콤

### A.X 조직 구조 (2025년 7대 사업부)

| 사업부 | 역할 |
|--------|------|
| 에이닷사업부 | A.(에이닷) 개인 AI 비서 |
| GPAA사업부 | 글로벌 AI 에이전트 서비스 |
| AIX사업부 | B2B AI 전환 (A.Biz) |
| AI DC사업부 | AI 인프라/클라우드 |

NUGU → 에이닷 완전 통합 / SK C&C → **SK AX** 사명 변경 (에이전틱 AI 스택 구축 집중)

### A.X K1 (독자 LLM)

| 항목 | 내용 |
|------|------|
| 파라미터 | **5,190억 개 (519B)**, 추론 시 활성화 약 330억 (MoE 구조) |
| 발표 | 2025.12 과기정통부 '독자 AI 파운데이션 모델(독파모)' 1차 발표회 |
| 개발 연합 | SKT + 크래프톤 + 42dot + 리벨리온 + 라이너 + 셀렉트스타 + 서울대 + KAIST |
| 향후 | 1조 파라미터급 진화 예정, 오픈소스 공개 예정 |

### 채용 포지션

| 직무명 | 대상 | 핵심 요건 |
|--------|------|---------|
| 대형 Foundation Model 개발자 | 석/박사 | 100B+ LLM/MLLM, GPU 분산학습, CUDA, ML 학회 논문 |
| 대화형 언어모델 개발자 | 석/박사 | Alignment Tuning (RLHF/RLAIF), 도메인 특화 대화 모델 |
| AI R&D Junior Talent | 석사 신입 (25~26년 2월 졸업) | Agentic AI, 제조/바이오 특화 VLM, ML 학회 논문 |
| A.X K1 인턴 | 석박사/우수 학부생 | 초거대 모델 개발 참여 (3개월, 선착순) |

**신입 채용 전형**: 지원(자소서 없음) → SKCT 심층 + 코딩테스트 → 서류(필기 합격자) → 1차·2차 면접

### 연봉

| 구분 | 수치 |
|------|------|
| 전체 평균 | 약 1억 4,400만 원 (업계 최상위) |
| AI 인력 비중 | 전체 인원의 약 40% |

---

## 8. KT

### AI 전략 및 조직

- **'AICT 컴퍼니'** 선언, AI 인재 전담 조직 '테크 리크루팅 센터' 신설
- MS(Microsoft)와 소버린 AI 개발 파트너십
- 믿음(midm) LLM → **sLLM(경량화) 방향으로 전환**, B2B/B2G 시장 집중

### 믿음(midm) LLM 현황

| 모델 | 파라미터 | 특징 |
|------|----------|------|
| 믿음 K 2.0 Mini | 2.3B | 온디바이스 최적화, HuggingFace 오픈소스 (MIT 라이선스) |
| **믿음 K 2.0 Base** | **11.5B** | **국내 독자 모델 중소형 1위**, 상업적 활용 무제한 |

- 국내 첫 '인공지능 신뢰성 인증' 획득
- 경기도 생성형 AI 플랫폼, 대법원 재판업무 지원 AI 활용 중

### 채용 포지션

| 직무명 | 채용 유형 | 핵심 업무 |
|--------|-----------|---------|
| **AI Agent 개발** | **신입/석사 공채 + AICT 우수인재** | Agentic AI, 생성형 AI 기반 에이전트 |
| **AI Agent Backend 개발** | 신입/석사 공채 | 에이전트 백엔드 시스템 |
| Gen AI/APP 선행연구 | 신입/석사 공채 | 생성형 AI 응용 선행연구 |
| 모델 경량화·추론 최적화 | 신입/석사 공채 | sLLM, 온디바이스 AI 최적화 |
| LLM기반 언어/대화 기술개발 | 경력 R&D | AICC, NLU, 감성분석 |
| LLM 고속 추론 기술개발 | 경력 석사 R&D | Triton/TensorRT-LLM/FastTransformer 서빙 |
| SI AI Agent Developer | AICT 우수인재 | 생성형 AI 기반 B2B/B2G SI 프로젝트 |

**LLM 개발 우대사항**: RAG/LLMOps, Triton/TensorRT-LLM, AI 탑티어 논문, sLLM 기반 대화/QA/검색 프로젝트

### 파격적 처우 개편 (2025년)

- IT 독립 직군 신설 (직급 단순화: 책임/선임/전임 3단계)
- **'책임' 직급 연봉 상한(페이 밴드) 폐지** → 20대 개발자도 억대 연봉 가능
- **석사 신입 입사 시 경력 2년 처우 인정**
- AI 인재 1,000명 확보 목표 (2024년), 2025년도 세 자릿수 규모 AX 인력 채용 지속

### 연봉

| 구분 | 수치 |
|------|------|
| 전체 평균 | 약 1억 1,000만 원 |
| AI 직군 | 연봉 상한 폐지, 역량에 따라 억대 가능 |

---

## 9. 전체 기업 연봉 비교

| 기업 | 전체 평균 연봉 | AI 개발자 초봉 (추정) | 특이 처우 |
|------|-------------|-------------------|---------|
| SK텔레콤 | **약 1억 4,400만 원** | 대기업 상위권 | AI 인력 40%, 석/박사 우대 |
| 네이버 본사 | 약 1억 2,900만 원 | 약 7,000만 원 | 성과급 최대 50%, Connected Work |
| 삼성전자 | 약 1억 3,011만 원 | 약 5,300만 원 | 글로벌 AI센터 처우 별도 |
| 토스 | 약 1억 2,600만 원 | 5,500 ~ 6,500만 원 | 이직 시 최대 1.5배 |
| 카카오뱅크 | 약 1억 706만 원 | — | 복지카드 500만원/년 |
| 카카오 본사 | 약 1억 200만 원 | 약 6,000만 원대 | 성과 기반 |
| 현대오토에버 | 약 1억 364만 원 | 약 5,113만 원 | 차량 AI 도메인 |
| KT | 약 1억 1,000만 원 | 석사 신입 경력 2년 인정 | **AI 직군 연봉 상한 폐지** |
| LG전자 | 약 1억 1,700만 원 | 약 5,300만 원 | 포괄임금제 |
| 카카오페이 | 약 8,800만 원 | 약 5,309만 원 | 유연근무 |
| 네이버클라우드 | 약 6,259만 원 | 약 4,574만 원 | Connected Work |

---

## 10. GitHub 프로필 타겟 기업 전략

### DevOps 백그라운드 보유자 기준 접근성 분류

| 접근 난이도 | 기업 | 이유 |
|-----------|------|------|
| **높음** (즉시 지원 가능) | 현대오토에버, KT, LG CNS | MCP/A2A/인프라 경험 직접 활용 가능 |
| **중간** (6~12개월 준비) | 토스, 카카오페이, 업스테이지, 뤼튼 | LangChain/RAG 프로젝트 추가 필요 |
| **낮음** (연구 역량 필요) | 삼성리서치, LG AI연구원, SKT, 네이버 | 석박사·탑티어 논문 사실상 필요 |

### 현대오토에버 지원 시 GitHub 어필 포인트

현재 DevOps/K8s 경험 → AI Agent 전환 시 **가장 유리한 포지션**:
- MCP 프로토콜 기반 툴 연동 프로젝트 (직접 우대사항 충족)
- A2A 아키텍처 구현 예시 코드
- Kubernetes 기반 LLM API 서버 배포 (기존 인프라 역량 + AI 결합)

### 토스 지원 시 GitHub 어필 포인트

- LLMOps 파이프라인 (MLFlow + Kubeflow 연동)
- 금융 도메인 RAG 시스템 (토스증권 AI Silo 방향)
- FastAPI + Triton Inference Server LLM 서빙 구현

### 카카오 지원 시 주의사항

JD 명시 경고: *"단순 오픈소스 사용자 제외"*
- LangGraph 소스코드 분석 블로그 포스팅
- LangChain 커스텀 노드 구현 (기본 API 사용 넘어서기)
- LLM 파인튜닝 실험 과정을 W&B로 시각화한 레포지토리

---

## 출처 요약

| 기업군 | 주요 출처 |
|--------|---------|
| 토스 | [toss.tech](https://toss.tech/), [toss.im/career](https://toss.im/career/jobs), [토스페이먼츠 MCP](https://toss.tech/article/tosspayments-mcp) |
| 삼성 | [samsungcareers.com](https://www.samsungcareers.com/), [Samsung Newsroom](https://news.samsung.com/kr/) |
| LG AI연구원 | [lgresearch.ai](https://www.lgresearch.ai/), [lgresearch.ai/careers](https://www.lgresearch.ai/careers) |
| 현대차그룹 | [career.hyundai-autoever.com](https://career.hyundai-autoever.com), [42dot.ai/careers](https://42dot.ai/careers/openroles) |
| 카카오 | [careers.kakao.com](https://careers.kakao.com/jobs), [kakaocorp.com](https://www.kakaocorp.com/) |
| 네이버 | [recruit.navercorp.com](https://recruit.navercorp.com/), [HyperCLOVA X 논문](https://arxiv.org/pdf/2404.01954) |
| SKT | [careers.sktelecom.com](https://careers.sktelecom.com/), [A.X K1 발표](https://news.sktelecom.com/217811) |
| KT | [recruit.kt.com](https://recruit.kt.com/), [믿음 K 2.0](https://enterprise.kt.com/pd/P_PD_NE_00_316.do) |
