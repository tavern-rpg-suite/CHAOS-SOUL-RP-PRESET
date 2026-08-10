# 📝 CHAOS & SOUL — UNIVERSAL RP PRESET

A flexible, model-agnostic instruction set for immersive, character-driven roleplay: natural pacing, rich sensory detail, consistent logic — and a layered toggle system that scales from heavy budget models up to top-tier ones. 💕

**Version 1.0.2**

---

## 🔗 Integration

Works flawlessly as the narrative engine for the **Tavern RPG Suite**. Pair it with the RPG Map Engine, Inventory, and Status Bar for the ultimate text-based RPG experience.

## 📦 Install

1. Download the `CHAOS & SOUL RP PRESET.json` file from this repository.
2. Open SillyTavern.
3. Go to the **Chat Completion Presets**.
4. Click **Import** and select the JSON file.
5. Apply the preset and enjoy a smarter, more dynamic roleplay experience!

## ✅ Tested on
· DeepSeek-V4 (Temperature 1,00) 
· DeepSeek-flash (Venice) (Temperature 1,00) 
· Nemotron-3 Super (Temperature 1,00)
· Gemini-2.5-flash-lite (Temperature 2,00)
· Gemini 2.5 Pro (Temperature 2,00)
· Gemini 3.1 Pro-preview (Temperature 2,00)
· Gemini 3.5 Flash (Temperature 2,00)
· Claude-Haiku-4.5 (Temperature 2,00)
· Grok 4 (Temperature 1,00)
· Kimi K2.6 (Temperature 1,00)
· MiniMax M2.5 - M2.7 (Temperature 1,00)
· Qwen 3.6 Plus (Temperature 1,00)
· Gemma 4 31b (Temperature 2,00)
· Trinity Large Preview (Temperature 1,00)
· Mistral Large 3 (Temperature 1,00)
· Free Models Router (Temperature 0,85)
(Best with 100k+ context.)


## 🎛️ TOGGLE GUIDE — what each switch does


🟢 ALWAYS ON — the engine. Leave these.
🧩 Main System Prompt · 📚 Enhance Definitions · 🥝 CORE RULES · 🤝 NPC GENERAL RULES · 🫀 PHYSICAL REALISM · 👁️‍🗨️ POV & ANTI RECAP · 🔊 NPC SPOKEN DIALOGUE · 🌐 WORLD RULES · 🎭 PLOT & IMMERSION · 📖 NARRATIVE EXECUTION · ♟️ ANTI 5D CHESS · 💬 RESPONSE CONFIGURATION · 🔄 ENTRY ROTATION · 🧠 EMOTIONAL DEPTH · ✍️ WRITING RULES · 🫂 CHARACTER AUTONOMY & PERSONAL REGARD · 🚀 MICRO-CONTINUITY · 💫 GEMINI VIBE · ✨ THIRD PERSON ONLY

🔘 OPTIONAL — flip per model / per scene.

⛓️‍💥 Jailbreak Prompt — [DEFAULT: ON] Compact "fiction mode" frame that stops stubborn/strict models from refusing or breaking character. Turn ON only if a model refuses or lectures mid-scene.

🤝 Commitment + ✅ Confirmation (handshake) — [DEFAULT: ON] A two-part injection (a fake prior assistant "oath" + a fake user "format check") that makes the model treat compliance as already-agreed and treats any refusal/softening as a mere FORMAT error. This is the heavy artillery for weak/strict models. TURN OFF on strong models — it makes their output wooden and formulaic. Use together with the Jailbreak.

🏛️ THREE PILLARS — [DEFAULT: ON] Forces every reply to use 2 of 3 layers (action+environment / dialogue+subtext / inner+sensory). Booster for weak models that write flat "talking heads." Strong models do this naturally — leave OFF to avoid over-describing.

🔥 NSFW SCENE++ — [DEFAULT: OFF] Detail booster for intimate scenes (slow pacing, foreplay, vivid sensory, no interruptions). Turn ON when a scene gets intimate, OFF afterward.

🛠️ RESPONSE TUNING — [DEFAULT: OFF] Pacing control: one major action per reply, no meta-asides, no repeated phrases. Turn ON if the model rushes or chains too much.

📏 RESPONSE CAP — [DEFAULT: OFF] Hard 250–300 token limit. Turn ON if replies get too long.

📌 SMOOTH PROSE — [DEFAULT: OFF] Fixes clunky free routers (removes "A pause."/"A beat." tics, overused intensifiers). OFF for clean models (Mistral, Kimi).


## 🍳 RECIPES — when to enable what


🪶 WEAK / STRICT MODELS (DeepSeek-flash, budget & free routers)
Max crutches. ON: 🧠 CoT, ⛓️ Jailbreak, 🤝+✅ Handshake, 🏛️ Three Pillars. 📌 Smooth Prose for free OpenRouter routers. Add 🔥 NSFW SCENE++ during intimate scenes only. Enable <think> auto-parse. (This is how DeepSeek-flash-Venice was pushed to full, in-character, leading output.)

🦅 STRONG MODELS (Gemini, Grok, Kimi, Mistral Large, MiniMax)
Minimal. Keep the always-on core. OFF: 🤝+✅ Handshake (makes them wooden), 🏛️ Three Pillars (over-describe). ⛓️ Jailbreak only if that specific model actually refuses. Light or no prefill. Rule of thumb: smart model → fewer crutches.

🧠 LITE MODELS (Gemini-2.5-flash-lite) 
Max crutches. ON: 🧠 CoT, ⛓️ Jailbreak, 🤝+✅ Handshake, ✨ Narration: third person only, 📌 Smooth Prose, 🛠️ response tuning, 📏 length · balanced (default).

🔥 INTIMATE / NSFW SCENE
Turn ON 🔥 NSFW SCENE++ and the explicit prefill (+ ⛓️ Jailbreak / handshake if the model balks). Turn 🔥 OFF again afterward.

🌙 NORMAL / SFW SCENE
🔥 NSFW SCENE++ OFF; keep the prefill mild or cleared.

🩹 MODEL LOSING THE THREAD
Trim 🧠 CoT to the minimal 2-line version and/or disable the least-critical always-on blocks (📖 NARRATIVE EXECUTION, 💬 RESPONSE CONFIGURATION, 🧠 EMOTIONAL DEPTH). Less context = better coherence on small models.


Adjust temperature per model if needed (defaults (1,00) work for most). Enjoy! 💕

---
Built over time from bits and pieces I collected while learning. If you recognise your work here, tell me and I'll credit you properly.

