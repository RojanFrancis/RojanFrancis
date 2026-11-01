<div align="center">

# Rojan Francis R

### Backend engineer · Java 21 · Spring Boot · AI integrations

I build Java backends that hold up in production: signed webhooks, idempotent money movement, retries that can't double-send.<br>
Then I wire AI in as a typed, tested component, not a chatbot bolted on the side.

[![Live project](https://img.shields.io/badge/Live_demo-ElevateBox_voice_agent-2ee6a6?style=for-the-badge&logo=render&logoColor=black)](https://elevatebox-agent.onrender.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-111111?style=for-the-badge&logo=googlechrome&logoColor=white)](https://rojanfrancisportfolio.freebuff.app/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:rojanfrancis0@gmail.com)
<!-- Add when ready:
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/YOUR-HANDLE)
-->

**Open to:** backend / SDE internships with a PPO and SDE-1 roles from 2027, especially in fintech

</div>

---

## Right now

- 📞 **ElevateBox** makes real phone calls: message "call me" on WhatsApp and an AI agent rings you within a minute, sends details to your WhatsApp *during* the call, and rates the lead when you hang up.
- 🌱 **Open-source contributor:** 1 pull request merged into OpenRewrite, 4 more in review at Spring AI, OpenRewrite and Google Jib.
- 🎓 Final-year B.Tech (Computer & Communication Engineering), **Manipal University Jaipur**, graduating **May 2027** · CGPA 8.1
- 💼 Previously **Backend Developer Intern at FinStocks AI** (AI trading startup, Dec 2025 – Feb 2026): Java and Spring Boot for a platform that backtests strategies and places approved orders through users' brokerage accounts.

---

## Featured: ElevateBox AI voice agent

<a href="https://elevatebox-agent.onrender.com"><img src="https://raw.githubusercontent.com/RojanFrancis/elevatebox-agent/main/docs/demo.png" alt="ElevateBox demo page: an animated phone replays a real call next to the pitch" width="100%"></a>

**[Live demo](https://elevatebox-agent.onrender.com) · [Code](https://github.com/RojanFrancis/elevatebox-agent)**

```
WhatsApp "call me"  →  consent + cooldown check  →  AI calls from an Indian number
        →  agent calls send_whatsapp mid-call  →  Gemini rates the lead  →  summary on WhatsApp + dashboard
```

- Coordinates **four external systems** (Meta WhatsApp Cloud API, Bolna voice AI, Gemini, TiDB) from one Spring Boot service, with the voice platform swappable by config (Bolna or Vapi).
- **Verified webhooks:** Meta's HMAC-SHA256 signatures, a separate secret for voice callbacks and tools, constant-time comparison.
- **Safe to retry:** de-duplicated deliveries, so each call is analysed once and the mid-call WhatsApp is sent once, however often a webhook fires.
- **Consent and cost limits:** calls only on request, one per number per day, a global daily cap, a missed call frees the cooldown.
- Webhooks answer instantly and the AI work runs on a bounded pool (503 when full, so senders retry). **143 tests** in CI, Docker on Render.

`Java 21` `Spring Boot 3` `Spring Data JPA` `WebClient` `Bolna` `Gemini` `Meta WhatsApp Cloud API` `TiDB` `Docker` `GitHub Actions`

---

## More projects

### 💳 [Event-sourced payment ledger](https://github.com/RojanFrancis/event-sourced-ledger) · [Live demo](https://event-sourced-ledger-1.onrender.com)
Every money movement is an immutable `CREDIT` / `DEBIT` event. There is **no balance column**: balances, current or as of any timestamp, are derived by replaying history, and every transfer is a debit and a credit that sum to zero.
- Double-entry bookkeeping, idempotent transfers, account statements, JWT-secured REST APIs
- AI finance controller: Gemini for batch reconciliation and plain-English settlement queries

`Java 21` `Spring Boot 3.5` `Spring Security (JWT)` `Spring Data JPA` `MySQL` `React 19` `Gemini`

### 🔐 [CipherLab](https://github.com/RojanFrancis/cipherlab)
Cryptography lab and secure-messaging prototype: AES-GCM, ECDH key exchange, digital signatures, HKDF and authenticated handshakes, built on the standard Java crypto APIs.

`Java` `JCA / JCE`

### 🏠 FlatMate OS *(private)*
Local-first assistant for shared flats: turns free-form household messages into validated expenses, chores and reminders with a local model, so no data leaves the machine.

`React` `TypeScript` `Ollama` `Gemma 3 4B`

---

## Open source

| Project | Contribution | Status |
|---|---|---|
| [spring-projects/spring-ai](https://github.com/spring-projects/spring-ai) | [#7263](https://github.com/spring-projects/spring-ai/pull/7263): HSQLDB dialect for the JDBC session repository, with a standard-SQL `MERGE` upsert, schema, docs and contract tests | 🟡 In review |
| [openrewrite/rewrite-spring](https://github.com/openrewrite/rewrite-spring) | [#1235](https://github.com/openrewrite/rewrite-spring/pull/1235): fixes `JdbcTemplateQueryForLongMigration`, which mis-bound `Object[], int[]` arguments and turned SQL `NULL` into an NPE; rebuilt on `JavaTemplate` | 🟡 In review |
| [openrewrite/rewrite-spring](https://github.com/openrewrite/rewrite-spring) | [#1242](https://github.com/openrewrite/rewrite-spring/pull/1242): stops `MigrateAuditorAwareToOptional` from wrapping `return`s inside nested lambdas, which produced code that didn't compile | ✅ Merged |
| [openrewrite/rewrite-spring](https://github.com/openrewrite/rewrite-spring) | [#1243](https://github.com/openrewrite/rewrite-spring/pull/1243): keeps statically imported `PathSelectors.regex(..)` calls compiling when `NormalizeSpringfoxPathSelectorsRegexToAnt` rewrites them to `ant(..)` | 🟡 In review |
| [GoogleContainerTools/jib](https://github.com/GoogleContainerTools/jib) | [#4531](https://github.com/GoogleContainerTools/jib/pull/4531): makes `jib.container.environment` a lazily evaluated Gradle `MapProperty` (fixes #4067) | 🟡 In review |

---

## Toolbox

![Java](https://img.shields.io/badge/Java_21-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat&logo=springsecurity&logoColor=white)
![Hibernate](https://img.shields.io/badge/JPA_/_Hibernate-59666C?style=flat&logo=hibernate&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Render](https://img.shields.io/badge/Render-000000?style=flat&logo=render&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![Gemini](https://img.shields.io/badge/Gemini_API-4285F4?style=flat&logo=googlegemini&logoColor=white)
![WhatsApp](https://img.shields.io/badge/WhatsApp_Cloud_API-25D366?style=flat&logo=whatsapp&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white)

**Certifications:** Cisco CyberOps Associate · Cisco DevNet Associate · Cisco Ethical Hacker · Oracle Certified Professional: Java SE 21 Developer *(in progress)*
