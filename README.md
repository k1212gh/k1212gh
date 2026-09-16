<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:2563eb&height=200&section=header&text=김건희%20Kev&fontSize=46&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=AI%20Backend%20%C2%B7%20LLM%20Serving%20%C2%B7%20RAG&descAlignY=58&descSize=18" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=60A5FA&center=true&vCenter=true&width=560&lines=%EC%B8%A1%EC%A0%95%ED%95%98%EA%B8%B0+%EC%A0%84%EC%97%94+%EB%AF%BF%EC%A7%80+%EC%95%8A%EC%8A%B5%EB%8B%88%EB%8B%A4.;Measure+first%2C+then+scale.;Embedded+%E2%86%92+AI+Backend+%26+LLM+Serving" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/AWS-Solutions%20Architect%20Associate-FF9900?style=flat-square&logo=amazonaws&logoColor=white"/>
  <img src="https://img.shields.io/badge/삼성청년SW·AI아카데미-14기%20AI-1428A0?style=flat-square&logo=samsung&logoColor=white"/>
  <img src="https://img.shields.io/badge/한컴%20AI%20아카데미-1기-00A0E9?style=flat-square"/>
</p>

---

### 👋 About
- 임베디드 시스템 전공 → **AI 백엔드 · LLM 서빙 · RAG**로 확장 중
- 모든 설계 결정은 **before / after 수치**로 검증합니다. 실패한 실험도 기록합니다.

### 🛠 Tech Stack
<p>
  <img src="https://skillicons.dev/icons?i=python,java,kotlin,c,cpp&theme=dark" /><br/>
  <img src="https://skillicons.dev/icons?i=fastapi,pytorch,redis,postgres,mongodb&theme=dark" /><br/>
  <img src="https://skillicons.dev/icons?i=docker,aws,prometheus,grafana,linux,githubactions&theme=dark" />
</p>

---

### 🚀 Projects

#### 🗣️ WithY — 실시간 OTT 같이보기 AI 서비스 · `🏆 공통 프로젝트 우수상 1위`
> AI 파트 리더 · [Watch-with-WITHY/WITHY-AI](https://github.com/Watch-with-WITHY/WITHY-AI)

| 지표 | Before | After |
|---|---|---|
| 채팅 AI 통신 평균 지연 (K6, 100 VU) | REST 517ms | **gRPC 356ms (−31%)** |
| 최대 지연 | 1,400ms | **554ms (−60%)** |
| 스포일러/분탕 분류 정확도 (Qwen2.5-3B LoRA, 검증 101건) | 75.2% | **97.0%** |

- 욕설 필터 1차(화이트리스트 우선) 버전이 466건 기준 66%·FN 135건으로 실패 → **Level 1 절대 차단 구조로 재설계**
- AI 서버 장애 시 채팅이 멈추지 않도록 **Fail-Open** 정책 적용

#### 🧠 HAPA — AI 코딩 어시스턴트 (한컴 AI 아카데미)
> 담당: 모델 학습 파이프라인 + vLLM Multi-LoRA 서빙

- DeepSeek-Coder 6.7B · QLoRA로 **태스크별 LoRA 어댑터 4종** 학습, AWS Spot 인스턴스 중단 대비 체크포인트 핸들러
- vLLM Multi-LoRA 서빙 중 **AWQ 양자화 토큰 손상** 디버깅 → 양자화 제거 · tokenizer 모드 조정 · `max_loras` 튜닝
- 서비스 전체 지표(팀): 시맨틱 캐시 히트율 **78%**, 평균 응답 **1.2s**

#### 💸 Billage — P2P 대여 법률·세무 RAG 챗봇 (핀테크 특화 프로젝트)
> 팀장 · AI 리드 · 6인

| 지표 | Before | After |
|---|---|---|
| AI 서버 장애율 (Locust) | 34.4% | **0%** |
| 평균 응답 | 6,223ms | **4,449ms (−28.5%)** |
| 최대 응답 | 16.7s | **9.3s (−44%)** |
| 검색 Hit Rate@3 | 60% (bge-m3 단일) | **85.0%** (BM25 + reranker 하이브리드) |

- 원인: sentence-transformers OpenMP 스레드 ↔ Uvicorn 워커 경합 → 스레드 설정으로 해결
- HyDE는 +2초 지연·환각 위험으로 **검토 후 미채택**
- Redis 시맨틱 캐시 · 4단계 환각 제어 · ChromaDB

#### 🗺️ Wayfare — APK → 화면 전환 지도(Screen Map) 엔진
> 기업연계 프로젝트(6인)에서 담당한 엔진을 개인 레포로 지속 개발 · [k1212gh/wayfare](https://github.com/k1212gh/wayfare)

- 화면 중복 노드 문제를 **3-Level Screen Signature**로 해결
- androguard 인텐트 필터 파싱 버그를 수동 데이터 검증으로 추적해 라이브러리 레벨 원인 확정
- Ablation으로 **"99.3% 압축률"이 오병합 착시**임을 입증 · 유닛 테스트 371개

---

### 📊 Stats
<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=k1212gh&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=k1212gh&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117" />
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com?user=k1212gh&theme=github-dark-blue&hide_border=true" />
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:2563eb,100:0f172a&height=100&section=footer" />
</p>
