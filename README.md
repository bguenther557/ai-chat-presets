# ai-chat-presets

## Disclaimer / Liability Notice

### No Warranty

These AI presets are provided **"AS IS"** without warranty of any kind, either express or implied, including but not limited to warranties of merchantability, fitness for a particular purpose, or non-infringement. The author makes no guarantee regarding the accuracy, reliability, completeness, or effectiveness of any preset contained in this repository.

### Limitation of Liability

To the maximum extent permitted by applicable law, in no event shall the author or contributors be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including but not limited to: procurement of substitute services; loss of data, revenue, or profits; or business interruption) arising in any way out of the use of these presets, even if advised of the possibility of such damage.

### Use at Your Own Risk

Users are solely responsible for:
- Testing presets in their specific environment before production use
- Ensuring compliance with applicable laws and regulations
- Verifying that outputs generated using these presets meet their requirements
- Any consequences arising from the use or misuse of these materials

### AI-Specific Considerations

AI model outputs are non-deterministic and may vary. Results depend on factors including model version, temperature settings, context, and external data sources beyond the control of this repository.

---

## Description

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

