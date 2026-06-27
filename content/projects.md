---
title: "Projects"
showTags: false
showDate: false
---

## Semblance

A multi-agent system that semantically compares GSEA enrichment results — matching biological *programs* rather than overlapping gene-set names. Four LLM agents (preprocessor, orchestrator, interpreter, verifier) act as an **MCP** client calling a deterministic **MCP** server that owns all the math, so the model interprets and verifies but never computes the similarity itself. It embeds pathways with a biomedical language model, adds RAG-grounded cross-ontology explanations, and re-checks every claim against the engine's numbers as a hallucination guard. Built with Gradio, FastMCP, and Groq on Hugging Face Spaces.
👉 [Try it live](https://huggingface.co/spaces/yueyvettehao/Semblance)

## Nom or Not

A full-stack web app for tracking whether your cats actually eat their food — log each feeding (😋 ate / 😐 sniffed / 🙅 refused) and turn it into insights like favorite flavors, most-refused foods, eating trends, and a Picky Meter ranking. There's no separate backend: the analysis runs inside the database and the app just plots the results, with Row-Level Security enforcing privacy per user at the data layer. It also supports multi-cat logging and CSV import. Built with Next.js 16, React 19, and Tailwind on Vercel, backed by Supabase (hosted Postgres).
👉 [Give it a spin](https://nom-or-not.vercel.app/) · [See the example dashboard](https://nom-or-not.vercel.app/example) · [Read the blog post]({{< ref "/posts/nom-or-not" >}})


## Board Game Finder

A conversational board game recommender powered by a Retrieval-Augmented Generation (RAG) system: it embeds your query, runs a similarity search over 20,000+ BoardGameGeek titles in Pinecone, then uses Llama 3.1 8B (via Groq) to pick the best matches and explain why. Built with LangChain and Gradio on Hugging Face Spaces.
👉 [Try it live](https://huggingface.co/spaces/yueyvettehao/BoardGameFinder)

## Chinese Folk Music

Exploring what gives Chinese folk music its regional "accent." Most of it is built on the same pentatonic scale (宫商角徵羽), yet northern and southern tunes can sound worlds apart — so this project quantifies the melody itself, measuring the semitone distance between every consecutive pair of notes and visualizing it as a color-coded melodic contour and an interval-distribution histogram. The headline finding: Northern Shaanxi (陕北) tunes spring oscillating wide leaps (up–down–up–down) for a bold, far-carrying sound, while Jiangnan (江南) tunes stay smooth and stepwise — gentle and delicate — with Shandong (山东) sitting in between.
👉 [Explore the interactive comparison](https://yueyvettehao.github.io/ChineseFolkMusic/) · Try the [jianpu 简谱 player]({{< ref "/posts/jianpu-player" >}}), a proof-of-concept that reads numbered notation and plays it back in the browser.

[Variations on a Theme of Folk Songs from Shaanxi](https://youtu.be/zjbXUn2w-Rw?si=zY8wAVjMbBM1Mpfh).

## Beso Elite Music Academy

Website for Ms. Sophia's piano studio.
👉 [Visit the site](https://www.besoelitemusic.com/)
