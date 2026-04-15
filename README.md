# Raghav Sejpal

CSE (AI & ML) · VIT Vellore

Chairperson, IEEE Computer Society VIT

---
> **Trying to build things that leave impact.**
---

[Resume](https://drive.google.com/file/d/1WqCuKjGZyL_ktYiZ6uuPn6NnC5kVMxCs/view) &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/raghav-sejpal/) &nbsp;·&nbsp; sejpalraghav05@gmail.com

---

<picture>
  <source media="(prefers-color-scheme: dark)"
    srcset="https://raw.githubusercontent.com/Sejpal-Raghav/Sejpal-Raghav/output/github-contribution-grid-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)"
    srcset="https://raw.githubusercontent.com/Sejpal-Raghav/Sejpal-Raghav/output/github-contribution-grid-snake.svg" />
  <img alt="github contribution grid snake animation"
    src="https://raw.githubusercontent.com/Sejpal-Raghav/Sejpal-Raghav/output/github-contribution-grid-snake.svg" />
</picture>

---

## Recent Projects

<details>
<summary><strong>ValidateAI</strong> — AI Startup Idea Validator &nbsp;|&nbsp; <code>Next.js</code> <code>Gemini</code> <code>PostgreSQL</code></summary>

&nbsp;

Most startup validators give you a vibe check. ValidateAI gives you a structured report.

Built a full-stack platform that takes a startup idea and generates analysis across 7 dimensions: market sizing, competition landscape, monetization potential, risk factors, target audience, go-to-market, and overall viability. The whole thing runs on a 5-model Gemini fallback chain so users never hit a dead end even under high API demand.

Prompt design was the hard part. Vague inputs (like "I want to build an app") need to be caught before they produce hallucinated analysis, so I built vagueness detection with strict JSON enforcement before anything reaches the model. Rate limiting and prompt injection sanitization sit on top of that.

Output is stored in JSONB for schema-flexible retrieval, and users can export their report as a PDF.

`Next.js 16` `Google Gemini` `Neon (PostgreSQL)` `Tailwind CSS` `Framer Motion` `Vercel` `html2pdf`

[GitHub](https://github.com/Sejpal-Raghav/AI-startup-validator) &nbsp;·&nbsp; [Live](https://ai-startup-validator-ten.vercel.app/)

</details>

---

<details>
<summary><strong>TextOrigin</strong> — 3-Class Text Origin Classifier &nbsp;|&nbsp; <code>RoBERTa</code> <code>FastAPI</code> <code>T5</code></summary>

&nbsp;

Binary AI detectors (human vs AI) are easy to fool with a paraphrase. TextOrigin targets that gap with a third class: AI-paraphrased.

Fine-tuned RoBERTa-base on 15,000 samples with fp16 precision. To avoid depending on hand-labelled paraphrased data, I synthesized 5,000+ samples using a T5 paraphrasing model. On top of the transformer, I engineered 6 statistical features — GPT-2 perplexity, burstiness, entropy, AI phrase ratio, and more — that distinguish how humans and LLMs write differently at a structural level.

The model outputs a confidence score across all 3 classes with an explainability signal attached. Deployed as a FastAPI REST API and CLI supporting text, file, and JSON input modes with auto-generated Swagger docs.

`Python` `RoBERTa-base` `T5` `FastAPI` `Uvicorn` `scikit-learn` `NumPy` `Pandas`

[GitHub](https://github.com/Sejpal-Raghav/textorigin)

</details>

---

<details>
<summary><strong>Input Integrity Firewall</strong> — Offline Data Validation Engine &nbsp;|&nbsp; <code>.NET 8</code> <code>C#</code></summary>

&nbsp;

Data pipelines fail silently. By the time bad data reaches a model or a database, the damage is already done. This project is a deterministic offline validation layer that catches problems before they get that far.

Built in .NET 8 with zero external dependencies. Runs 5 detection checks across a 7-component modular architecture: schema validation, statistical drift detection, outlier flagging (beyond 3.0 z-score), variance comparison against a baseline (flags anything exceeding 25%), and type integrity checks.

Every input receives a 0-100 trust score bucketed into 3 tiers, with configurable penalty weights (20 per critical violation, 5 per warning). Output is a structured allow/block decision with a full audit trail.

`.NET 8` `C#` `JSON` `CSV Parsing` `Statistical Analysis`

[GitHub](https://github.com/Sejpal-Raghav/Input-Integrity-Firewall)

</details>

---

<details>
<summary><strong>Cryptography-ML</strong> — PRNG Classifier &nbsp;|&nbsp; <code>XGBoost</code> <code>scikit-learn</code> · IEEE paper in progress</summary>

&nbsp;

The standard way to test if a number generator is truly random is NIST SP 800-22, a suite of 15 statistical tests. The problem: those tests require long sequences to work. At short sequence lengths, they become statistically inoperable and produce unreliable results.

I built a classifier using XGBoost and Random Forest trained on 18 statistical features extracted from outputs of 8 different PRNG algorithms. The finding: ML classifiers correctly distinguish generator types at sequence lengths where NIST fails entirely. This has real implications for cryptographic auditing and embedded systems where only short outputs are available.

IEEE paper currently under review.

`Python` `XGBoost` `Random Forest` `scikit-learn` `Statistical Analysis` `NumPy`

[GitHub](https://github.com/Sejpal-Raghav/Cryptography-ML)

</details>

---

<details>
<summary><strong>LLMInsight</strong> — LLM Evaluation Framework &nbsp;|&nbsp; <code>Sentence Transformers</code> <code>Streamlit</code></summary>

&nbsp;

Prompt engineering without measurement is just guessing. LLMInsight is a framework for actually evaluating how different prompting strategies change model output quality.

Supports zero-shot, role-prompted, chain-of-thought, and few-shot templates. Scores outputs using semantic similarity via all-MiniLM-L6-v2 so you can compare across prompt styles quantitatively, not just by feel. Live on Hugging Face Spaces.

`Python` `Sentence Transformers` `all-MiniLM-L6-v2` `Streamlit` `Hugging Face Spaces`

[GitHub](https://github.com/Sejpal-Raghav/LLMINSIGHT) &nbsp;·&nbsp;

</details>

---

## Stack

<details>
<summary>Languages & Frameworks</summary>

&nbsp;

`C++` `Python` `Java` `JavaScript` `TypeScript` `C#` `Bash`

`Next.js` `React` `Node.js` `Express.js` `FastAPI` `.NET` `Tailwind CSS`

</details>

<details>
<summary>AI / LLM</summary>

&nbsp;

`RAG Pipelines` `LLM Evaluation` `Prompt Engineering` `Ollama` `GenAI` `PyTorch (basic)`
`Token Usage Analysis` `Response Quality Assessment` `Semantic Similarity`

</details>

<details>
<summary>Tools & Infra</summary>

&nbsp;

`PostgreSQL` `MySQL` `MongoDB` `Docker` `Git` `Linux` `AWS fundamentals` `CI/CD basics` `Postman`

</details>

---

## Research

Investigating whether RLVR-based reasoning fine-tuning degrades tool-grounding fidelity in LLM agents.
Targeting EMNLP 2026 / ACL Findings. Sits at the intersection of RL, NLP, and agent behavior.

---

## Leadership

**Chairperson — IEEE Computer Society, VIT**

250 members · Leading technical initiatives across domains

---

## Coursework

Machine Learning · Machine Vision · Reinforcement Learning · Operating Systems · Computer Networks · DSA · Design & Analysis of Algorithms

