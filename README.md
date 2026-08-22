# 🎭 Chaos & Soul — UNIVERSAL RP PRESET

<p align="center">
<img width="1536" height="1024" alt="fd754dbd-20de-419b-abf4-f61491d2ec32" src="https://github.com/user-attachments/assets/8dd06370-73b1-4f8b-906e-9713bdd7001f" />
</p>

<p align="center">
  <strong>🎭 Chaos & Soul</strong>
</p>

<p align="center">
  <strong>Download · Import · Play</strong><br>
  The preset is already configured. Just load it into SillyTavern and start your story.
</p>

---
A SillyTavern roleplay preset focused on **character autonomy, believable world behavior, and natural prose**.

Instead of teaching the model to simply “write beautifully”, Chaos & Soul focuses on making characters **behave like people**.

Characters have their own goals, opinions, boundaries and lives. They can disagree, lie, refuse, leave, change their minds or act without waiting for the player. NPCs continue living their lives outside the current scene.

The world also has **information boundaries**: characters only know what they could realistically perceive or learn. No mind-reading, wall-hearing, unexplained name recognition or solving mysteries the player has not revealed.

The result is roleplay that aims to feel **less like a chatbot and more like an unfolding story**.

---

## 🔧 Prompt Structure

The preset uses SillyTavern's injection positions to separate **long-term rules** from **generation-time reminders**.

Core world, character and behavior rules are placed higher in the prompt, while POV, pacing, continuity and execution rules are reinforced near the end of the context.

Some important rules appear in both locations: detailed at the top and as a short reminder near generation.

The preset also includes its own Regex scripts. They are designed to clean the generated prompt without modifying the original `.jsonl` chat history.

---
## ⚙️ What's Inside

### 🧱 Core

The main rules always remain active:

- **Main System Prompt** — You are the narrator and all characters; the player controls only themselves.
- 🥝 **CORE RULES** — Character autonomy, meaningful action in every response, and scenes that keep moving.
- 🤝 **NPC GENERAL · NPC DIALOGUE** — NPCs are independent people with their own goals, personalities, and voices.
- 🌐 **WORLD RULES** — The world continues without the player; secrets are discovered gradually.
- 🫀 **PHYSICAL REALISM** — Physics, anatomy, distance, positioning, and the limits of perception.
- ♟️ **ANTI 5D CHESS** — Information must be discovered through interaction, not magically obtained.
- 👁️‍🗨️ **POV & ANTI-RECAP · ANTI-ECHO** — Never write for the player or simply repeat their message.
- 🎭 **PLOT & IMMERSION** — New characters and developments appear naturally, not on a schedule.
- 🫂 **CHARACTER AUTONOMY** — Characters have lives of their own while still feeling like people sharing the scene.
- 🧠 **EMOTIONAL DEPTH** — Emotional carryover, contradictions, changing feelings, and the ability to refuse.
- ✍️ **WRITING RULES · GEMINI VIBE** — A balance of description and dialogue, sensory detail, and subtext.
- 📖 **NARRATIVE EXECUTION · RESPONSE CONFIG** — Avoids summary-like prose and depersonalizing metaphors.
- 🔄 **ENTRY ROTATION** — Varying ways to enter and open a scene.
- 🚀 **MICRO-CONTINUITY** — Keeps track of positions, objects, and ongoing physical states.
- ✨ **THIRD PERSON ONLY** — Strict third-person narration.

### 🔘 Optional Toggles

Enable only what you need:

- 📏 **LENGTH** — Short / Balanced / Long
- 🔥 **NSFW SCENE++** — additional pacing and detail for intimate scenes
- 🛠️ **RESPONSE TUNING** — limits the response to one major action
- 📌 **SMOOTH PROSE** — reduces repetitive phrasing and stylistic tics
- 🎲 **SCENE DRIVING FORCE** — introduces controlled scene variation
- ⚡ **GROUNDED COMPLICATION** — adds plausible complications to keep scenes moving
- 🌿 **NATURAL HUMAN PROSE** —  Already included by Tavern RPG Suite → [RPG Status Bar + Bonds](https://github.com/tavern-rpg-suite/RPG-Status-Bar-Bonds) when "Inject the natural-prose writing rules" is enabled. Leave this disabled to avoid duplication.

### 🧩 Generation Layer

Placed close to the end of the chat for stronger influence during generation:

- 🧠 **CoT / Think** — hidden planning before the response
- ⛓️ **Jailbreak** — additional framing for adult fictional roleplay
- 🤝 **Commitment + Confirmation** — helps stubborn models follow the preset

---

### 🧹 ANTI-SLOP REGEX

A built-in cleanup layer that removes common AI writing clichés, unwanted formatting, and repetitive phrasing from generated text.

It works in two places at once:

- 👁️ **Chat Display (`markdownOnly`)** — cleans what you see in the chat.
- 🧠 **Outgoing Prompt (`promptOnly`)** — cleans what is sent back to the model, so removed phrases do not become part of its conversation history and reinforce themselves.

Your original `.jsonl` chat file is **never modified**.  
Everything is reversible: disable a script and the original text appears again.

#### ⚙️ Cleanup Order

The scripts run in a fixed order because some replacements depend on earlier steps:

`P → T → A → B → C → D → Z`

- 🧽 **P — Pre-clean** — removes optional unwanted blocks.
- 🔤 **T — Typography** — normalises quotes, apostrophes, ellipses, etc.
- 🩹 **A — Personal Replacements** — applies custom replacements before sentence deletion.
- 🗑️ **B — Sentence Cleanup** — removes entire cliché sentences.
- 🔧 **C — In-Sentence Cleanup** — replaces unwanted phrases within sentences.
- 🚫 **D — Word Cleanup** — removes selected individual words.
- 🧼 **Z — Final Polish** — repairs punctuation and applies the remaining cleanup scripts.

If you add your own scripts, place them in the appropriate group rather than simply adding them to the end.

#### ⚠️ Global Regex Scripts

The cleanup order in SillyTavern is:

`Global → Preset → Scoped`

#### 🔬 Optional Scripts

Some cleanup rules are **disabled by default** because they can occasionally alter legitimate writing.

These include:

`B6 · B7 · C33 · C34 · C35 · D12 · D13 · D14 · D15 · D16 · D17 · D18`

They are best enabled individually and tested with your own characters.

#### 📝 A Few Notes

- **A2** changes `"A breath."` into a male-oriented line. For female POV, change `He` → `She` in the SillyTavern editor.
- **Group D** is intentionally case-sensitive, so words at the beginning of sentences are not accidentally altered.
- **Z1** fixes articles after replacements, such as `an pure` → `a pure`.

#### ✍️ What Regex Does *Not* Try to Fix

Regex is good at catching **specific, repeatable patterns**. It cannot reliably judge whether something is cliché based on context.

Things such as:

- rule-of-three phrasing;
- predator/prey metaphors;
- architectural metaphors;
- forced comparisons to weather or everyday objects;
- stacked adjectives;
- explaining the symbolic meaning of an action immediately after describing it;
- repetitive romantic gestures;
- animal-like sounds used for human characters.

These are handled by **📌 SMOOTH PROSE** and **✍️ WRITING RULES** instead.

## 📦 Installation

Import:

`Chaos_and_Soul.json` → **SillyTavern → Chat Completion Presets → Import**

The included Regex scripts are available under:

**Extensions → Regex → Preset Scripts**

If you have global copies of the same scripts enabled, disable them so they don't run twice.

The preset contains an **📝 FAQ** with toggle combinations, model-specific notes and temperature recommendations.
