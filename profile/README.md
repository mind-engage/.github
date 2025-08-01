# MindEngage

> AI-powered authoring studio for interactive lessons, quizzes, diagrams, and simulations.

[Website](https://mindengage.ai) · [Docs](https://mindengage.gitbook.io/mindengage-docs/) · [Contact](mailto:hello@mindengage.ai)

---

## What is MindEngage?
MindEngage is a managed (proprietary) platform to **generate, edit, and publish** interactive courseware with LLMs and optional RAG.  
This GitHub organization hosts **public companion projects** (gateways, validators, integrations) and **forks** we use in our workflows.  
> Self-hosting the core platform is not supported. If you need private deployment options, contact us.

---

## Public Repositories

| Repo | What it is | Tech | Notes |
|---|---|---|---|
| **mindengage-lms** | Service(s) supporting LMS workflows used with MindEngage | Go | Public |
| **certichain-gateway** | Stateless **LTI 1.3** gateway that bridges LMS course completions to the **CertiChain** network for automated verifiable credential issuance | TypeScript | Public |
| **certichain** | Decentralized protocol for issuing & verifying secure, fraud-proof skills certificates on a blockchain | Solidity | Public |
| **headless-html-validator** | Node 20 microservice using headless Chrome (Puppeteer) to load HTML, capture console/network/runtime errors, and return a JSON verdict; Prometheus metrics; Dockerfile included | JavaScript | Public |
| **canvas-lms** | *Fork* of Instructure’s open LMS | Ruby | Fork (upstream: Instructure) |
| **whisper.cpp** | *Fork* of OpenAI’s Whisper C/C++ implementation | C/C++ | Fork (upstream: ggerganov) |

See each repository’s README for detailed setup, configuration, and licensing.

---

## Using the Platform (API/Integrations)
1. **Get access** – email **hello@mindengage.ai** for an account and API key (org name & use case).
2. **Connect your LMS** – use `certichain-gateway` for LTI 1.3 events → credential issuance on **CertiChain**.
3. **Validate content at build/deploy** – run `headless-html-validator` in CI/CD to gate broken embeds/scripts.
4. **Publish** – export from MindEngage to Google Classroom/Forms or portable HTML bundles per Docs.

---

## Contributing
We welcome issues and PRs for **public repos only** (above). For platform feature requests, open an issue in the relevant public repo or email us.

- Please see each repo’s `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, and `SECURITY.md` (if present).

---

## Licensing
This organization contains **mixed licenses**. Refer to each repository’s `LICENSE`.  
MindEngage core services remain **proprietary** and are governed by our Terms of Service and EULA.

© 2025 MindEngage. All rights reserved. Trademarks belong to their respective owners.
