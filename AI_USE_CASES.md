# AI Use Cases (2026) — Waiter Copilot

## Agentic upgrade
- **Voice → structured order** — Whisper / Web Speech → Claude with JSON-schema output
- **Allergen RAG** — LlamaIndex over menu + ingredient database; cite source
- **Kitchen ETA** — Gemini long-context regression over kitchen-load + order history
- **Upsell suggester** — Claude Sonnet over historical attach-rate data
- **POS write-back** — Square / Toast MCP

## Stack (free/OSS)
- **ASR:** Whisper, Faster-Whisper, Web Speech API
- **LLMs:** Claude Sonnet 4.6, Gemini 2.x (ETA forecasting with long-context)
- **RAG:** LlamaIndex + Qdrant
- **MCP:** Square, Toast, Stripe
- **Eval:** Promptfoo on voice → JSON-order accuracy

## Prompt (voice → order)
```
SYSTEM: Convert the spoken order to JSON.
Schema: [{item_id, qty, modifiers, notes}].
- Match item names case-insensitively against the provided menu.
- If ambiguous, return clarification_question instead of guessing.
- Never invent items.
```

## Limitations
Square/Toast MCP need merchant accounts. Web Speech is browser-only; Whisper local needs a server.
