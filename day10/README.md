# 🧠 Building Agentic AI Applications — AI Frontier Day 10

> **Session by Mr. K. Akshay Kumar** · Python & AI App Dev, Kovan Labs
> CIT Summer Internship "AI Frontier" · 29 May 2026 · 1:30 PM – 4:30 PM

We assemble a *mind*, one part at a time, and end up with **Wanderlust AI** — a travel agent that plans a real trip from **Coimbatore to Coorg**, using the Google GenAI SDK and a teaser of Google ADK.

**Brain → Senses → Hands → Will → Team → Framework.**

---

## 🔗 Quick links

| | |
|--|--|
| 🎞 **Slides** | [day10/slides.html](https://akshaykumar-1729.github.io/ai-frontier-python/day10/slides.html) |
| 📋 **All snippets** | [day10/](https://akshaykumar-1729.github.io/ai-frontier-python/day10/) |
| 📓 **Colab notebook** | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AkshayKumar-1729/ai-frontier-python/blob/main/day10/notebook/session_notebook.ipynb) |

---

## ⚙️ One-time Colab setup

1. Get a free key at **[aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)**.
2. In Colab's left sidebar → **🔑 Secrets** → add a secret named `GOOGLE_API_KEY`, paste your key, toggle **Notebook access** ON.
3. Run **Snippet 0** first. The GenAI SDK is light — **no restart needed**.

> **`RESOURCE_EXHAUSTED`?** That's just the free-tier quota. Wait a few seconds and re-run the cell — it is **not** a bug in your code.

> **Snippet 7 (Google ADK)** is the one heavy install. If its import errors, do **Runtime → Restart session**, re-run Snippet 0, then the ADK cell.

We use **two models on purpose**: plain text runs on the fast/cheap `gemini-3.1-flash-lite`; the live-search beats (Hands, Team, ADK) run on `gemini-2.5-flash`.

---

## 📦 What's in the notebook

| # | Body part | Snippet | What it does |
|---|-----------|---------|-------------|
| 0 | ⚙️ Setup    | Warm up the engine | Install SDK, read key, define models, smoke test |
| 1 | 🧠 Brain    | Naive prompt | Plain ask → generic guidebook answer |
| 2 | 🧠 Brain    | Persona | Kodava-guide persona + constraints → opinionated, alive |
| 3 | 👁 Senses   | Multimodal | Hand Gemini a photo — it sees and suggests |
| 4 | ✋ Hands    | Google Search | Grounded live-web answer **+ the real source URLs** |
| 5 | ⚙️ Will     | ReAct loop | The model decides to call **your** Python function |
| 6 | 🤝 Team     | Parallel agents | Two streaming specialists → manager synthesis (the hero) |
| 7 | 🏗 Framework| Google ADK | Declare an agent, let the framework run the loop |
| 8 | 🔥 Bonus    | Chain-of-thought | "Think step by step" makes it self-correct |
| 9 | 🔥 Bonus    | RAG | Embeddings give the agent private memory |

---

## 📚 Sources & further reading

- [Gemini API docs](https://ai.google.dev/gemini-api/docs) — the Google GenAI SDK
- [Text generation](https://ai.google.dev/gemini-api/docs/text-generation) · [Vision](https://ai.google.dev/gemini-api/docs/vision) · [Embeddings](https://ai.google.dev/gemini-api/docs/embeddings)
- [Grounding with Google Search](https://ai.google.dev/gemini-api/docs/google-search)
- [Function calling](https://ai.google.dev/gemini-api/docs/function-calling)
- [ReAct: Reasoning + Acting (Yao et al., 2022)](https://arxiv.org/abs/2210.03629)
- [Google ADK (Agent Development Kit)](https://google.github.io/adk-docs/)

---

*Built with Google Colab · Slides and snippet site hosted on GitHub Pages.*
