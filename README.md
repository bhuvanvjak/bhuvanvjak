# Hi, I'm Bhuvan

I build LLM applications for people who will never read a line of code — finance analysts, non-technical stakeholders, anyone who just needs the answer, not the pipeline. That constraint is what I find interesting about this work: a model that hallucinates one number is worse than useless in finance, so most of my engineering time goes into making AI outputs boring, predictable, and correct — not into making demos impressive.

Currently: shipping a local-LLM finance agent in production at RealPage. Before that: debugging generative vision pipelines at Tech Mahindra's Makers Lab.

📍 Hyderabad, India · [vukkemBhuvan@gmail.com](mailto:bhuvanesh9139@gmail.com)

---

## What I'm doing right now

- 🔧 Hardening an EPM finance agent through its 8th prompt-iteration cycle — chasing down the last few formatting edge cases before full production handoff
- 📚 Teaching myself RAG properly: building an "Ask My Resume" bot with sentence-transformers + Chroma + Groq, since every JD I read wants this and I don't want to fake it
- 🧠 Next up: LangGraph and cloud deployment, once the RAG basics are solid

---

## Featured Projects

### 🧾 EPM Financial Summary Agent
The problem: financial data can't touch the cloud, so ChatGPT/Copilot were off-limits, and an analyst was hand-writing the same commentary from scratch twice a month.

The build: a fully local LLM agent (Mistral 7B via LM Studio) that reads a Flash Deck Excel and writes the commentary itself — on-device, zero external calls.

The hard part wasn't the LLM call, it was everything around it: the full workbook blew the context window at 3M tokens, so I built a surgical extractor that pulls only the ~50 cells that matter (~400 tokens). And I stopped asking the model to do math entirely — every number is pre-formatted in code before the LLM ever sees it, which is the actual fix for hallucination, not a longer prompt.

**Result:** 2–3 hours of manual work → one click, under a minute. In active production use.
`React` `SheetJS` `Mistral 7B` `LM Studio`

### 🗣️ NL → SQL Finance Agent
Non-finance teams kept pinging the FP&A team for basic number lookups. Built a tool-calling agent (Qwen 13B) that lets anyone ask a plain-English question and get back a real, database-verified answer — no SQL required on either end.
`Qwen 13B` `Tool-calling` `Structured outputs`

### 📊 Revenue Data Extraction Pipeline
360 revenue centres, one Excel file each, one analyst doing it by hand. Wrote a pandas/glob/openpyxl pipeline that walks all 360 automatically.
**Result:** 2-week manual extract → 2 days.
`Python` `pandas` `openpyxl`

### [🧠 Gender Classification with CLIP](https://github.com/bhuvanvjak/gender-classification-with-CLIP)
Used CLIP as a frozen feature extractor with a custom Keras classifier on top — then spent more time on failure analysis (occlusion, lighting, pose) than on the model itself, because that's usually where the real accuracy gains hide.
`PyTorch` `TensorFlow/Keras` `OpenAI CLIP`

### [🎓 University Recommendation System](https://github.com/bhuvanvjak/CollegeRecommendationSystem) · [Live Demo](https://collegerecommendationsystem-1.onrender.com/)
End-to-end ML app, deployed — not just a notebook. Preprocessing through Flask deployment, with model selection driven by actual comparative evaluation rather than picking the first thing that worked.
`Python` `Flask` `Scikit-learn`

---

## Technical Skills

**Languages:** Python, JavaScript, SQL, Java, C
**AI / LLMs:** Mistral 7B, Qwen 13B, Groq API, OpenAI CLIP, Stable Diffusion, ControlNet, HuggingFace Transformers
**AI Frameworks:** LangChain (basic), LM Studio, prompt engineering, tool-calling agents, structured outputs
**ML:** PyTorch, TensorFlow/Keras, Scikit-learn
**Frontend/Backend:** React, SheetJS, Flask, FastAPI (familiar), REST APIs
**Data:** pandas, NumPy, openpyxl, ETL pipelines
**Tools:** Git, GitHub, Postman, Power BI

*Currently expanding into RAG pipelines, vector databases, LangGraph, and cloud deployment.*

---

## GitHub Activity

![Bhuvan's GitHub Stats](https://github-readme-stats.vercel.app/api?username=bhuvanvjak&show_icons=true&theme=default&hide_border=true&count_private=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=bhuvanvjak&layout=compact&theme=default&hide_border=true)

---

[GitHub](https://github.com/bhuvanvjak) · [Email](mailto:vukkemBhuvan@gmail.com)
