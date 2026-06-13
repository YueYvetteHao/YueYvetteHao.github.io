---
title: "To Nom or Not to Nom: Tracking Feline Pickiness"
date: 2026-06-12
categories:
  - projects
tags:
  - nextjs
  - supabase
  - side-project
slug: nom-or-not
thumbnailImage: images/luna.png
---

You know the drill. You crack open a fancy new flavor, set the bowl down all hopeful, and your cat strolls over, takes one sniff, gives you a look, and walks off. Hit or snub? No clue. And two weeks later? Absolutely no memory of which foods landed and which got the cold shoulder. So I built [Nom or Not](https://nom-or-not.vercel.app/) to stop guessing and start keeping receipts.

<!--more-->

It's simple to use. Log a feeding — which cat, which food, and the verdict: 😋 ate, 😐 sniffed, or 🙅 refused. Do that for a while and the app turns it into something useful: each cat's favorite flavors, the foods that get rejected most, eating trends over time, and the crown jewel — a **Picky Meter** that ranks who's the fussiest in the house. (My household already knew. Now we have proof.)

The stack is small and modern: Next.js 16, React 19, and Tailwind on the front, deployed on Vercel. Data lives in Supabase (hosted Postgres). My favorite part is that there's no separate backend — the analysis runs inside the database, and the app just plots the results. Row-Level Security scopes every table to its owner, so privacy is enforced at the data layer.

Want to snoop without signing up? There's a no-login [example dashboard](https://nom-or-not.vercel.app/example) loaded with sample data. There's also multi-cat logging (one form, whole household) and CSV import if you're coming from a spreadsheet.

It started with one petty little question — *who's the pickiest eater in this house?* — and now I have the answer. Spoiler: it's Luna, the floof staring at you from the top of this post, pickiest of them all. 👑
