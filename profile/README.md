<!-- team-skyjs/.github/profile/README.md — English. 한국어: README.ko.md -->

**English** · [한국어](./README.ko.md)

<p align="center">
  <img src="./images/hero.png" alt="K-Bap — scan any Korean menu, see what's safe for you" width="720">
</p>

<p align="center">
  <a href="https://apps.apple.com/app/id6788635067"><img src="./images/badge-app-store.svg" alt="Download on the App Store" height="44"></a>
  &nbsp;
  <a href="https://play.google.com/store/apps/details?id=com.rocher.kbap"><img src="./images/badge-google-play.svg" alt="Get it on Google Play" height="44"></a>
</p>

<p align="center">
  <b>iOS</b> on the App Store · <b>Android</b> rolling out on Google Play · Project board: <a href="https://simhani1.atlassian.net/jira/software/projects/KB/boards/2">Jira KB</a> (team members only)
</p>

---

# skyjs

We are a two-person team building **K-Bap**, a Korean food safety guide for people who can't read a Korean menu but need to know what's safe for them to eat.

| | Role | GitHub |
|---|---|---|
| **Yejin Kim** | Product · mobile (React Native) · backend · design integration | [@rocher71](https://github.com/rocher71) |
| **Jonghan Sim** | Backend · infrastructure · data pipeline | [@simhani1](https://github.com/simhani1) |

---

## K-Bap

> Scan any Korean menu. See what's safe for *you* before you order.

Korean menus rarely list ingredients, and staff often can't explain them in English. K-Bap closes that gap for travelers and residents with allergies, dietary rules (vegan, halal, kosher, gluten-free …) and spice limits.

<p align="center">
  <img src="./images/screen-scan.png" alt="Scan a menu" width="180">
  <img src="./images/screen-risk.png" alt="Personal risk verdict" width="180">
  <img src="./images/screen-ingredients.png" alt="What's inside" width="180">
  <img src="./images/screen-ask-owner.png" alt="Ask the owner card" width="180">
</p>

**What it does**

- **Scan a menu** — point the camera at a Korean menu; dishes are recognized and matched to our curated food database.
- **Personal risk verdict** — every dish is rated Safe / Caution / Danger / Unable to assess against the ingredients you avoid, with the reason shown.
- **Ingredients, explained** — what's inside each dish, how often an ingredient appears across restaurants, and translated names.
- **Ask the owner** — a one-tap Korean card you show to staff: "Does this contain X? I have a food allergy."
- **Reviews from travelers like you** — ratings and notes, filterable by your own nationality.
- **Order history & reminders** — keep what you ordered and get a nudge to review it later.

10 UI languages: English, 한국어, 中文(简体·繁體), 日本語, Español, Русский, Tiếng Việt, Bahasa Indonesia, ไทย.

---

## Repositories

| Repo | What it is | Stack |
|---|---|---|
| [kbap-fe](https://github.com/team-skyjs/kbap-fe) | Mobile app | React Native · Expo · TypeScript |
| [kbap-server](https://github.com/team-skyjs/kbap-server) | API server | Kotlin · Spring Boot · MySQL · AWS |
| [kbap-image-maker](https://github.com/team-skyjs/kbap-image-maker) | Dish image generation pipeline | Python |
| [kbap-langchain](https://github.com/team-skyjs/kbap-langchain) | LLM experiments for menu understanding | Python |
| [kbap-legal](https://github.com/team-skyjs/kbap-legal) | Privacy policy, terms, safety notice | Static site |
| [kbap-study](https://github.com/team-skyjs/kbap-study) | Server-side study notes | — |

Specs, the admin console and internal tooling live in private repositories.

---

## How we work

- Jira for tasks, GitHub PRs with AI-assisted code review, and a spec repository as the single source of truth for product decisions.
- Safety first: a dish is never shown as "safe" unless we can verify it. When we can't, we say so and point you to the owner.

_Safety information in K-Bap is guidance, not medical advice. Always confirm with the restaurant._
