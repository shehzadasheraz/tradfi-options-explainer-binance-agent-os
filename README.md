# TradFi & Options Explainer — Binance Agent OS

A Claude skill that teaches TradFi Perpetuals and Options concepts, pulls live TradFi Perpetual prices from Binance Agent OS, and runs a scored, timed quiz to test what the user learned.

Built on Binance Agent OS (Binance's MCP server for AI applications).

## Installation

1. Download or clone this repo
2. Zip the tradfi-options-explainer-binance-agent-os folder (folder itself as the root of the zip)
3. In Claude.ai, go to Settings, then Customize, then Skills
4. Click the plus button, then "Create skill", then "Upload a skill"
5. Upload the zip file, then toggle the skill on

See SKILL.md for the full workflow logic and references/knowledge-base.md for the complete Q&A content bank.

## Three modes

Explain — ask any concept question:
"What is Theta in options?"

Live data — ask for current TradFi Perp prices:
"What's AAPL TradFi perpetual trading at right now?"

Quiz — test yourself with a scored, timed quiz:
"Start a TradFi & Options quiz"

The quiz can run conversationally, or as a fully interactive experience — open tradfi-quiz.html directly in a browser for a real 15-second countdown timer and live XP scoring.

## License

MIT — free to use, modify, and share.
