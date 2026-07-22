# NotebookLM Grounded Research & Source Guide

Google NotebookLM is uniquely suited for **stateless, grounded evidence research** because its architecture restricts answers strictly to your uploaded sources (PDFs, docs, research papers, web links).

This guide provides the custom guiding prompts and source preparation workflow to execute the **v4.8 Executive Research Protocol** inside NotebookLM.

---

## 1. Source Upload Strategy (Step 4 Alignment)

To maintain maximum evidence integrity in NotebookLM:
1. **Clean Source PDF Uploads**: Upload full-text research papers, regulator filings (GAO, NAO, SEC), or news articles.
2. **Exclude Consultant Fluff**: Avoid marketing whitepapers or generic blog posts.
3. **Structured Source Tagging**: Rename sources in NotebookLM using standard handles: `[CaseName_Outlet_Year]`.

---

## 2. NotebookLM Master Guiding Prompt

Copy and paste the following master prompt into NotebookLM chat when analyzing your uploaded sources:

```text
You are a Global Digital Transformation Expert and Critical Editorial Director.
Analyze the uploaded sources strictly according to these non-negotiable rules:

1. SOURCE CONTAINMENT: Answer using ONLY the uploaded source documents. Do not use external pre-training knowledge.
2. NO EM DASHES: Do not use em dashes ("—"). Use hyphens ("-") or commas (",") instead.
3. QUOTED HANDLES: For every factual claim or case observation, provide the exact quote handle (first 6 to 8 words) and source document title.
4. EXECUTIVE TONE: Sober, direct, plain, authoritative. No consultant jargon or fluff.
5. HARM MAPPING: When explaining organizational failure, state the tangible harm (cost, delay, risk, bureaucracy, capability loss) and explain the underlying mechanism supported by the sources.

Awaiting user query on Illusion & Reality Check or Case Study Extraction.
```

---

## 3. NotebookLM Step-by-Step Workflow Prompts

### Step A: Evidence Extraction Pack
> **Prompt**:  
> *"Extract all empirical evidence from the uploaded sources related to [Illusion / Topic]. Group the extractions by Section and provide quoted handles (first 6-8 words of the source line) for each point. Highlight any gaps where the sources do not provide empirical proof."*

### Step B: Executive Case Narrative Drafting
> **Prompt**:  
> *"Draft a single-paragraph executive case study narrative based EXCLUSIVELY on the extracted quotes. Format: 1 opening sentence defining mistaken belief, 3 to 5 evidence-backed sentences with quoted handles, and 1 closing sentence linking failure to organizational mechanism. Do not introduce any facts outside the uploaded sources. Do not use em dashes."*

### Step C: Evidence Trace Audit
> **Prompt**:  
> *"Generate a sentence-by-sentence trace table for the draft paragraph above. Map each sentence directly to its supporting quote handle from the uploaded sources. Mark any unevidenced sentence as 'NO DIRECT EVIDENCE'."*
