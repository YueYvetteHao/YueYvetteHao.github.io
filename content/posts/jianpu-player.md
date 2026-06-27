---
title: "A Tiny Jianpu 简谱 Player in the Browser"
date: 2026-06-11
categories:
  - projects
tags:
  - javascript
  - web-audio
  - music
slug: jianpu-player
---

If you grew up learning music in China, you probably read *jianpu* (简谱) — numbered musical notation, where `1`–`7` stand in for do-re-mi instead of dots on a staff. It's compact, easy to scribble, and surprisingly fun to parse with code. So I built a little player that reads jianpu text, lays it out, and plays it back right in the browser.

{{< alert success >}}
**Update 6/27:** The full project is now live. Visit the [Chinese Folk Music project site](https://yueyvettehao.github.io/ChineseFolkMusic/) to see the regional melody-texture comparison — melodic contours, interval-distribution histograms, summary statistics, and interactive analyzers.
{{< /alert >}}

<!--more-->

This is a proof-of-concept demo for an ongoing project of mine exploring Chinese folk music, comparing tunes from different regions. No libraries, no audio files — just a small parser and the Web Audio API generating sine tones on the fly. Type a melody, pick a tempo and key, and hit play. Each note lights up as it sounds.

{{< jianpu >}}

## How it works

The parser walks the text one character at a time. A digit `1`–`7` starts a new note; a trailing `-` adds a beat to the note before it; `'` bumps it up an octave and `,` drops it down. That turns a string like `3-3561'1'65-565---` into a list of notes with pitch, octave, and duration.

Playback is just the Web Audio API: for each note I create an oscillator at the right frequency, wrap it in a short volume envelope so it doesn't click, and schedule it for the note's duration. The frequency comes from a base table (C4–B4), shifted by the chosen key and octave. A `setTimeout`-based loop walks the notes in tempo and toggles a highlight class so you can follow along.

The whole stack is refreshingly small: plain JavaScript does the parsing, the browser's built-in Web Audio API makes the sound (no audio files or MIDI library), and a little CSS handles the layout and the play-along highlight. It lives in a single Hugo shortcode, so it renders right here in the post — no separate page or app.

It's a small thing, but it scratches a specific itch: jianpu is everywhere in Chinese music education and almost nowhere on the web. Now I can paste a tune and hear it instantly.
