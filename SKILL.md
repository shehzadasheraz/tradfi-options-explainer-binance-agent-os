# TradFi & Options Explainer — Binance Agent OS

A Claude skill that teaches TradFi Perpetuals and Options concepts, pulls live TradFi Perpetual market data from Binance Agent OS, and runs an interactive timed quiz to test what the user has learned.

Built on Binance Agent OS (Binance's MCP server for AI applications).

## The problem

Binance TradFi Perpetuals and Commodity Options let users trade tokenized equities, ETFs, and commodities the same way they trade crypto — but most users don't know how these products actually work. Expiry rules, exercise style, funding mechanics, and weekend pricing modes for TradFi Perps are all different from what crypto traders are used to, and there's no single place that explains it while also showing live data.

## How it works

This skill operates in three modes, and a user can move between them freely in conversation.

### 1. Explain mode
When a user asks a concept question (what is a strike price, how does funding rate work), answer clearly and concisely using the knowledge base in references/knowledge-base.md. Use plain language and a short example, not just the definition.

### 2. Live data mode
When a user asks about current prices for a TradFi Perpetual (what's AAPL perpetual trading at, check NVDA TradFi perp price), pull live kline data via Binance Agent OS using contractType TRADIFI_PERPETUAL on the relevant pair (for example AAPLUSDT, NVDAUSDT, TSLAUSDT). Report the latest close price, and the recent high and low if useful context. Be upfront if a requested symbol isn't a supported TradFi Perp pair.

### 3. Quiz mode
When a user asks to start a quiz or test me:
1. Pick questions from the knowledge base's Q&A bank.
2. Present one question at a time with 4 options.
3. Wait for the user's answer.
4. Reveal whether it was correct, show the correct answer if they got it wrong, and award XP.
5. Move to the next question.
6. At the end, report total XP and score out of total questions.

Scoring: correct answers earn XP, up to 1000 XP scaled down the longer it takes to answer. Wrong or skipped answers earn 0 XP.

Interactive version: for a real timed experience with a genuine 15-second countdown, generate and share tradfi-quiz.html, a self-contained interactive quiz with a visual countdown ring and live XP counter. This is the recommended way to run the quiz when the user wants the full timed experience, since a text chat alone cannot enforce a real countdown.

## Why this matters

TradFi Perps and Options are new enough that most users approach them with crypto-native assumptions that don't apply. Pairing explanation with live data and a scored quiz turns passive reading into active, verifiable learning.

## Structure

This repository contains SKILL.md (core workflow logic, this file), LICENSE, tradfi-quiz.html (standalone interactive quiz with a real 15 second timer and XP), and a references folder containing knowledge-base.md (the full Q&A knowledge base used for Explain and Quiz modes).

## Requirements

A Claude.ai account with Code execution and file creation enabled in Settings, under Capabilities. The Binance Agent OS MCP connector connected to your account, for live price checks.

## Disclaimer

This skill is educational only. It does not provide financial advice, trade recommendations, or execute trades. Live price data shown is for informational context, not for trading decisions.
