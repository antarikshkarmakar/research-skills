# AUDIT_TRAIL.md — Immutable Research Decision & Scoring Audit Register

> **PURPOSE**: Complete historical audit log capturing candidate case scoring rationales, source verification results, evidence handle trace mappings, and candidate rejection logs.

---

## 1. Candidate Case Scoring Log (Step 2 Audit)

| Date | Candidate Case Name | Relevance (0-5) | Multi-Harm (0-5) | Recency (0-5) | Impact (0-5) | Private Weight (0-5) | Source Access (0-5) | Causal Link (0-5) | Composite Score | Audit Decision |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| YYYY-MM-DD | `[Case A]` | 5 | 4 | 4 | 5 | 5 | 4 | 5 | **4.57** | `RECOMMENDED` |
| YYYY-MM-DD | `[Case B]` | 3 | 2 | 5 | 3 | 2 | 2 | 3 | **2.85** | `DISCARDED` |

### Candidate Rejection Rationale
- **Case B Rejected**: Failed source accessibility threshold and weak causal link to Reality Check Harm #2.

---

## 2. Source Verification & Admissibility Log (Step 3 & 4 Audit)

| Date | Source Handle | Expected Archetype Pointer | Verified Open-Access Status | PDF Uploaded | Admissibility Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| YYYY-MM-DD | `[CaseA_FT_2024]` | `[FT / Financial Failure / "Overrun"]` | `VERIFIED` | `YES` | `ADMISSIBLE EVIDENCE` |
| YYYY-MM-DD | `[CaseC_Blog_2023]` | `[Vendor PR Blog]` | `UNVERIFIED` | `NO` | `DISCARDED (PROHIBITED)` |

---

## 3. Evidence Extraction & Handle Trace Audit (Step 5 & 7 Audit)

| Sentence ID | Drafted Sentence Content | Quote Handle (First 6-8 Words) | Source PDF & Location | Verification Status |
| :--- | :--- | :--- | :--- | :--- |
| `S1` | *"The agency launched the core overhaul in 2021..."* | `"The agency launched its core cloud overhaul..."` | `[CaseA_FT_2024: Page 2, P3]` | `VERIFIED MATCH` |
| `S2` | *"Vendor costs doubled within six months..."* | `[NO DIRECT EVIDENCE IN PDF]` | `N/A` | `NO DIRECT EVIDENCE` |

---

## 4. Hard Fail & Protocol Execution Audit

| Date & Time | Trigger Type | Trigger Reason | Restated Active Unit | Restricted Mode Turn Counter | Resolution |
| :--- | :--- | :--- | :--- | :--- | :--- |
| YYYY-MM-DD | `@HARD FAIL@` | `[Manual / Auto em-dash detected]` | `[Sentence content]` | `[1/2 -> 2/2 -> Cleared]` | `Re-established context` |
