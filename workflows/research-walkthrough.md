# Workflow: Research Walkthrough & Interactive Progress Tracker

A specialized workflow module for tracking execution progress, visualizing candidate scoring, monitoring evidence extractions, and documenting step-by-step verification throughout the 8-step research pipeline.

---

## 1. Interactive 8-Step Pipeline Status Dashboard

```markdown
### Research Pipeline Progress
- [x] **Step 1: Ingest Illusion & Reality** — *[STATUS: Complete]*
- [x] **Step 2: Scored Candidate Cases (0-5 Matrix)** — *[STATUS: Complete]*
- [ ] **Step 3: User Verification of Open-Access Sources** — *[STATUS: IN PROGRESS]*
- [ ] **Step 4: PDF Source Upload & Admissibility Check** — *[STATUS: Pending]*
- [ ] **Step 5: Structured Evidence Extraction Pack** — *[STATUS: Pending]*
- [ ] **Step 6: Single-Paragraph Case Narrative Drafting** — *[STATUS: Pending]*
- [ ] **Step 7: Sentence Evidence Trace Audit** — *[STATUS: Pending]*
- [ ] **Step 8: Final Review, Paragraph Locking & MyLib Export** — *[STATUS: Pending]*
```

---

## 2. Step 2 Candidate Scoring Comparison Dashboard

| Candidate Case | Relevance | Multi-Harm | Recency | Impact | Private Pref | Source Access | Causal Link | Composite Score | Status |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| **Case 1: NHS NPfIT** | 5 | 5 | 3 | 5 | 1 | 5 | 5 | **4.14** | `SHORTLISTED` |
| **Case 2: Hertz vs Accenture** | 5 | 4 | 4 | 5 | 5 | 4 | 5 | **4.57** | `TOP PICK` |
| **Case 3: BBC DMI** | 4 | 4 | 3 | 4 | 2 | 5 | 4 | **3.71** | `RESERVE` |

---

## 3. Step 5 & 7 Evidence Trace Audit Visualization

```text
DRAFT PARAGRAPH:
[Sentence 1 content...] (CaseA_FT_2024: Page 2, P3)
[Sentence 2 content...] (CaseA_FT_2024: Page 4, P1)

EVIDENCE TRACE AUDIT:
- Sentence 1 -> Supported by Evidence [1] (quoted handle: "The agency launched its core cloud overhaul...")
- Sentence 2 -> Supported by Evidence [2] (quoted handle: "Implementation costs escalated from 50M to...")
```

---

## 4. Execution Prompt

```text
Run Research Walkthrough Workflow on current session state:
Update the 8-Step Progress Dashboard, display current candidate scoring matrices, and generate the sentence evidence trace table for active drafts.
```
