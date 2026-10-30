# Copyright Infringement Evidence & Enforcement Case Study

Educational portfolio project. All parties, works, events and evidence are fictional. This is not legal advice and does not describe any real dispute.

**Author:** [SATYAM KUMAR SINGH]
**Jurisdiction:** India
**Assumed date of analysis:** 30 October 2026

---

## 1. Overview

This repository works through one invented copyright dispute from intake to enforcement decision. A Delhi photography studio believes a snacks company used a commissioned food photograph beyond the terms of a 12-month digital licence: on its website after the licence ended, in a social media post of unknown date, and on retail packaging that the company says is its own reshoot.

The point of the exercise is not to prove infringement. It is to show how a careful first draft handles a case that does not fall neatly either way:

- the studio's own engagement terms suggest the photographer, not the studio, owns the copyright;
- the licence email says 12 months while the invoice says "ongoing";
- the packaging photograph shares some choices with the original and differs in others;
- the key screenshot has no date, the camera original file is missing, and every capture was made by an interested party.

The conclusion reached is that litigation is not justified on the present file, and that the proportionate steps are to fix title, preserve evidence properly, and approach the other side for a retrospective licence.

## 2. Skills demonstrated

- Element-by-element analysis of copyright infringement under Indian law, each element tied to a statutory provision and to identified evidence.
- Verification of authority against primary sources, with an explicit status for every provision and case, including an honest record of what could not be checked.
- Disciplined separation of stipulated facts, sourced facts, assumptions, inferences, allegations and conditional conclusions.
- Digital evidence handling: web capture, metadata, file naming, chain of custody, SHA-256 integrity verification, and admissibility under the Bharatiya Sakshya Adhiniyam, 2023.
- Argument from the other side: the respondent's case put at its strongest before any conclusion is drawn.
- Proportionate enforcement planning: graduated options, each with preconditions, risks and qualitative costs.
- Procedural awareness: forum, commercial-dispute classification, pre-institution mediation, limitation and the effect of delay.

## 3. Methodology

1. **Design the dispute.** Build in a genuine ownership question, a licence-scope question, a credible alternative explanation for similarity, and a real evidentiary weakness.
2. **Fix the facts.** Create 12 evidence items with identifiers, and a chronology that matches them exactly.
3. **Research the law.** Start from official sources; record a verification status, the precise proposition relied on, and the limits of what was inspected.
4. **Analyse.** Test each element, compare the works feature by feature, then argue the respondent's case.
5. **Identify gaps.** State what is missing, why it matters, how it could be obtained lawfully, and what follows if it cannot be.
6. **Decide.** Recommend the least escalated step that fits the evidence and the value of the claim.
7. **Check.** Verify that identifiers, dates and descriptions match across every file, that the CSVs parse, and that nothing claims more than was actually verified.

## 4. Repository guide

| Start here if you want to | Read |
|---|---|
| Understand the dispute in five minutes | `case-file/case-background.md` |
| See the reasoning in full | `analysis/preliminary-legal-memorandum.md` |
| Check the evidence | `case-file/fictional-evidence-pack.md`, `case-file/evidence-index.csv` |
| See how the law was verified | `research/sources-and-case-law.md` |
| Judge the evidence method | `templates/evidence-handling-protocol.md` |
| See whether the analysis is balanced | `analysis/defences-and-counterarguments.md` |
| Know what the author does not claim to know | `analysis/limitations.md` |

```
copyright-infringement-evidence-enforcement-case-study/
├── README.md
├── LICENSE
├── .gitignore
├── case-file/
│   ├── case-background.md               Why a photograph; parties; facts; assumed forum and date
│   ├── fictional-evidence-pack.md       Items E-01 to E-12 in full
│   ├── chronology.md                    Events EV-01 to EV-22
│   └── evidence-index.csv               Index of all evidence items
├── analysis/
│   ├── preliminary-legal-memorandum.md  Seven issues: law, application, counterarguments, gaps
│   ├── copyright-elements-analysis.md   Ten elements against statute and evidence
│   ├── comparative-work-analysis.md     Feature-by-feature comparison of the works
│   ├── defences-and-counterarguments.md The respondent's case, then the replies
│   ├── evidence-gap-analysis.md         Gaps G-01 to G-12, with lawful ways to fill them
│   ├── enforcement-options.md           Six graduated options
│   └── limitations.md                   Limits of the scenario, research and method
├── templates/
│   ├── evidence-register.csv            Reusable register (EXAMPLE rows included)
│   ├── infringement-assessment-matrix.csv
│   ├── chronology-template.csv
│   ├── initial-review-checklist.md      Intake checklist for a new complaint
│   └── evidence-handling-protocol.md    The protocol a junior team member would follow
├── research/
│   └── sources-and-case-law.md          Verification table and notes on every authority
└── portfolio/
    └── cv-entry.md                      CV bullet options and a 60-word summary
```

`templates/evidence-handling-protocol.md` is the protocol referred to throughout the analysis; it sits in `templates/` because it is reusable on any matter.

## 5. Status tags

Used consistently in the analysis files.

| Tag | Meaning |
|---|---|
| `[STIPULATED]` | A fact fixed by the fictional scenario. |
| `[SOURCED]` | A fact supported by an identified evidence item or source. |
| `[ASSUMPTION]` | A fact assumed for the purposes of the analysis. |
| `[INFERENCE]` | A conclusion drawn from other facts. |
| `[ALLEGATION]` | An unverified claim by a party. |
| `[CONDITIONAL]` | A legal conclusion that depends on stated conditions. |

## 6. Risk scale

Risk is stated from the prospective claimant's point of view, in words only. No percentages, scores or probabilities are used anywhere in this repository.

| Level | Meaning |
|---|---|
| **Low** | On the stated facts and checked law, the point is unlikely to go against the claimant; remaining doubt concerns proof, not principle. |
| **Moderate** | Credible arguments both ways; the outcome turns on how a court reads the documents or weighs available evidence. |
| **Significant** | A real prospect the point goes against the claimant on present evidence; a corrective step or new evidence is needed. |
| **Indeterminate** | Cannot responsibly be assessed until missing evidence or unverified law is obtained. |

## 7. Verification status of authorities

Every provision and case carries one of three labels in `research/sources-and-case-law.md`: **VERIFIED** (relevant text inspected), **PARTIALLY VERIFIED** (headnote, operative conclusion, unofficial reproduction or commentary only), or **UNVERIFIED** (not accessed; not relied on). Where the analysis depends on a partially verified source, it says so. No citation, paragraph number, quotation or legal test in this repository was invented.

## 8. Licence

The written content and templates are licensed under **Creative Commons Attribution 4.0 International (CC BY 4.0)**. See `LICENSE`.

CC BY 4.0 was chosen because this is written work rather than software: a software licence such as MIT or Apache 2.0 would address warranties and patents that do not arise here, while CC BY 4.0 allows reuse and adaptation in teaching and training on the single condition of attribution. The `LICENSE` file reproduces Creative Commons' own short-form notice with the canonical links rather than a paraphrase.

## 9. Limitations

Summarised here; stated fully in `analysis/limitations.md`.

- The dispute and all evidence are invented. The works are described in words; no image is reproduced.
- Research was completed on 30 October 2026 and reflects nothing later.
- Several authorities are only partially verified, including *Eastern Book Company v. D.B. Modak*, *Arjun Panditrao Khotkar*, *Patil Automation*, *Yamini Manohar*, s. 170 and the Schedule of the Bharatiya Sakshya Adhiniyam, 2023, and Article 88 and s. 22 of the Limitation Act, 1963.
- Some questions were not researched at all, including whether a typed message is "signed" under s. 19(1) of the Copyright Act, 1957, whether accrued causes of action can be assigned, Delhi's pecuniary jurisdiction limits, and the measure of damages.
- No real evidence files exist, so no evidence hash is computed. The only computed hash in the repository is the worked example on `.gitignore` in the evidence protocol.
- The author is a law student. A supervising lawyer would review every conclusion before it was acted on.


