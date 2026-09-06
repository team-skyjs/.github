<!-- team-skyjs/.github/profile/README.ko.md — 한국어. English: README.md -->

[English](./README.md) · **한국어**

<p align="center">
  <img src="./images/hero.png" alt="K-Bap — 한국 메뉴판을 찍으면 나에게 안전한 음식이 보입니다" width="720">
</p>

<p align="center">
  <a href="https://apps.apple.com/app/id6788635067"><img src="./images/badge-app-store.svg" alt="App Store에서 다운로드" height="44"></a>
  &nbsp;
  <a href="https://play.google.com/store/apps/details?id=com.rocher.kbap"><img src="./images/badge-google-play.svg" alt="Google Play에서 받기" height="44"></a>
</p>

<p align="center">
  <b>iOS</b> App Store 출시 · <b>Android</b> Google Play 출시 중 · 프로젝트 보드: <a href="https://simhani1.atlassian.net/jira/software/projects/KB/boards/2">Jira KB</a> (팀원만 열람 가능)
</p>

---

# skyjs

한국 음식 안전 가이드 앱 **K-Bap**을 만드는 2인 팀입니다. 한국 메뉴판을 읽지 못하지만 자기가 먹어도 되는 음식인지 알아야 하는 사람들을 위한 앱입니다.

| | 역할 | GitHub |
|---|---|---|
| **김예진** | 제품 · 모바일(React Native) · 백엔드 · 디자인 연동 | [@rocher71](https://github.com/rocher71) |
| **심종한** | 백엔드 · 인프라 · 데이터 파이프라인 | [@simhani1](https://github.com/simhani1) |

---

## K-Bap

> 한국 메뉴판을 찍으면, 나에게 안전한 음식이 무엇인지 주문 전에 알려줍니다.

한국 메뉴판에는 재료가 적혀 있지 않고, 직원이 영어로 설명해 주기도 어렵습니다. K-Bap은 알레르기, 식단 규칙(비건·할랄·코셔·글루텐프리 등), 매운 정도 때문에 곤란한 외국인 여행자와 거주자를 위해 그 틈을 메웁니다.

<p align="center">
  <img src="./images/screen-scan.png" alt="메뉴 스캔" width="180">
  <img src="./images/screen-risk.png" alt="개인 위험도 판정" width="180">
  <img src="./images/screen-ingredients.png" alt="재료 설명" width="180">
  <img src="./images/screen-ask-owner.png" alt="사장님에게 물어보기 카드" width="180">
</p>

**주요 기능**

- **메뉴 스캔** — 카메라로 메뉴판을 찍으면 메뉴를 인식해 우리가 검수한 음식 DB와 매칭합니다.
- **개인 위험도 판정** — 내가 피하는 재료를 기준으로 모든 메뉴를 안전 / 주의 / 위험 / 판정 불가로 표시하고, 이유를 함께 보여줍니다.
- **재료 설명** — 음식에 들어가는 재료, 식당마다 쓰이는 비율, 번역된 재료 이름.
- **사장님에게 물어보기** — 직원에게 보여주는 한국어 카드: "이 음식에 X가 들어가나요? 음식 알레르기가 있어요."
- **같은 국적의 리뷰** — 여행자들의 평점과 후기를 내 국적 기준으로 걸러 봅니다.
- **주문 기록·리마인더** — 주문한 음식을 기록하고, 나중에 리뷰를 남기도록 알려줍니다.

UI 언어 10개: English, 한국어, 中文(简体·繁體), 日本語, Español, Русский, Tiếng Việt, Bahasa Indonesia, ไทย.

---

## 저장소

| Repo | 설명 | Stack |
|---|---|---|
| [kbap-fe](https://github.com/team-skyjs/kbap-fe) | 모바일 앱 | React Native · Expo · TypeScript |
| [kbap-server](https://github.com/team-skyjs/kbap-server) | API 서버 | Kotlin · Spring Boot · MySQL · AWS |
| [kbap-image-maker](https://github.com/team-skyjs/kbap-image-maker) | 음식 이미지 생성 파이프라인 | Python |
| [kbap-langchain](https://github.com/team-skyjs/kbap-langchain) | 메뉴 이해를 위한 LLM 실험 | Python |
| [kbap-legal](https://github.com/team-skyjs/kbap-legal) | 개인정보 처리방침 · 이용약관 · 안전 고지 | 정적 사이트 |
| [kbap-study](https://github.com/team-skyjs/kbap-study) | 서버 학습 노트 | — |

스펙, 어드민 콘솔, 내부 도구는 비공개 저장소에 있습니다.

---

## 스택 & 도구

**모바일 앱 (kbap-fe)**
- React Native 0.85 · Expo · expo-router · TypeScript
- TanStack Query · Reanimated · react-native-svg · i18next(10개 언어)
- Firebase Auth(Apple·Google 로그인) · ML Kit 텍스트 인식(온디바이스 OCR) · expo-camera · expo-notifications(로컬 리마인더) · expo-secure-store
- Sentry · Amplitude
- EAS Build / EAS Update(OTA, teamtest·production 채널) / EAS Workflows(자동 OTA CI) / EAS Submit · TestFlight · Jest

**백엔드 (kbap-server)**
- Kotlin · Spring Boot · Gradle 멀티모듈(api · batch · common)
- MySQL(JPA + Flyway) · Redis(리프레시 토큰 회전, 스캔 예약) · JWT
- Firebase Admin(토큰 검증·계정 삭제) · AWS S3(이미지, presigned 업로드) · S3 Vectors(음식 임베딩) · SQS(배치 파이프라인)
- OpenAI(gpt-4o-mini, text-embedding-3-small, gpt-image-2) · Google Places / Geocoding · Frankfurter(환율)
- Langfuse(LLM 관측) · Micrometer + Prometheus + Grafana · k6 + JFR 부하 테스트 · Docker

**인프라**
- AWS ECS + ALB + CloudWatch + SSM Parameter Store + Route 53 · Terraform
- GitHub Actions(빌드, dev/prod 카나리 배포)

**콘텐츠 파이프라인**
- kbap-langchain: LangGraph / LangChain(OpenAI + Google Gemini) · Langfuse · SQS 소비 · Python(uv)
- kbap-image-maker: OpenAI Images API(gpt-image-2) · Python

**어드민 (kbap-admin)**
- React · Vite · TypeScript · TanStack Router / Query / Table · Tailwind + shadcn/Radix · Cloudflare Pages

**디자인**
- Figma(디자이너 시안) · Claude Design(초기 디렉션) · Baloo 2(브랜드 폰트, Google Fonts)

**협업·운영**
- Jira(KB) · GitHub(조직, 브랜치 룰셋) · OpenAI Codex(PR 자동 리뷰) · Claude Code(커맨드 센터·FE·BE 세션, spec-kit)
- App Store Connect · Google Play Console · Firebase 콘솔 · Proxyman(네트워크 QA)

---

## 일하는 방식

- Jira로 태스크를 관리하고, GitHub PR마다 AI 코드 리뷰를 거치며, 제품 결정은 스펙 저장소를 단일 정본으로 둡니다.
- 안전이 먼저입니다. 확인할 수 없는 음식은 절대 "안전"으로 표시하지 않고, 모른다고 말한 뒤 사장님에게 확인하도록 안내합니다.

_K-Bap의 안전 정보는 참고용이며 의학적 조언이 아닙니다. 반드시 식당에 확인하세요._
