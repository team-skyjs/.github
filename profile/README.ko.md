<p align="center">
  <img src="https://raw.githubusercontent.com/team-skyjs/.github/main/profile/images/app-icon.png" alt="K-Bap app icon" width="112">
</p>
<h1 align="center">K-Bap</h1>
<p align="center"><b>한국 메뉴판을 내 언어로, 음식 이해부터 주문까지.</b></p>
<p align="center">
  <a href="https://kbap.site/">Website</a> ·
  <a href="https://apps.apple.com/us/app/k-bap/id6788635067">App Store</a> ·
  <a href="https://play.google.com/store/apps/details?id=com.rocher.kbap">Google Play</a>
</p>
<p align="center"><a href="https://github.com/team-skyjs/.github/blob/main/profile/README.md">English</a> · <a href="https://github.com/team-skyjs/.github/blob/main/profile/README.ko.md">한국어</a></p>

## 한국에서 무엇을 먹을지 고민될 때

K-Bap은 외국인 여행자와 거주자가 한국 메뉴판을 읽고, 음식을 이해하고, 주문할 수 있도록 돕는 앱입니다. **iOS와 Android에서 이용할 수 있습니다.**

메뉴 이름을 번역하는 것에서 한 걸음 더 나아가 음식 설명과 재료 정보, 다른 이용자의 리뷰를 함께 살펴보고 식당 직원에게 한국어 질문·주문 카드를 보여줄 수 있습니다.

- **메뉴판 스캔·번역** — 메뉴판을 찍고 번역된 음식 이름과 가격을 확인합니다.
- **음식·재료 탐색** — 음식 설명과 매운 정도, 피하는 재료에 따른 안내를 살펴봅니다.
- **국적별 리뷰** — 외국인 이용자의 음식 리뷰를 읽고 같은 국적의 리뷰로 필터링합니다.
- **한국어 질문·주문 카드** — 재료를 물어보거나 선택한 메뉴를 주문할 때 직원에게 보여줍니다.

재료 안내는 참고 정보이며 알레르기 안전이나 비건·할랄 등 식단 적합성을 보장하지 않습니다. 실제 재료와 조리 방식은 식당마다 다르므로 직원에게 확인해 주세요.

## 앱 화면

메뉴판 → 번역 결과 → 음식 상세 → 한국어 주문 카드

<p align="center">
  <img src="https://raw.githubusercontent.com/team-skyjs/.github/main/profile/images/screen-menu.png" alt="Korean example menu" width="180">
  <img src="https://raw.githubusercontent.com/team-skyjs/.github/main/profile/images/screen-scan.png" alt="Translated menu results" width="180">
  <img src="https://raw.githubusercontent.com/team-skyjs/.github/main/profile/images/screen-detail.png" alt="Dish and ingredient details" width="180">
  <img src="https://raw.githubusercontent.com/team-skyjs/.github/main/profile/images/screen-order.png" alt="Korean order card for staff" width="180">
</p>

2026년 10월 14일 iOS 시뮬레이터 캡처 · 예시 메뉴와 사용자 설정을 사용했습니다. 화면의 표시는 해당 예시 설정에 따른 안내입니다.

**지원 언어 10개:** English · 한국어 · 日本語 · 简体中文 · 繁體中文 · Español · Русский · Tiếng Việt · Bahasa Indonesia · ไทย

## Team skyjs

K-Bap을 만드는 2인 팀입니다.

| 팀원 | 역할 | GitHub |
|---|---|---|
| 김예진 | 제품 · 모바일 · 백엔드 · 디자인 연동 | [@rocher71](https://github.com/rocher71) |
| 심종한 | 백엔드 · 인프라 · 데이터 파이프라인 | [@simhani1](https://github.com/simhani1) |

## 공개 저장소

| 저장소 | 내용 | 기술 |
|---|---|---|
| [kbap-fe](https://github.com/team-skyjs/kbap-fe) | 모바일 앱 | React Native · Expo · TypeScript |
| [kbap-server](https://github.com/team-skyjs/kbap-server) | API·배치 서버 | Kotlin · Spring Boot · MySQL · Redis |
| [kbap-landing](https://github.com/team-skyjs/kbap-landing) | 공식 웹사이트 | Web |
| [kbap-langchain](https://github.com/team-skyjs/kbap-langchain) | 음식 데이터 파이프라인 | Python · LangChain / LangGraph |
| [kbap-image-maker](https://github.com/team-skyjs/kbap-image-maker) | 음식 이미지 생성 도구 | Python |
| [kbap-legal](https://github.com/team-skyjs/kbap-legal) | 개인정보 처리방침·약관 | Static site |
| [kbap-study](https://github.com/team-skyjs/kbap-study) | 서버 개발 학습 기록 | Documentation |

## 개발과 운영

- 모바일: Expo Router · TanStack Query · Reanimated · i18next · Firebase Auth · ML Kit 온디바이스 OCR
- 서버: Spring Boot · JPA / Flyway · MySQL · Redis · AWS
- 품질·배포: GitHub PR 리뷰 · Jest · EAS Build / Update · GitHub Actions
- 제품·디자인: Jira · Figma · 제품 명세와 실제 구현을 대조하는 검토

[공식 웹사이트](https://kbap.site/) · [개인정보 처리방침](https://team-skyjs.github.io/kbap-legal/privacy-policy.html)

_소개 갱신: 2026-10-16_
