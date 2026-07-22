# Handoff.md — Session State Handoff Protocol

> **PURPOSE**: Enables seamless state transitions across chat turns, context windows, or subagents, preserving the 8-step pipeline stage, active target unit, and locked paragraphs without losing context.

---

# Session Handoff — [YYYY-MM-DD]

## 1. Accomplished Pipeline Steps
- [ ] **Step 1: Illusion & Reality Ingested** — `[Completed / Pending]`
- [ ] **Step 2: Candidate Cases Scored** — `[Completed / Pending]`
- [ ] **Step 3: Source Verification** — `[Completed / Pending]`
- [ ] **Step 4: PDF Evidence Upload** — `[Completed / Pending]`
- [ ] **Step 5: Evidence Extraction Pack** — `[Completed / Pending]`
- [ ] **Step 6: Narrative Paragraph Drafted** — `[Completed / Pending]`
- [ ] **Step 7: Sentence Evidence Trace** — `[Completed / Pending]`
- [ ] **Step 8: Review, Lock & MyLib Export** — `[Completed / Pending]`

---

## 2. Current Session State
- **Active Research Seam**: `[Topic / Case under edit]`
- **Active Unit (Sentence/Line under edit)**:
  ```text
  [Verbatim active sentence under edit]
  ```
- **Locked Surrounding Text**:
  ```text
  [Verbatim surrounding locked paragraph bytes - IMMUTABLE]
  ```
- **Protocol Execution Mode**: `[Normal Protocol Mode | Restricted Mode 1/2 | Restricted Mode 2/2]`

---

## 3. Active Files & Evidence Sources
- **Active Document**: `[file basename](file:///absolute/path/to/file)`
- **Uploaded Source PDFs**:
  - `[Source_ID]`: `[File name / URL handle]`
- **Open Evidence Gaps**:
  - `[Detail any Reality Check harms lacking PDF proof]`

---

## 4. Immediate Next Step for Incoming Agent
- [ ] `[Single exact action for incoming agent to execute next]`
