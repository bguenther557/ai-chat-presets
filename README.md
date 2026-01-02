# ai-chat-presets

This repository contains small, copy/paste “preset prompts” you can store in an AI chat app. Depending on which app you use, these care called "preset" or "slash command". Each preset is designed for one narrowly defined job (logic check, grammar fix, synonyms, style), with clear input/output rules.

## How to use a preset (step by step)

1. Pick a preset file in this repo (for example `Logic Preset`).
2. Open it and copy the full text.
3. In your AI chatbot interface, create a new preset (or "slash command"):
   - Some tools have dedicated preset management (e.g., AnythingLLM)
   - Most tools require you to "store" the preset as a custom memory instruction ("Hey ChatGPT, remember <<enter preset prompt here>> when I type <<<enter preset title here>>>!")
4. Name the preset after its header (for example `/logic`) so you can quickly pick it later.
5. When you want to use it, activate/select the preset and send your content as the user message, filling in any placeholders like `[INPUT TEXT: …]`.
6. Check the output against the preset’s rules. If needed, resend with more context (e.g., the full section instead of a single sentence).

## Example: using `Logic Preset`

### 1) Save the preset
- Create a new preset named `/logic`.
- Paste the full contents of `Logic Preset` into your tool’s System/Instructions field.

### 2) Run it on your text
Send your text as the next user message. For example:

"Our product reduced costs by 50% for all customers. We ran a pilot with three users and everyone agreed it was faster."

### 3) What you should get back
The preset asks the model to output a table (in the same language as your input) with these columns:
- Sequential numbering
- Category(ies)
- Verbatim quote
- Rationale
- Improvement suggestion (only when it doesn’t require guessing missing facts)

