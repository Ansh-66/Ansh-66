# Ansh Kumar Singh

**AI Engineer — building with LLMs, and rebuilding the engineering underneath.**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anshks)
[![Gmail](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:anshkumarsingh107@gmail.com)

---

## About

I build LLM systems for a living — document extraction, schema-enforced validation, retrieval — and I'm deepening the engineering underneath that work.

A lot of what I've shipped was built with AI coding tools. So I started building things the other way: from scratch, measuring what I claim. The RAG pipeline was built with code generation switched off. In the Graph RAG project I designed the system and wrote the retrieval core myself, with an AI assistant handling plumbing. The repositories are small on purpose, and every number in them comes from an evaluation harness in the repo.

**Currently:** building a frontend for the Graph RAG project, and working through DSA daily.

---

## Projects

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

---

## Tech

**Languages** · Python · JavaScript · SQL · HTML/CSS

**Building with LLMs** · Gemini, OpenAI and Groq APIs · prompt engineering · schema-enforced structured outputs · RAG (chunking, embeddings, retrieval, reranking) · Graph RAG (relation extraction, entity resolution, graph traversal) · evaluation (hit@k, test suites, multi-arm comparisons)

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