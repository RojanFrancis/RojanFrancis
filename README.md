<div align="center">

# Rojan Francis R

**Backend Engineer · Java · Spring Boot · AI Integration**

*I build Java backends where correctness comes first — and wire LLMs in as typed components, not chatbots bolted on.*

[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat&logo=googlechrome&logoColor=white)](https://rojanfrancisportfolio.freebuff.app/)
[![Email](https://img.shields.io/badge/rojanfrancis0@gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:rojanfrancis0@gmail.com)
<!-- Add when ready:
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/YOUR-HANDLE)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat&logo=leetcode&logoColor=black)](https://leetcode.com/u/YOUR-HANDLE)
-->

</div>

---

## About

Final-year B.Tech (Computer & Communication Engineering) at **Manipal University Jaipur** · graduating **May 2027** · CGPA 8.1/10.
Former **Backend Developer Intern at FinStocks AI** (AI trading startup, Dec 2025 – Feb 2026): Java, Spring Boot.

**Open to:** backend / SDE internships with PPO and SDE-1 roles, especially fintech.

---

## Projects

### 💳 [Event-Sourced Payment Ledger](https://github.com/RojanFrancis/event-sourced-ledger) · [Live demo](https://event-sourced-ledger-1.onrender.com)
Every money movement is an immutable `CREDIT`/`DEBIT` event. The accounts table has **no balance column** — balances (current or as of any timestamp) are derived by replaying history, and every transfer is a debit + credit that sum to zero.
- Double-entry bookkeeping, account statements, JWT-secured REST APIs
- AI Finance Controller: Gemini for batch reconciliation and natural-language settlement queries

`Java 21` `Spring Boot 3.5` `Spring Security (JWT)` `Spring Data JPA` `MySQL` `React 19` `Gemini`

### 📞 [ElevateBox AI Voice Agent](https://github.com/RojanFrancis/elevatebox-agent) · [Live demo](https://elevatebox-agent.onrender.com)
Post-call sales pipeline: the full call transcript is classified **HOT / WARM / COLD / UNKNOWN** by Gemini with structured JSON output, then the matching action runs — a transcript-aware WhatsApp follow-up or a callback time extracted from what the lead said.
- Bearer-authenticated Vapi webhook with async processing and duplicate-event protection
- Dockerised, CI on GitHub Actions, deployed on Render

`Java 21` `Spring Boot` `Vapi` `Gemini` `Meta WhatsApp Cloud API` `TiDB` `Docker`

### 🔐 [CipherLab](https://github.com/RojanFrancis/cipherlab)
Educational cryptography lab and secure-messaging prototype — AES-GCM, ECDH key exchange, digital signatures, HKDF and authenticated handshakes.

`Java` `JCA/JCE`

### 🏠 FlatMate OS
Private, local-first assistant for shared flats: converts free-form household messages into validated, structured expenses, chores and reminders using a local model — no data leaves the machine.

`React` `TypeScript` `Ollama` `Gemma 3 4B`

---

## Open Source

| Project | Contribution | Status |
|---|---|---|
| [spring-projects/spring-ai](https://github.com/spring-projects/spring-ai) | [#7263](https://github.com/spring-projects/spring-ai/pull/7263): HSQLDB dialect for the JDBC session repository: standard-SQL `MERGE` upsert, schema, docs and contract tests | 🟡 Open, in review |
| [openrewrite/rewrite-spring](https://github.com/openrewrite/rewrite-spring) | [#1235](https://github.com/openrewrite/rewrite-spring/pull/1235): fix `JdbcTemplateQueryForLongMigration`, which mis-bound `Object[], int[]` arguments and turned SQL `NULL` into an NPE; rebuilt on `JavaTemplate` | 🟡 Open, in review |
| [GoogleContainerTools/jib](https://github.com/GoogleContainerTools/jib) | [#4531](https://github.com/GoogleContainerTools/jib/pull/4531): make `jib.container.environment` a lazily-evaluated Gradle `MapProperty` (fixes #4067) | 🟡 Open, in review |

---

## Stack

![Java](https://img.shields.io/badge/Java_21-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat&logo=springsecurity&logoColor=white)
![Hibernate](https://img.shields.io/badge/JPA_/_Hibernate-59666C?style=flat&logo=hibernate&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![Gemini](https://img.shields.io/badge/Gemini_API-4285F4?style=flat&logo=googlegemini&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white)

---

## Certifications

- Cisco **CyberOps Associate** · **DevNet Associate** · **Ethical Hacker**
- Oracle Certified Professional: **Java SE 21 Developer** — in progress
