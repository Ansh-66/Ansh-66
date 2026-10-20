# Ansh Kumar Singh

**AI Engineer — building with LLMs, and rebuilding the engineering underneath.**

[![Portfolio](https://img.shields.io/badge/Portfolio-222222?style=for-the-badge&logo=githubpages&logoColor=white)](https://ansh-66.github.io/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anshks)
[![Gmail](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:anshkumarsingh107@gmail.com)

---

## About

I build LLM systems for a living: document extraction, schema-enforced validation, retrieval, and grounded analytics where the numbers come from SQL and the model only writes the prose.

The projects here are where I go deeper on the engineering underneath that work. They're small on purpose, they measure what they claim, and every number in them comes from an evaluation harness in the repo. The RAG pipeline was written with code generation switched off.

**Currently:** measuring when a team of agents beats a single agent, on the Graph RAG knowledge base; working through DSA daily.

---

## Projects

### GoodFoods Reservation Agent &nbsp;·&nbsp; [repo](https://github.com/Ansh-66/goodfoods-agent) &nbsp;·&nbsp; [demo video](https://drive.google.com/file/d/19X58cKDnBxULvZTbs0d39nogYVOV5TLf/view)

`Python` `MCP` `Groq` `Sarvam AI`

Conversational booking agent for a 75-outlet restaurant chain, built without an agent framework. The tool loop is my own; eight tools sit behind an MCP server; the model is gpt-oss-20b on Groq; and Sarvam handles voice in 11 languages.

- Writes are gated in code, not in the prompt: no booking, change or cancellation goes through until the guest confirms. When an outlet is full, the agent offers another time or a nearby outlet instead of losing the booking.
- A 16-journey evaluation checks tool choice, arguments and end state. Fixes driven by its failures raised case success from 11/16 to 13/16 and tool selection from 17/22 to 20/22.
- The prompt-injection journey is still marked as a fail in the harness, though the outcome was safe: nothing was written, and the agent asked the guest to confirm. The harness is strict on purpose.

### RAG Pipeline from Scratch &nbsp;·&nbsp; [repo](https://github.com/Ansh-66/rag-from-scratch)

`Python` `NumPy` `Gemini API`

Retrieval pipeline built end to end with AI code generation disabled — chunking, embeddings, cosine-similarity retrieval written directly in NumPy, LLM reranking, and grounded generation.

- Diagnosed an inert reranking stage: hit@1 came back identical to the no-rerank baseline, because a prompt that didn't enforce a full permutation made every call fall back silently to cosine order.
- Fixing the prompt contract took hit@1 from 13/17 to 17/17 on a 17-question labelled set over a 6-chunk corpus.
- Includes the hit@k evaluation harness the numbers come from.

### Insurance Graph RAG &nbsp;·&nbsp; [repo](https://github.com/Ansh-66/Insurance-Graph-RAG)

`Python` `Pydantic` `Groq` `sentence-transformers`

Entity-centric graph retrieval over 110 Indian insurance-sector news articles, for questions whose answer needs facts from more than one article. LLM relation extraction with deal status and ownership intervals, entity resolution, two-hop traversal, and cited answers.

- Evaluated three ways on 11 questions: graph RAG answered 10/11, vector RAG 9/11, and the model alone 3/11. On cross-document multi-hop questions, graph 4/4 against vector 3/4. One run each, so a direction rather than a proof.
- Vector won the one question whose article was lost during extraction. Without retrieval, the model gave confident, specific wrong answers, including an acquisition that never happened.
- Traced a weakly supported answer to retrieval rather than the model: one heavily reported deal filled 14 of 30 context slots and crowded out the second-hop evidence. Round-robin evidence assembly fixed it.

### Single vs Multi-Agent &nbsp;·&nbsp; [repo](https://github.com/Ansh-66/single-vs-multi-agent) &nbsp;·&nbsp; *in progress*

`Python` `Groq` `tool calling`

A measured comparison on the Graph RAG knowledge base: when does a team of agents beat one agent with the same tools, and what does it cost? Three designs share one model (gpt-oss-120b, temperature 0), the same three retrieval tools and the same answer rules: a single tool-calling agent, a planner with worker agents, and the same plus a verifier. They will be scored on accuracy, grounding, tokens, LLM calls and a failure taxonomy, over 12 to 15 questions written before the multi-agent designs exist. The agent loop is written by hand, with no agent framework. Results are not in yet.

- Measured tool-result sizes before choosing any format. Returned as raw JSON, one graph lookup on a hub company came to about 17,000 tokens, and every later call in the question resends it. Compact text, one evidence sentence per edge, an optional second-company filter and a 6,000-character cap bring the worst case to about 1,500 tokens.
- A single tool round trip showed that 90% of the model's output tokens were hidden reasoning, and that a prompt mentioning tools the request did not include made the model invent one.

---

## Tech

**Languages** · Python · JavaScript · SQL · HTML/CSS

**Building with LLMs** · Gemini, OpenAI, Groq and Sarvam APIs · MCP · tool calling · agent loops without frameworks · prompt engineering · schema-enforced structured outputs · RAG (chunking, embeddings, retrieval, reranking) · Graph RAG (relation extraction, entity resolution, graph traversal) · evaluation (hit@k, journey-based agent evals, test suites, multi-arm comparisons)

**Libraries & tools** · NumPy · Pydantic · scikit-learn · sentence-transformers · Git · SQLite · DuckDB · Ollama

**Used in client and team delivery** · FastAPI · SQLAlchemy · LangChain · React

---

## Certifications

Databricks Certified Generative AI Engineer Associate · Databricks Certified Machine Learning Associate · Claude Certified Developer – Foundations (Anthropic) — all Sep 2026

---

## Education

**B.E. Electronics & Communication** — The National Institute of Engineering, Mysore (2020–2024)

---

📍 Pune, India · open to relocation and remote