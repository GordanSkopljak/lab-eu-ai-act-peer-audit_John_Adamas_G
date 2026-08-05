# Audit your teammate's project

> **How you'll submit this lab**
>
> This repo is your lab. Fork it, do the work described below in your fork, then open a pull
> request back into this repository. An AI reviewer will check your PR against `rubric.md` and
> leave feedback directly on the PR. See `README.md` for the full workflow.

In this lab, you audit a teammate's SilverTrust project — and they audit yours. Neither of you has built the other's system, which is exactly the point. An external reviewer catches things that builders miss. Fresh eyes see gaps that familiarity hides.

This lab pairs with the self-audit lab. You should complete your own self-audit first. The peer audit tests whether an independent reviewer reaches the same conclusions — and surfaces the differences when they don't.

## Lesson alignment

- **Learning objectives:** By the end, you can conduct an independent compliance review of an AI system you did not build, produce a structured audit report, and engage in a productive debrief conversation with the system's builder.
- **Lesson setup requirements:** Completed self-audit (`02_lab_self-audit.md`), review of `01_eu-ai-act-fundamentals.md` risk tiers and obligations, and the compliance/legal framing from `00_compliance-and-legal.md`.

---

## Submission hygiene

- **Filenames:** Use clear, descriptive names (avoid names such as `peer_review.md` or `audit_teammate.pdf`).
- **Scope:** Your **GitHub** repository must contain **only materials for this lab**—no unrelated projects, dumps, or personal files.
- **README:** Add a short file map if you submit multiple documents. Include your teammate's name and which project you audited.

**GitHub only:** Submit the URL to a **GitHub repository** that contains everything for this lab. Do **not** submit a standalone Google Doc, Notion page, or cloud-only link.

---

## Kick-off

### What you exchange

Before you begin, you and your teammate exchange **system briefs only** — not your self-audit findings.

Your teammate gives you:
- The system brief they wrote in Phase 1 of the self-audit lab (300–500 words describing what they built)
- Any technical documentation or architecture diagrams they produced during the course (optional but useful)

Your teammate does **not** give you:
- Their risk tier classification
- Their gap analysis
- Their compliance memo

The point is to audit independently. If you see their conclusions first, you're confirming their thinking, not testing it.

### Ground rules

- Work independently until the debrief. Don't discuss your findings with your teammate until Phase 5.
- Ask clarifying questions in writing only, and log them — these questions become part of your audit trail ("information requested from client on [date]").
- If the brief is unclear or incomplete, note the ambiguity and state what you assumed. In a real engagement, incomplete information is the norm.

---

## CFU checkpoints

### 1. Recognize

Read the teammate's system brief and form a first-pass risk tier classification: prohibited, high-risk, limited risk / transparency, or minimal risk. Write one paragraph justifying your classification by reference to the specific Article or Annex entry that governs it.

### 2. Probe

Identify the three most important clarifying questions you would ask the client before confirming your classification. In a real engagement, you would ask these before issuing any opinion. Note what your provisional answer is for each if you don't get a response.

### 3. Map roles

Map the provider, deployer, and any third-party vendors in your teammate's system. Identify the key obligations that flow from each role.

### 4. Find the gaps

If the system is high-risk: review it against the 11 provider obligations and identify which are met, partial, or absent based on the available information.

If the system is limited risk: identify what transparency disclosures are required and whether the brief suggests they are in place.

In all cases: flag any parallel legal issues (GDPR, consumer protection, sector regulation) that appear relevant.

### 5. Debrief

Compare your audit findings with your teammate's self-audit. Discuss where you agreed, where you disagreed, and why.

---

## Core

### Phase 1: Read and annotate

Read your teammate's system brief once without taking notes. Then read it again and annotate:

- Underline any element that affects the risk tier classification
- Circle any element that is unclear or that you'd need to clarify before forming a view
- Mark any element that suggests a specific obligation applies

Keep these annotations — they become the evidence base for your report.

### Phase 2: First-pass classification

Complete the same classification table you used in the self-audit:

| Question | Your answer |
|---|---|
| Does this system fall under any prohibited category (Article 5)? | |
| Does this system operate in any of the eight Annex III areas? | |
| If Annex III: does it significantly influence decisions in that area, or is it narrow/preparatory? | |
| Does this system interact with end users or generate content requiring disclosure (Article 50)? | |
| First-pass risk tier | |
| One-sentence justification citing the specific article or Annex entry | |

If you are uncertain between tiers, state the uncertainty and list the clarifying questions that would resolve it.

### Phase 3: Clarifying questions log

Write down the three to five questions you would ask before finalizing your audit. For each question, note:

- What you need to know
- Why it matters for the risk classification or obligation mapping
- What you are **provisionally assuming** in the absence of an answer

This log is part of your deliverable. In consulting, documenting what you asked and what you assumed is as important as the conclusions.

### Phase 4: Audit report

Write a structured audit report covering the following sections. Keep it to two pages maximum.

**Section 1: System summary**
Brief restatement of what the system does, in your own words. This confirms you understood the brief correctly. (3–5 sentences)

**Section 2: Risk classification**
Your first-pass tier, the justification, and any areas of uncertainty.

**Section 3: Role map**
Provider, deployer, any third-party vendors, and the key obligations that flow from each role.

**Section 4: Compliance findings**

Use this structure for each finding:

> **Finding [number] — [Obligation or issue]**
> **Severity:** Blocking / Significant / Minor
> **Description:** What the requirement is and what the evidence suggests about whether it is met.
> **Recommended action:** What the team should do to address this finding.
> **Escalation needed?** Yes / No — and if yes, to whom.

Severity guide:
- **Blocking** — deployment cannot proceed without resolving this (e.g., a prohibited practice, a missing conformity assessment for high-risk AI)
- **Significant** — deployment could proceed, but the risk is material and remediation should begin immediately
- **Minor** — good practice to resolve, but does not block launch

**Section 5: Overall recommendation**
One of three positions, with a one-paragraph rationale:
- **Clear to proceed** — no blocking findings, minor issues noted
- **Proceed with conditions** — significant findings must be addressed before deployment; specify conditions
- **Do not proceed** — one or more blocking findings; redesign required before any further assessment

**Section 6: What this report is not**
A short standard disclaimer: this report is not a legal opinion, not a conformity assessment, and not a certification. Conclusions should be verified with legal counsel before any EU market placement.

### Phase 5: Debrief conversation

Sit down with your teammate. Run the debrief in this order:

1. **Auditor presents** — walk through your audit report without interruption. Your teammate listens.
2. **Builder responds** — your teammate has five minutes to explain any choices, context, or information that was missing from the brief.
3. **Compare classifications** — each person reveals their self-audit tier and the auditor's tier. If they differ, discuss why. Was it a genuine disagreement about the regulation, or did the brief not communicate something important?
4. **Compare gap lists** — each person shares their top findings. What did the self-audit catch that the external audit missed? What did the external audit catch that the builder missed?
5. **Joint closing note** — together, write two to three sentences answering: *What does this debrief reveal about the difference between auditing your own work and auditing someone else's?*

This closing note is a required deliverable. Include it in your submission.

---

## Reinforce

If you finish the core tasks early:

- Review the clarifying questions your teammate asked you about your own system. Are there any you cannot answer? What does that tell you about your documentation?
- Identify one finding from your teammate's audit report that you, as the builder, initially disagreed with. After the debrief, do you still disagree? Why or why not?

## Stretch

Take one **Significant** or **Blocking** finding from your audit report and draft the consulting work plan to address it:

- What deliverable would close this gap? (A policy, a technical change, a process design, a legal review)
- Who would be responsible for producing it?
- What is a realistic timeline?
- What evidence would you need to verify it is closed?

Keep this to half a page. The goal is to move from "here is a problem" to "here is a plan" — which is what a client actually needs.
