# Ansh Kumar Singh

**AI Engineer — building with LLMs, and rebuilding the engineering underneath.**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anshks)
[![Gmail](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:anshkumarsingh107@gmail.com)

---

## About

I work on the Rapid Build Team at Tata Consultancy Services, turning enterprise client use cases into working LLM systems — document extraction, schema-enforced validation, approval workflows — for clients in banking, government, and real estate.

A lot of that delivery happened with AI coding tools. So I started building things the other way: from scratch, with code generation switched off, measuring what I claim. The repositories here are the result. They're small on purpose, and every number in them comes from a harness I wrote.

**Currently:** finishing a Graph RAG pipeline, and working through DSA daily.

---

## Projects

### RAG Pipeline from Scratch &nbsp;·&nbsp; [repo](https://github.com/Ansh-66)

`Python` `NumPy` `Gemini API`

Retrieval pipeline built end to end with AI code generation disabled — chunking, embeddings, cosine-similarity retrieval written directly in NumPy, LLM reranking, and grounded generation.

- Diagnosed an inert reranking stage: hit@1 came back identical to the no-rerank baseline, because a prompt that didn't enforce a full permutation made every call fall back silently to cosine order.
- Fixing the prompt contract took hit@1 from 13/17 to 17/17 on a 17-question labelled set over a 6-chunk corpus.
- Includes the hit@k evaluation harness the numbers come from.

### Insurance Graph RAG &nbsp;·&nbsp; [repo](https://github.com/Ansh-66/Insurance-Graph-RAG) &nbsp;·&nbsp; *in progress*

`Python` `Pydantic` `Groq` `sentence-transformers`

Entity-centric graph retrieval over Indian insurance-sector news, for questions that need evidence from more than one article. LLM relation extraction, entity resolution, and two-hop traversal with cited answers.

Being evaluated three ways — no context, vector top-k, and graph traversal — to test whether traversal actually beats vector retrieval on multi-hop questions. Results go here when the comparison is done.

---

## Experience

**AI Engineer — AI & Service Transformations, Tata Consultancy Services** *(Jan 2025 – present)*

- Delivered LLM document-processing proof-of-concepts for three enterprise clients: a loan and policy onboarding system for an Indian private-sector bank, a driver-licensing document validator for a UK transport authority, and a conversational intake agent for a Gulf megaproject developer.
- Facilitated AI enablement sessions for executive leadership at two international enterprises — 4 sessions, 35–40 board members and senior executives each — including a live multi-agent demo I built and presented.

---

## Tech

**Languages** · Python · JavaScript · SQL · HTML/CSS

**Building with LLMs** · Gemini, OpenAI and Groq APIs · prompt engineering · schema-enforced structured outputs · RAG (chunking, embeddings, retrieval, reranking) · retrieval evaluation (hit@k)

**Libraries & tools** · NumPy · Pydantic · sentence-transformers · Git · SQLite · Ollama

**Used in client and team delivery** · FastAPI · SQLAlchemy · LangChain · React

---

## Certifications

Databricks Certified Generative AI Engineer Associate · Databricks Certified Machine Learning Associate · Claude Certified Developer – Foundations (Anthropic) — all Sep 2026

---

## Education

**B.E. Electronics & Communication** — The National Institute of Engineering, Mysore (2020–2024)

---

📍 Pune, India · open to relocation and remote
