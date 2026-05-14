<h1 align="center">김희태 · AI Agent Developer</h1>

<p align="center">
  <a href="https://gimhuitae-portfolio.vercel.app" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white"/>
  </a>
  <a href="https://cardnews-saas.vercel.app" target="_blank">
    <img src="https://img.shields.io/badge/CardNews_SaaS-4F46E5?style=for-the-badge&logo=vercel&logoColor=white"/>
  </a>
</p>

<br/>

처음엔 HTML도 몰랐습니다.

학원 6개월, HTML부터 시작해서 JavaScript, Java, Spring, Python을 훑었어요. 그때 만든 건 2개짜리 프로젝트였는데, 그게 시작이었습니다.

그 뒤로 늘 같은 방식이었어요. **풀고 싶은 문제가 생기면, 그걸 반복해서 해결할 수 있는 수단을 찾았습니다.** 환자 욕창을 막고 싶어서 컴퓨터 비전과 강화학습을 공부했고, 상권을 데이터로 분석하고 싶어서 XGBoost를 썼어요. 서비스를 직접 팔아보고 싶어서 결제 시스템까지 붙였고, AI가 쓴 글을 믿을 수 없어서 팩트체커를 만들었습니다. 도메인은 의료, 부동산, SaaS, 금융으로 매번 달라졌지만, 방식은 한 번도 바뀌지 않았어요.

필요해서 배웠고, 배운 건 반드시 동작하는 무언가로 만들었습니다.

지금은 그 연장선에서 **AI 에이전트**를 만들고 있어요. 사람이 반복해서 해야 했던 판단과 실행을, AI가 스스로 해내는 시스템입니다.

`문제 정의` `반복 가능한 시스템` `자동화` `LLM 파이프라인`

---

## 🛠 Tech Stack

**AI / ML**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Claude](https://img.shields.io/badge/Claude_API-D97757?style=flat-square&logo=anthropic&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini_API-4285F4?style=flat-square&logo=google&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-FF6600?style=flat-square&logo=python&logoColor=white)
![YOLO](https://img.shields.io/badge/YOLO_Pose-00FFFF?style=flat-square&logo=opencv&logoColor=black)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square&logo=google&logoColor=white)

**Frontend / Backend**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white)

**Infra / Tools**

![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=flat-square&logo=selenium&logoColor=white)
![Telegram](https://img.shields.io/badge/Telegram_Bot-26A5E4?style=flat-square&logo=telegram&logoColor=white)
![Google Sheets](https://img.shields.io/badge/Google_Sheets-34A853?style=flat-square&logo=google-sheets&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

---

## 🚀 주요 프로젝트

| 프로젝트 | 설명 | 스택 |
|---------|------|------|
| 🤖 **[Blog Agent RAG](https://gimhuitae-portfolio.vercel.app/BlogAgentRAG.html)** | 상한가 종목 감지 → DART 크롤링 → LLM 블로그 자동 작성 → 네이버 발행까지 완전 자동화 파이프라인. 팩트체커·환각 감지 내장 | Python · Claude · Gemini · Playwright · Google Sheets |
| 🃏 **[CardNews SaaS](https://cardnews-saas.vercel.app)** | 텍스트 → AI 카드뉴스 자동 변환 SaaS. 무료/유료 구독 플랜, 결제 연동 | Next.js · TypeScript · Claude · Supabase · Stripe |
| 🗺️ **[Real Estate Analysis](https://github.com/kimheetae0104/real-estate-analysis-app)** | 500m 격자 기반 브랜드 밀집도 분석으로 저평가 상권 발굴. "올리브영+다이소 조합 = 지가 15% 프리미엄" 정량화 | Python · XGBoost · Claude · Google Slides |
| ☕ **[Starbucks Seat Finder](https://github.com/kimheetae0104/starbucks-seat-finder)** | 위치 기반 스타벅스 혼잡도 실시간 모니터링 + 텔레그램 자동 알림 | Python · Playwright · Naver Map API · Telegram Bot |
| 🏥 **[DeepCare Nursing App](https://github.com/kimheetae0104/deepcare-nursing-app)** | 컴퓨터 비전(YOLO-Pose)으로 환자 자세 추정 + 강화학습(DQN/PPO)으로 욕창 예방 간호 스케줄 최적화 | Python · YOLO · MediaPipe · DQN · PPO |

---

## 🏗️ 설계 철학

> **Directives → Orchestration → Execution**
>
> LLM의 비결정성 문제를 3계층 구조로 해결합니다.
> - **Directives**: 목표와 제약 정의 (what)
> - **Orchestration**: 작업 분해 및 흐름 제어 (how)
> - **Execution**: 결정론적 Python 코드로 실제 실행 (do)
>
> 여러 프로젝트(Blog Agent, Real Estate Analysis, Starbucks Finder)에 동일하게 적용 중.

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=kimheetae0104&show_icons=true&theme=tokyonight&hide_border=true" height="150"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=kimheetae0104&layout=compact&theme=tokyonight&hide_border=true" height="150"/>
</p>

---

<p align="center">
  <i>AI가 단순 반복을 대신하고, 저는 더 어려운 문제를 풀 시간을 법니다.</i>
</p>
