---
title: "Projects"
showTags: false
showDate: false
---

## Semblance

A multi-agent system that semantically compares GSEA enrichment results — matching biological *programs* rather than overlapping gene-set names. Four LLM agents (preprocessor, orchestrator, interpreter, verifier) act as an **MCP** client calling a deterministic **MCP** server that owns all the math, so the model interprets and verifies but never computes the similarity itself. It embeds pathways with a biomedical language model, adds RAG-grounded cross-ontology explanations, and re-checks every claim against the engine's numbers as a hallucination guard. Built with Gradio, FastMCP, and Groq on Hugging Face Spaces.
👉 [Try it live](https://huggingface.co/spaces/yueyvettehao/Semblance)

## Nom or Not

A web app for tracking whether your cats actually eat their food — log each feeding and turn it into insights like favorite flavors, most-refused foods, and a Picky Meter ranking.
👉 [Give it a spin](https://nom-or-not.vercel.app/) · [Read the blog post]({{< ref "/posts/nom-or-not" >}})


## BoardGameFinder

A conversational board game recommender powered by a Retrieval-Augmented Generation (RAG) system: it embeds your query, runs a similarity search over 20,000+ BoardGameGeek titles in Pinecone, then uses Llama 3.1 8B (via Groq) to pick the best matches and explain why. Built with LangChain and Gradio on Hugging Face Spaces.
👉 [Try it live](https://huggingface.co/spaces/yueyvettehao/BoardGameFinder)

## Chinese Folk Music

An ongoing project exploring Chinese folk music, comparing tunes from different regions. 👉 Try the [interactive jianpu player]({{< ref "/posts/jianpu-player" >}}), a proof-of-concept demo that reads numbered notation and plays it back in the browser.

[Variations on a Theme of Folk Songs from Shaanxi](https://youtu.be/zjbXUn2w-Rw?si=zY8wAVjMbBM1Mpfh).

## Beso Elite Music Academy

Website for Ms. Sophia's piano studio.
👉 [Visit the site](https://www.besoelitemusic.com/)
