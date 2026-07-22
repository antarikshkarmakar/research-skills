# Workflow: Research to Executive Slide Deck Generator

A specialized workflow module for translating rigorous research papers, evidence extractions, or case study narratives into structured, board-ready presentation slide decks.

Based on `luwill/research-skills/paper-slide-deck` and Protocol v4.8 presentation standards.

---

## 1. Deck Architecture Standards

1. **Executive Structure**: 5 to 10 slides maximum for C-suite presentation.
2. **One Core Message per Slide**: Every slide must have a distinct action-oriented headline (not generic titles like "Background" or "Results").
3. **Data & Evidence Anchors**: Bullet points must include specific metric handles or evidence handles from verified PDFs.
4. **No Fluff & No Em Dashes**: Maintain strict protocol tone and punctuation rules.

---

## 2. Slide Deck Template Structure

```markdown
# Executive Presentation: [Topic / Case Title]

## Slide 1: Executive Title & Core Thesis
- **Headline**: [1-line provocative executive takeaway]
- **Context**: [2 lines summarizing scope & methodology]
- **Bottom Line**: [Key recommendation or warning]

## Slide 2: The Core Illusion vs. Enterprise Reality
- **Perceived Belief**: [What the organization assumed]
- **Empirical Reality**: [What actually happened]
- **Mechanism Breakdown**: [2 bullet points detailing failure mechanism]

## Slide 3: Tangible Organizational Consequences (Harms)
- **Financial Impact**: [Cost overrun / revenue impairment handle]
- **Operational Risk**: [Capability degradation / schedule delay handle]
- **Governance Gap**: [Incentive misalignment handle]

## Slide 4: Case Study Evidence & Audit Findings
- **Case Evidence**: [Case name & audited source quote handle]
- **Key Observation 1**: [Primary empirical finding]
- **Key Observation 2**: [Secondary empirical finding]

## Slide 5: Board Mirror Questions & Strategic Mandate
- **Mirror Question 1**: [Diagnostic question for CxOs]
- **Mirror Question 2**: [Diagnostic question for Board]
- **Required Action**: [Clear next step]
```

---

## 3. Execution Prompt

```text
Run Paper Slide Deck Generator Workflow on the following research output / case narrative:
[PASTE RESEARCH OR CASE NARRATIVE HERE]

Convert into a 5-slide Executive Presentation Deck adhering to the Deck Architecture Standards. Use action headlines, explicit evidence handles, zero em dashes, and board-ready language.
```
