# Readme

# Harness Engineering for Auditable Generative AI

### Replication Package — Cross-Border Construction Contract Risk Review (HYT × LDH Case)

This repository holds the complete input, output, and audit-trail materials for the instrumental case study reported in:

> **Harness Engineering for Auditable Generative AI: A Four-Property Paradigm with Empirical Validation**
> Jin-Ching Shen, Nai-Ching Su, and Yi-Bing Lin
> College of Artificial Intelligence, National Yang Ming Chiao Tung University; Department of Project Management and Industrial Engineering, Shandong University.

With these materials you can trace an AI-assisted contract review end to end—from the original agreement, through the risk analysis and the derisked draft, to the audit log that records both the Agent Skill's decisions and the human confirmations behind them.

---

## Why this repository exists

Generative AI has moved into high-stakes decision-support settings faster than the governance frameworks meant to keep it accountable. The EU AI Act and the NIST AI RMF both require AI outputs to be transparent to authorized auditors, yet most controlled-generation work—RAG, Chain-of-Thought prompting, RLHF—has concentrated on the input side, treating output trustworthiness as something to infer rather than something to demonstrate.

The paper proposes **Harness Engineering**, a workflow-level design layer that sits between prompt engineering and institutional AI governance, and formalizes the **Auditable Generation Paradigm (AGP)** through four co-dependent properties:

- **P1 — Knowledge Traceability:** every invoked knowledge unit carries a retrievable citation record.
- **P2 — Rule-Governed Generation Boundary:** every generation stays within an explicit, externally inspectable rule set.
- **P3 — Accountable Decision Logging:** every decision leaves a complete, independently reconstructable provenance record.
- **P4 — Structured Human Verification:** each critical decision node passes through a logged human-authorization gate.

This repository is the empirical backbone of that argument—a single production-grade deployment, the **HYT × LDH** cross-border factory-renovation contract review, in which all four properties reached full compliance at the output level.

> **Core contribution on display here:** a two-layer accountability mechanism. The Agent Skill's rule-governed decisions and the human reviewer's per-clause confirmations are recorded in one auditable trail, so any external reviewer can reconstruct what was decided, on what basis, by whom, and with what consequence.

---

## The review workflow at a glance

```
  Original Contract  ──►  Risk Review Report  ──►  Derisked Contract
   (de-identified)         (AI analysis +           (finalised draft,
                            human decisions)          all changes applied)
                                   │
                                   └──────────►  Audit Report
                                                 (decision trail +
                                                  authorisation scope)
```

The original contract is the input. The risk review report runs a four-dimensional analysis—legality, reasonableness, legal risk, risk level—on each clause and produces recommendations. At the Stage 10 verification gate, a human reviewer confirms, modifies, or rejects each recommendation; the derisked contract is the finalized draft that results. The audit report captures the whole chain: the citations used, the rules triggered, the decisions taken, and the one boundary case the system flagged for human determination instead of resolving on its own.

---

## Repository contents

Four PDF files, all de-identified for academic release. Party identities, tax codes, bank details, and signatures are redacted and marked `[REDACTED]`.

- **`HYT_LDH_Construction_Contract_Deidentified.pdf`** — The input artefact: the original trilingual (Vietnamese / English / Traditional Chinese) cross-border construction contract between a Taiwanese-invested investor (Party A) and a Vietnamese local contractor (Party B), before any AI-assisted review. Every recommendation is measured against this baseline.
- **`1_Risk_Review(HYT_LDH).pdf`** — The AI analysis artefact: a clause-by-clause risk assessment covering the 23 mandatory review items, absolute red lines, and escalation triggers, with recommendations and an interactive amendment summary. This is the primary evidence for Knowledge Traceability (P1) and Rule-Governed Generation Boundary (P2).
- **`2_Derisked(HYT_LDH).pdf`** — The generative output artefact: the consolidated contract after the review round, with amended and newly inserted clauses—confidentiality, liability scope, language priority, VIAC arbitration, and others—marked for negotiation. It shows the end state that the logged decisions produce.
- **`3_Audit_Report(HYT_LDH).pdf`** — The accountability artefact: a six-section decision log (stage confirmation record, citation inventory, Stage 10 amendment history, AI-identified new-scenario log, final decisions on open items, and auto-application results). This is the primary evidence for Accountable Decision Logging (P3) and Structured Human Verification (P4), and the single document from which the full reasoning chain can be reconstructed.

**A note on de-identification.** Everything here has been anonymized for open-science release: company names are reduced to the neutral labels HYT and LDH, and all personal and financial identifiers are redacted. The analytical structure, statutory citations, and decision trail are kept intact, so the case remains fully reproducible.

---

## How to read the materials

On a first pass, this order works well:

1. **Start with the original contract** to see the baseline agreement and the risks it leaves unaddressed.
2. **Move to the risk review report** to follow how each clause is analyzed and what changes are recommended.
3. **Compare against the derisked contract** to see those recommendations realized as finalised clauses.
4. **Finish with the audit report**, which ties the first three together and shows the human-authorization trail. Two moments are worth pausing on: the warranty-period decision, where the reviewer overrode the AI's recommendation, and the confidentiality scenario, which the system flagged as a new case rather than forcing it into an existing category.

Taken together, the four documents make the paper's central point concrete: accountability in generative AI is secured most effectively not at the model level but at the workflow-architecture level, where Harness Engineering operates.

---

## Citation

If you use these materials, please cite the paper:

```bibtex
@article{shen_harness_engineering,
  title   = {Harness Engineering for Auditable Generative AI: Formalizing a
             Four-Property Paradigm and Its Empirical Instantiation in
             Cross-Border Contract Review},
  author  = {Shen, Jin-Ching and Su, Nai-Ching and Lin, Yi-Bing},
  note    = {Please refer to the published version for full journal, volume,
             and DOI details.}
}
```

*(Journal, volume, and DOI will be added once the article is published. Please update this entry with the final publication details.)*

---

## License

Unless stated otherwise, the materials in this repository are released for **academic and research use**. Please keep attribution to the authors and cite the associated paper when reusing any part of them. If you plan to redistribute or adapt the contents, consider adding an explicit license file (for example, `CC BY 4.0` for the documents) so the reuse terms are unambiguous.

---

## Acknowledgements

We thank the reviewers and colleagues who helped shape the analytical protocol and who independently verified the boundary cases reported in the study. The de-identified case materials are shared in the spirit of open science—to support reproducibility, and to invite scrutiny of the Auditable Generation Paradigm as a qualitative-research paradigm for trustworthy AI.
