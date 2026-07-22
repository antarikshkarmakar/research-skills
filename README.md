# Universal AI Research Skills Protocol

A platform-agnostic, hyper-rigorous AI research skill suite designed for high-stakes executive research, evidence verification, case-study narrative synthesis, and fact-checking.

Engineered for seamless execution across **Claude**, **OpenAI (ChatGPT / Custom GPTs)**, **Gemini**, and **NotebookLM**, featuring second-brain memory indexing, session handoffs, interactive walkthroughs, and immutable audit logs.

---

## 🌟 Core Features

- **Stateless Memory Clamp & Second Brain Indexing (`MEMORY.md`)**: Restricts reasoning strictly to user-provided PDFs, open-access sources, or verified extractions, while indexing active context across turns.
- **Session Handoff System (`Handoff.md`)**: Preserves pipeline stage, active target unit, and locked paragraphs during turn transitions or subagent handoffs.
- **8-Step Case Study Workflow & Walkthrough (`workflows/research-walkthrough.md`)**: Structured pipeline from Illusion & Reality framing to candidate case list generation, source verification, PDF extraction, narrative drafting, and line-by-line evidence tracing.
- **Immutable Audit Trail & ADRs (`AUDIT_TRAIL.md` & `memory/adr/`)**: Complete historical audit log documenting candidate case scores (0-5 matrix), source verification logs, quoted handle traces, and Analytical Decision Records.
- **Board-Ready Persona & Voice**: Executive-level, authoritative, non-fluffy, non-dramatic output with strict prohibition on consultant filler and em dashes (`—`).
- **Multi-Platform Adapters**: Tailored formatting for Claude Skills (`SKILL.md`), OpenAI System Prompts, Gemini AI Studio Instructions, and NotebookLM Source Prompts.

---

## 📁 Repository Structure

```
researchSkills/
├── gist.md                          # Source Protocol v4.8 (Digital Transformation Insights)
├── ref.md                           # Reference Skill Registries
├── README.md                        # Master Documentation & Setup Guide
├── core-protocol.md                 # Core Platform-Agnostic Protocol Engine
├── MEMORY.md                        # Universal Second Brain Research Index
├── Handoff.md                       # Session State Handoff & Transition Template
├── AUDIT_TRAIL.md                   # Immutable Research Decision & Scoring Register
├── memory/
│   ├── sources-index.md             # Verified Sources & PDF Evidence Catalog
│   ├── observations.md              # Research Protocol Observations & Process Log
│   └── adr/
│       └── template.md              # Analytical Decision Record Template
├── adapters/
│   ├── claude/
│   │   ├── SKILL.md                 # Claude Skill Definition (YAML + System + Checklist + Triggers)
│   │   └── references/
│   │       └── protocol-v4.8.md     # Full 21-section canonical protocol (binding source-of-truth)
│   ├── openai/
│   │   └── system_instructions.md   # ChatGPT / Custom GPT System Prompt
│   ├── gemini/
│   │   └── system_instructions.md   # Gemini AI Studio / System Instructions
│   └── notebooklm/
│       └── source_guide.md          # NotebookLM Grounded Source & Prompt Guide
└── workflows/
    ├── paper-fact-checker.md        # Claim verification & audit matrix
    ├── parallel-deep-research.md    # Multi-angle query decomposition & synthesis
    ├── executive-insight-generator.md # Board mirror-questions & provocative insights
    ├── paper-slide-deck.md          # Research to presentation deck workflow
    └── research-walkthrough.md      # Progress dashboard & interactive walkthrough
```

---

## 🚀 Quick Start & Platform Deployment

### 1. Claude

**Claude Code (CLI):**
```bash
mkdir -p ~/.claude/skills/universal-research-protocol/references
cp adapters/claude/SKILL.md ~/.claude/skills/universal-research-protocol/
cp adapters/claude/references/protocol-v4.8.md ~/.claude/skills/universal-research-protocol/references/
```
Restart your session so the skill loads. It auto-triggers on requests matching its description (case-study research, fact-checking, evidence extraction), or invoke it by name if your harness supports that.

**Claude Desktop / Claude Web / Anthropic API:** upload both `adapters/claude/SKILL.md` and `adapters/claude/references/protocol-v4.8.md` as project files (or paste `SKILL.md` into a system prompt) — the `references/protocol-v4.8.md` pointer only resolves if that file is attached alongside it.

**Using it:**
- Trigger with a case-study/fact-checking request, or the tokens `@HARD FAIL@`, `@STATUS@` / `@STATUS,n@`.
- It runs an 8-step pipeline: Illusion & Reality Check → 5 scored candidate cases → source verification → PDF upload → evidence-pack approval → narrative draft → evidence trace → lock & MyLib reference export. Each step waits for your explicit approval before advancing — it will not skip ahead.

### 2. OpenAI (ChatGPT Custom GPTs / Assistants API)

**ChatGPT Custom GPT (no code):**
1. Open ChatGPT → **Explore GPTs** → **Create**.
2. In the **Configure** tab, set the GPT **Name** and **Description** (e.g. "Universal Executive Research Protocol - case-study evidence synthesis with hard-fail safety").
3. Paste the entire contents of `adapters/openai/system_instructions.md` into the **Instructions** field.
4. Under **Knowledge**, upload any project-specific reference files (your `MEMORY.md`, `Handoff.md`, prior `AUDIT_TRAIL.md`, source PDFs) so the GPT can ground responses in your corpus. Optional but recommended.
5. Under **Capabilities**, leave **Web Browsing** and **DALL-E** off to honour the no-hallucination rule. Code Interpreter is safe to leave on.
6. **Save** and start a new conversation. The 8-step pipeline and `@HARD FAIL@` / `@STATUS@` tokens become active immediately.

**Assistants API / OpenAI Platform (programmatic):**
1. In the OpenAI dashboard, create a new Assistant.
2. Paste `adapters/openai/system_instructions.md` into the **System instructions** field.
3. Enable the **File search** tool and attach the same `core-protocol.md` plus any `memory/` files you want the assistant to retrieve from.
4. Create a Thread and run it. The assistant enforces stateless evidence containment, em-dash ban, paragraph locking, and the 8-step pipeline automatically.

**Using it:**
- Trigger with a case-study / fact-checking request, or the tokens `@HARD FAIL@`, `@STATUS@` / `@STATUS,n@`.
- It runs the same 8-step pipeline as the Claude adapter: Illusion & Reality Check → 5 scored candidate cases → source verification → PDF upload → evidence-pack approval → narrative draft → evidence trace → lock & MyLib reference export. Each step waits for your explicit approval before advancing.
- Lifecycle files (`MEMORY.md`, `Handoff.md`, `AUDIT_TRAIL.md`, `memory/sources-index.md`) can be uploaded as Knowledge so the assistant can read and append them across threads.

### 3. Gemini (Google AI Studio / Gems)

**Gemini API (Google AI Studio, programmatic):**
1. Open [aistudio.google.com](https://aistudio.google.com) and create a new **System Instructions** prompt (or open the **Structured prompt** view if you want section labels).
2. Paste the entire contents of `adapters/gemini/system_instructions.md` into the **System Instructions** field.
3. Set **Temperature** to a low value (0.1-0.3) to reduce drift, and **Top-P** to a similarly conservative range.
4. Under **Grounding**, attach `core-protocol.md` and any project-specific files (`MEMORY.md`, `Handoff.md`, `AUDIT_TRAIL.md`, source PDFs) so Gemini grounds outputs in your corpus.
5. Run a test prompt to confirm the 8-step pipeline, em-dash ban, and `@HARD FAIL@` / `@STATUS@` tokens are honoured before using it on real research.

**Custom Gems (gemini.google.com, no code):**
1. Open Gemini → **Gems** → **Create a new Gem**.
2. Set the Gem **Name** and a short description matching the protocol.
3. Paste the contents of `adapters/gemini/system_instructions.md` into the **Instructions** field.
4. Optionally upload reference files via the file attachment control at the start of each chat (Gems do not persist file attachments across sessions, so re-attach `core-protocol.md` and any lifecycle files each time).
5. Save and start chatting. The Gem enforces the same stateless evidence containment, em-dash ban, paragraph locking, and 8-step pipeline as the Claude and OpenAI adapters.

**Using it:**
- Trigger with a case-study / fact-checking request, or the tokens `@HARD FAIL@`, `@STATUS@` / `@STATUS,n@`.
- It runs the same 8-step pipeline as the Claude and OpenAI adapters: Illusion & Reality Check → 5 scored candidate cases → source verification → PDF upload → evidence-pack approval → narrative draft → evidence trace → lock & MyLib reference export. Each step waits for your explicit approval before advancing.
- If a Gem loses context mid-session, paste the relevant `Handoff.md` block and re-paste the protocol's "Permanent Rules" section to re-clamp behaviour.

### 4. NotebookLM (Google NotebookLM)
Upload your primary source PDFs into NotebookLM, then paste `adapters/notebooklm/source_guide.md` as the guiding prompt.

---

## 📜 Lifecycle Management

- **Memory**: Update `MEMORY.md` whenever an Illusion/Reality check is ingested or a paragraph is locked.
- **Handoff**: Generate a `Handoff.md` block at the end of a session to pass context to the next agent.
- **Audit**: Log candidate case scores (0-5 matrix) and quoted handle traces in `AUDIT_TRAIL.md`.

---

## 📜 License & Acknowledgments
Based on Protocol v4.8 for Executive Digital Transformation Insights & Evidence Synthesis. Inspired by [antarikshSkills](https://github.com/antarikshkarmakar/antarikshSkills).
