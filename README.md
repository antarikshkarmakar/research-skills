# Universal AI Research Skills Protocol

A platform-agnostic, hyper-rigorous AI research skill suite designed for high-stakes executive research, evidence verification, case-study narrative synthesis, and fact-checking.

Engineered for seamless execution across **Claude**, **OpenAI (ChatGPT / Custom GPTs)**, **Gemini**, and **NotebookLM**.

---

## 🌟 Core Features

- **Stateless Memory Clamp & Evidence Containment**: Strict anti-hallucination guardrails that restrict reasoning to user-provided PDFs, open-access sources, or verified extractions.
- **8-Step Case Study Workflow**: Structured pipeline from Illusion & Reality framing to candidate case list generation, source verification, PDF extraction, narrative drafting, and line-by-line evidence tracing.
- **Board-Ready Persona & Voice**: Executive-level, authoritative, non-fluffy, non-dramatic output with strict prohibition on consultant filler and em dashes.
- **Multi-Platform Adapters**: Tailored formatting for Claude Skills (`SKILL.md`), OpenAI System Prompts, Gemini AI Studio Instructions, and NotebookLM Source Prompts.
- **Specialized Workflows**: Modules for paper fact-checking, parallel deep research, executive insight generation, and slide deck structuring.

---

## 📁 Repository Structure

```
researchSkills/
├── gist.md                          # Source Protocol v4.8 (Digital Transformation Insights)
├── ref.md                           # Reference Skill Registries
├── README.md                        # Master Documentation & Setup Guide
├── core-protocol.md                 # Core Platform-Agnostic Protocol Engine
├── adapters/
│   ├── claude/
│   │   └── SKILL.md                 # Claude Skill Definition (YAML Frontmatter + XML Blocks)
│   ├── openai/
│   │   └── system_instructions.md   # ChatGPT / Custom GPT System Prompt
│   ├── gemini/
│   │   └── system_instructions.md   # Gemini AI Studio / System Instructions
│   └── notebooklm/
│       └── source_guide.md          # NotebookLM Grounded Source & Prompt Guide
└── workflows/
    ├── paper-fact-checker.md        # Claim verification & evidence mapping
    ├── parallel-deep-research.md    # Multi-angle query decomposition & synthesis
    ├── executive-insight-generator.md # Board mirror-questions & provocative insights
    └── paper-slide-deck.md          # Research to presentation deck workflow
```

---

## 🚀 Quick Start & Platform Deployment

### 1. Claude (Claude Desktop / Claude Web / Anthropic API)
Copy the contents of `adapters/claude/SKILL.md` into your Claude Desktop `skills` folder or upload as a project file / system prompt.

### 2. OpenAI (ChatGPT Custom GPTs / Assistants API)
Copy `adapters/openai/system_instructions.md` into the **Instructions** box of your Custom GPT or Assistant. Attach `core-protocol.md` as Knowledge if required.

### 3. Gemini (Google AI Studio / Gems)
Copy `adapters/gemini/system_instructions.md` into System Instructions in Google AI Studio or your custom Gem configuration.

### 4. NotebookLM (Google NotebookLM)
Upload your primary source PDFs / papers into NotebookLM, then paste `adapters/notebooklm/source_guide.md` as the guiding prompt for note generation and grounded Q&A.

---

## 📜 License & Acknowledgments
Based on Protocol v4.8 for Executive Digital Transformation Insights & Evidence Synthesis.
