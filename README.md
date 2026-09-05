<h1 align="center">김희태 · AI Agent Developer</h1>

<p align="center">
  <a href="https://gimhuitae-portfolio.vercel.app" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white"/>
  </a>
  <a href="https://inkk.online" target="_blank">
    <img src="https://img.shields.io/badge/INKK-4F46E5?style=for-the-badge&logo=vercel&logoColor=white"/>
  </a>
  <a href="mailto:heetae0104@gmail.com">
    <img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/>
  </a>
</p>

<br/>

저는 개발자가 되기 위해 코드를 배운 사람이 아닙니다. 해결하고 싶은 문제가 있어서 개발을 배웠습니다.

사회복지사로 일하며 비효율을 개선했고, 데이터를 분석하기 위해 머신러닝을 익혔고, 서비스를 검증하기 위해 직접 제품을 만들었습니다. 의료, 제조, 콘텐츠, 금융까지 분야는 달라졌지만 목표는 같았습니다. 문제를 발견하고, 반복 가능한 시스템으로 만드는 것.

지금은 AI Agent와 Workflow로 사람의 업무를 자동화하는 서비스를 설계합니다.

---

## 지금 하는 일

- **[token-saver](https://github.com/kimheetae0104/token-saver)** · Claude Code용 토큰 효율화 플러그인을 만들고 실측 데이터를 쌓고 있습니다. 표준 라이브러리만 사용, 테스트 223개.
- **[INKK](https://inkk.online)** · 카드뉴스 자동 생성 SaaS를 운영하며 생성 품질과 비용을 함께 조정하고 있습니다.
- LLM의 비결정성을 다루는 3계층 설계(아래 [설계 철학](#설계-철학))를 여러 프로젝트에 반복 적용하며 검증하는 중입니다.

---

## 대표 작업

### 🧰 [token-saver](https://github.com/kimheetae0104/token-saver) · Claude Code 플러그인

에이전트가 서브에이전트에 작업을 위임할 때, 작업 성격(검증 오라클 유무·배치 크기·위험도)에 맞는 모델 티어를 고르도록 강제하는 게이트입니다.

- **어려웠던 지점.** "자동으로 싼 모델을 쓴다"는 접근은 품질을 떨어뜨립니다. 그래서 모델을 자동 전환하지 않고, **판단을 빼먹지 못하게 막는 쪽**으로 설계를 바꿨습니다.
- **결과.** 실험에서 정답률·품질 손실 없이 비용만 6.8~7.6배 감소. 다만 N=6~7 세션 실측이고 제3자 검증이 없다는 점을 리드미에 명시했습니다. 근거는 [PROTOCOL.md](https://github.com/kimheetae0104/token-saver/blob/main/experiments/PROTOCOL.md)에 있습니다.
- **스택.** Python(표준 라이브러리만) · Claude Code Plugin API · 테스트 223개

### 🏭 [NOxO](https://gimhuitae-portfolio.vercel.app/NOxO.html) · 산업 시계열 예측

발전소 CEMS 1초 스트림을 받아 5분 뒤 NOx 농도를 예측합니다.

- **어려웠던 지점.** 초기 모델의 성능이 비정상적으로 좋았습니다. 원인을 추적해 **라벨 누수**를 찾아냈고, 시간 순서를 지키는 walk-forward 검증으로 구조를 다시 설계했습니다.
- **결과.** 누수를 제거한 정직한 기준에서 Test MAE 20배 개선.
- **스택.** Python · Ridge · LightGBM · walk-forward CV

### 🃏 [INKK](https://inkk.online) · 카드뉴스 생성 SaaS

주제 한 줄을 넣으면 1분 안에 카드뉴스 5~10장을 만듭니다.

- **어려웠던 지점.** LLM 출력이 그대로면 "AI가 쓴 티"가 납니다. 후처리를 4층으로 나눠 문체 흔적을 걷어냈습니다.
- **결과.** 11종 ROLE TYPES 자동 배정, 6종 스타일 프리셋으로 운영 중.
- **스택.** Next.js 16 · TypeScript · Claude / Groq Llama · Supabase RLS · Upstash

### 🤖 [Blog Agent](https://gimhuitae-portfolio.vercel.app/blogagent.html) · RAG 기반 자동 발행

로컬 LLM 초안 → Gemini 검증 → Claude 편집 → Naver 자동 발행까지 이어지는 파이프라인입니다.

- **어려웠던 지점.** 검증 단계가 한 모델에 의존하면 그 모델이 막히는 순간 전체가 멈춥니다. 4단 폴백으로 끊기지 않게 만들었습니다.
- **결과.** ChromaDB RAG 기준 Recall@2 84.6%, 섹터 필터 적용 시 46.1%p 상승.
- **스택.** Python · Ollama(exaone3.5) · Claude · Gemini · ChromaDB · DART API

<details>
<summary><b>그 외 프로젝트</b></summary>

<br/>

| 프로젝트 | 한 줄 설명 |
|---|---|
| [JANN](https://gimhuitae-portfolio.vercel.app/JANN.html) · iOS 온디바이스 AI | 카메라로 식재료 인식 후 향미 분자 1,107종 기반 추천. CoreML 18MB, 네트워크 호출 0 |
| [Real Estate Analysis](https://github.com/kimheetae0104/real-estate-analysis-app) | 500m 격자 브랜드 밀집도로 저평가 상권 발굴. "올리브영+다이소 조합 = 지가 15% 프리미엄" 정량화 |
| [DeepCare Nursing App](https://github.com/kimheetae0104/deepcare-nursing-app) | YOLO-Pose 자세 추정 + 강화학습(DQN/PPO)으로 욕창 예방 스케줄 최적화 |
| [Starbucks Seat Finder](https://github.com/kimheetae0104/starbucks-seat-finder) | 위치 기반 혼잡도 모니터링 + 텔레그램 자동 알림 |
| [DACON 스마트창고](https://gimhuitae-portfolio.vercel.app/DACON.html) | 물류 최적화 AI 대회. 최종 LB 10.1873 |

</details>

---

## 설계 철학

> **Directives → Orchestration → Execution**
>
> LLM은 같은 입력에 같은 출력을 주지 않습니다. 그래서 판단이 필요한 부분과 정확해야 하는 부분을 분리합니다.
>
> - **Directives**: 목표와 제약을 정의한다 (what)
> - **Orchestration**: 작업을 분해하고 흐름을 제어한다 (how)
> - **Execution**: 결정론적 Python 코드로 실제로 실행한다 (do)

이 구조를 Blog Agent, Real Estate Analysis, Starbucks Finder에 반복 적용했고, token-saver에서는 한 걸음 더 나가 **효과를 측정 가능한 형태로 남기는 것**까지 설계에 넣었습니다. 실측 없이 "빨라졌다, 싸졌다"고 말하지 않는 것이 이 철학의 마지막 조각이라고 생각합니다.

---

## 기술 스택

**AI · ML** Python · Claude API · Gemini API · Ollama · ChromaDB · XGBoost · LightGBM · YOLO-Pose · MediaPipe · CoreML

**Product** TypeScript · Next.js · React · Supabase · Tailwind · Vercel

**Automation** Playwright · Selenium · Telegram Bot API · Google Sheets API

---

<p align="center">
  <i>AI가 단순 반복을 대신하고, 저는 더 어려운 문제를 풀 시간을 법니다.</i>
</p>
