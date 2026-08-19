# Audit report and compliance memorandum: Virtual Coffee Chat Bot

**To:** John Adams, provider and deployer

**From:** Gordan, external reviewer

**Date:** 18 August 2026

**Re:** EU AI Act compliance position and peer audit findings

**Status:** Advisory. Not a legal opinion. See Section 15.

---

## 1. Purpose, scope and evidence base

This document is both the peer audit report and the durable classification record for the Virtual Coffee Chat Bot. It states what the system is under Regulation (EU) 2024/1689, which obligations attach, which are met, what has to change, and whether deployment should proceed.

**Scope.** The EU AI Act. Data protection, consumer protection and vendor contractual terms are outside the substantive analysis; the material ones are flagged in Section 7.6 because a compliance position that hides them would be misleading, not focused.

**Evidence base.** The provider's published project documentation: three workflow descriptions, the tool and API table, setup notes, and his own written limitations section. No access to the running system, the exported workflow definitions, or any non public material.

**Exchange record.** No self audit findings, risk classification, gap analysis or compliance position were exchanged in either direction before this report, per the lab ground rules. The audit was formed independently from the documentation above. Material received directly from the provider, and the date: [record here]. Five clarifying questions were sent on 18 August 2026 and were outstanding at issue; they are reproduced with their provisional assumptions in Section 9.

**Jurisdictional scope.** The provider is established in the Union and the system is put into service in the Union, so Article 2(1) is engaged. The Article 2(8) research and development exemption covers activity before a system is placed on the market or put into service; once the widget is exposed to third parties for a professional purpose the exemption is spent. There is no household exemption in the AI Act.

## 2. System summary

A conversational agent that stands in for John Adams during a first contact with a recruiter or hiring manager. It chats in his voice, answering questions about his work history, skills and projects from a retrieval layer holding his CV, CliftonStrengths results and narrative career material. It also acts: it checks Calendly availability, books a call, and sends email. Every turn, including thumbs up or down feedback, is written to a persistent `chat_log` table. It runs on self hosted n8n over OpenAI (gpt-5-mini, text-embedding-3-small), Pinecone, Cohere rerank, the Calendly API and Resend. The use case is professional identity and recruiting: the system exists so a stranger can learn about one candidate without that candidate being present.

## 3. Regulatory timeline

| Obligation set | Applies from | Relevant here |
|---|---|---|
| Article 5 prohibitions | 2 February 2025 | Screened. Not engaged. |
| Article 4 AI literacy | 2 February 2025 | Yes. Providers and deployers. Not deferred. |
| GPAI model obligations, Chapter V | 2 August 2025 | Rest with OpenAI. |
| Article 50 transparency | 2 August 2026 | **Yes. Live now.** |
| Article 50(2) machine readable marking | 2 December 2026 for systems on the market before 2 August 2026; from the outset thereafter | Probably. See Finding 4. |
| Annex III high risk obligations | 2 December 2027, deferred by Regulation (EU) 2026/1744 | Only on the alternative classification. |

Regulation (EU) 2026/1744, the Digital Omnibus on AI, was published in the Official Journal on 24 July 2026 and entered into force on 27 July 2026. The Commission adopted guidelines on the Article 50 obligations on 20 July 2026, complemented by the AI Office's Code of Practice on Transparency of AI-generated Content.

**Why the timeline matters more than the tier.** Even on the alternative reading that this system is high risk, the Annex III obligations do not bite until December 2027. Article 50 was not deferred. The obligations that apply today are identical under either classification, so the classification argument should not delay the disclosure work.

## 4. Risk classification

| Question | Answer |
|---|---|
| Prohibited practice under Article 5? | No. All eight limbs screened. |
| Operates in an Annex III area? | Contested. Determination: no. |
| If Annex III: significant influence or preparatory? | Preparatory, and the Article 6(3) derogation applies independently. |
| Interacts with end users or generates content requiring disclosure? | Yes. Article 50(1), and probably 50(2). |
| **First pass tier** | **Limited risk, Article 50 transparency obligations** |

**Article 5.** Not engaged on any limb. One point deserves recording rather than silent dismissal: the system is designed to speak in the voice of a specific named person to someone who may not know they are talking to software. That adjacency to deception is why Article 50(1) applies with force. It does not reach Article 5(1)(a), which requires a manipulative technique that materially distorts behaviour and causes significant harm.

**Annex III(4)(a).** The provision covers AI systems intended to be used for the recruitment or selection of natural persons, in particular to place targeted job advertisements, to analyse and filter job applications, and to evaluate candidates. **Determination: not caught.** Every limb describes a system acting on a population of candidates. This system acts on recruiters and presents exactly one candidate. The natural persons who interact with it are not the subjects of any assessment it performs; the only person profiled by the knowledge base is the provider himself. The harm the provision targets, an individual subjected to automated evaluation in a decision affecting their livelihood, is structurally absent.

**Consequence check.** If 4(a) caught this system, a job seeker could not lawfully publish a chatbot answering questions about their own CV without a conformity assessment, a declaration of conformity, CE marking and EU database registration. A reading that produces that outcome has taken a wrong turn.

**Contrary reading, recorded.** A purposive reading focused on influence over the hiring decision rather than on who is assessed would capture any AI deliberately inserted into a hiring workflow. Not frivolous, untested, not adopted here.

**Article 6(3) fallback.** If the contrary reading were adopted, the derogation applies independently: preparatory task ahead of a human assessment, no score or ranking, no profiling of natural persons. Article 6(4) requires that assessment to be documented before the system is put into service, which this document satisfies.

**Article 50.** Engaged. 50(1) applies to systems intended to interact directly with natural persons. The exemption for cases where the AI nature is obvious cannot be relied on by a system engineered to reproduce one named individual's voice: engineering the ambiguity forfeits the argument that it does not exist. 50(2) marking probably applies since the agent authors substantive text. 50(3) and 50(4) are not engaged.

**Uncertainty.** Confidence in "not Annex III" is moderate, not high. Q1 and Q5 in Section 9 would firm it up.

**Bottom line.** On the current facts this is a limited risk AI system subject to Article 50 transparency duties, not to the Chapter III high risk regime, and it is not high risk despite operating in a hiring context because it assesses no one other than the person who built it.

## 5. Role map

| Role | Party | Basis and key obligations |
|---|---|---|
| **AI system provider** | John Adams | Art 3(3). Develops the system and puts it into service under his own name. Owes Art 50(1) disclosure by design, Art 50(2) marking subject to Finding 4, Art 4 AI literacy, and the Art 6(4) documented assessment. No conformity assessment, CE marking, registration or quality management system at this tier. |
| **Deployer** | John Adams | Art 3(4). Uses it under his own authority. Owes Art 50 disclosure at the point of interaction and Art 4 AI literacy. |
| **GPAI model provider** | OpenAI | Chapter V obligations rest with OpenAI. None flow downstream. |
| Importer, distributor, authorised representative | None | No distribution chain; provider is EU established, so Art 22 does not apply. |
| Third party vendors | Pinecone, Cohere, Calendly, Resend, n8n hosting | Not providers of this AI system. Their obligations are contractual and, for personal data, under Art 28 GDPR. |
| Affected persons | Recruiters and hiring managers using the widget | Protected by Art 50, not by Chapter III. |

**Article 25 note.** The provider builds on gpt-5-mini through an API. He does not fine tune, modify, or place the model on the market under his own name, so Article 25 does not convert him into a provider of the model. He should nonetheless record model and embedding versions, because a silent upstream model change alters system behaviour and there is no other record of what the system was running when.

**Structural observation.** Provider and deployer are the same natural person. The Act's architecture assumes these roles sit at arm's length, with the deployer acting as a check on the provider. That check does not exist here. This report and the debrief are the only external scrutiny in the system's lifecycle.

## 6. Obligations register

Status key: **Met**, **Partial**, **Absent**, **Open**, **N/A**.

| ID | Obligation | Source | Status |
|---|---|---|---|
| O1 | Design the system so persons are informed they are interacting with an AI | Art 50(1) | Absent |
| O2 | Provide that information clearly and distinguishably at the first interaction | Art 50(5) | Absent |
| O3 | Mark outputs in a machine readable format as artificially generated | Art 50(2) | Open |
| O4 | Sufficient AI literacy among persons operating the system | Art 4 | Met in substance, unevidenced |
| O5 | Document the Article 6(3) assessment before putting into service | Art 6(4) | Met by this document |
| O6 | Conformity assessment, declaration of conformity, CE marking, EU registration | Arts 43, 47, 48, 49 | N/A at this tier |
| O7 | Risk management, data governance, technical documentation, logging, human oversight, accuracy | Arts 9 to 15 | N/A at this tier. Logging and error handling exist voluntarily, which is useful evidence if the tier is ever challenged |
| O8 | Quality management system, documentation retention, corrective action, cooperation | Arts 17 to 21 | N/A at this tier |
| O9 | Serious incident reporting | Art 73 | N/A at this tier |

## 7. Compliance findings

### 7.1 Finding 1 — Article 50(1) AI disclosure

**In one line:** users are not told they are talking to an AI, and the system is built to sound like a specific real person.
**Severity: Significant.**
**Description.** The system stands in for a named real person and draws on a cover letter voice and identity corpus. No disclosure appears anywhere in the documentation. The obligation has applied since 2 August 2026.
**Recommended action.** Four concrete parts. Placement: disclosure in the chat header or opening message, reaching the user before their first message. Wording: a plain statement that this is an AI trained on John's CV and that John is not on the other end, not "AI assistant" in small grey type. Robustness: a system prompt instruction, given explicit priority over the voice instruction, that the agent answers truthfully when challenged on identity. Evidence: a screenshot at first load and a transcript of an identity challenge. The design tension is worth naming: the value of the system is that it sounds like John, the obligation is that it must not be mistaken for John, and those are compatible only if the identity boundary is designed in rather than left to the model's discretion.
**Escalation needed?** No.

### 7.2 Finding 2 — Unbounded email tool operating under the provider's identity

**In one line:** if the agent picks the email recipient, a public webhook can send mail under John's identity from untrusted input.
**Severity: Blocking, pending the answer to Q2.**
**Description.** The agent holds a Resend send tool described as sending email on the end user's behalf, behind a public webhook, with no documented prompt injection defence. If the recipient address is agent selected from conversation input, the system is a public relay emitting mail under a named individual's identity, driven by untrusted text. The provider's own stated limitation, that a tool reporting success on silently wrong output goes undetected, removes the compensating control. This is not an AI Act obligation. It is the highest severity item in the review.
**Recommended action.** Pin the recipient at the node level rather than in the prompt. If outbound mail to third parties is intended, add an explicit confirmation step and rate limiting. Full plan in `06_work_plan.md`.
**Escalation needed?** Yes, to the provider before any public URL is shared or any live demo.

### 7.3 Finding 3 — Accuracy of claims about a real person, and unreviewed consequential actions

**In one line:** a hallucinated credential is a misrepresentation to an employer, and the system books and emails with no human check.
**Severity: Significant.**
**Description.** The system makes factual claims about a real person's employment history and qualifications to an audience making a hiring decision. It also books meetings and sends mail on the basis of conversation input, with no oversight point. Not an AI Act obligation at this tier; Article 14 human oversight would apply on the high risk reading.
**Recommended action.** Constrain the agent to retrieved context with an explicit refusal path when retrieval returns nothing. Add factual accuracy checks to the sample conversations already in the repository. Log tool call inputs and outputs alongside the conversation so a wrong booking is reconstructable.
**Escalation needed?** No.

### 7.4 Finding 4 — Article 50(2) marking of synthetic content

**In one line:** the system authors substantive text and may owe machine readable marking by 2 December 2026.
**Severity: Minor, applicability to be confirmed.**
**Description.** Article 50(2) requires providers of systems generating synthetic text to mark outputs in a machine readable format. The carve out for assistive functions that do not substantially alter input data does not fit an agent authoring substantive answers. Scope for one to one conversational output is unsettled and the Commission guidelines of 20 July 2026 have not been reviewed in detail.
**Recommended action.** Confirm applicability against the guidelines, then implement per the Code of Practice if in scope. Determine which side of 2 August 2026 the system was placed on the market, since that decides whether the deadline is 2 December 2026 or immediate.
**Escalation needed?** No.

### 7.5 Finding 5 — AI literacy and model versioning unevidenced

**In one line:** two cheap obligations are met in substance and recorded nowhere.
**Severity: Minor.**
**Description.** Article 4 has applied since 2 February 2025. The provider built the system, so the duty is met in substance, but an unevidenced obligation reads as an unmet one. Separately, model and embedding versions are not recorded, so an upstream change would be invisible.
**Recommended action.** One line each in the repository documentation.
**Escalation needed?** No.

### 7.6 Parallel legal issues, outside the scope of this memo

Flagged, not analysed. Each is material and none is an AI Act obligation.

| Issue | Severity | Note |
|---|---|---|
| No Article 13 GDPR notice; no defined retention for `chat_log` or `error_log` | Significant | Every turn is persisted; bookings and email capture names and addresses; no controller identity, lawful basis, or retention period appears anywhere. Error alerts additionally forward user content into a second system. |
| No Article 28 processor contracts or Chapter V transfer basis recorded | Significant | Five US established processors handle end user data. A one page register closes it. |
| Third parties named in the knowledge base | Open | If `kb/narrative/` names former colleagues or managers, they are data subjects who consented to nothing. Q5 resolves. |
| Calendly and Resend terms of service | Open | Govern automated use and outbound mail. Not reviewed. |

## 8. Overall recommendation

**Proceed with conditions.**

The system is limited risk and contains no design level defect requiring redesign. The engineering discipline is above what the tier demands: credentials held outside the repository, centralised error handling with two entry points, and an honest written limitations section that made this review easier and better. The conditions are narrow. Before public exposure: confirm the email tool cannot address arbitrary recipients (Finding 2), add the Article 50 disclosure with the identity instruction (Finding 1), and publish a privacy notice with a stated retention period (Section 7.6). Findings 3 through 5 should begin immediately but do not gate a demo. If the answer to Q2 is that the recipient is agent controlled and unconstrained, this recommendation drops to **do not proceed** until that is fixed, which is a single node configuration change rather than a redesign.

On enforcement: non compliance with Article 50 carries fines up to EUR 15 million or 3 percent of worldwide annual turnover, and for a natural person running a portfolio project the practical enforcement risk is negligible. The reason to comply is different in kind. This system exists to demonstrate professional competence to people who hire. The compliance work is cheap and it is part of the demonstration rather than a tax on it.

## 9. Clarifying questions log

Questions put to the provider in writing ahead of the debrief. Each provisional assumption is the position this report adopts pending an answer, which is why the report can issue with the questions still open. Record the date sent and any answer received in the final column.

| # | Question | Why it matters | Provisional assumption | Answer received |
|---|---|---|---|---|
| Q1 | Who can reach the bot, and how? Private link behind Basic Auth, or live on the public tunnel? | Decides whether Art 50 and the GDPR obligations are live or theoretical, and whether the Art 2(8) exemption is spent. | Publicly reachable. Audited as a live deployment. |  |
| Q2 | Can the agent choose the email recipient, or is it fixed at the node? | Moves the overall recommendation. Decides whether Finding 2 is blocking. | Agent controlled, since the documentation says "on the end user's behalf". Treated as blocking. |  |
| Q3 | What is the fifth tool, and is there any injection defence or input validation? | The documentation says five tools and lists four. Obligations attach to what a system can do, not to what its docs list. | Documentation error, and no defence beyond the system prompt. |  |
| Q4 | Is there any AI disclosure in the interface, and may the agent claim to be John? | Directly determines Art 50(1) compliance. | No disclosure. Audited as absent. |  |
| Q5 | What does `chat_log` store, for how long, and does the knowledge base name third parties? | Retention, notice, and whether non consenting data subjects appear in the corpus. | Full transcript retained indefinitely, no notice, employer names only. |  |

## 10. Remediation roadmap

**Before any public exposure, including a live demo**

| Action | Reference | Effort |
|---|---|---|
| Confirm and pin the Resend recipient | Finding 2 | Under half a day |
| AI disclosure in the chat interface | Finding 1 | Under an hour |
| Identity instruction in the system prompt, prioritised over the voice instruction | Finding 1 | Minutes |
| Capture the screenshot and identity challenge transcript | Finding 1 | Minutes |
| Privacy notice with stated retention | Section 7.6 | Two hours |

**Within 30 days**

| Action | Reference | Effort |
|---|---|---|
| Confirm Article 50(2) applicability | Finding 4 | Two hours |
| Record model and embedding versions, and the AI literacy line | Finding 5 | Fifteen minutes |
| Constrain the agent to retrieved context; add accuracy checks | Finding 3 | Half a day |
| Processor register: DPA and transfer basis per vendor | Section 7.6 | Two hours |
| Commit this document to the repository as the Article 6(4) record | O5 | Immediate |

**By 2 December 2026.** Article 50(2) marking if in scope and if the system was placed on the market before 2 August 2026.

## 11. Residual risks accepted

- Classification risk on the contrary reading of Annex III(4)(a). Accepted on the strength of the Article 6(3) fallback and the December 2027 deferral.
- No quality management system and no post market monitoring plan. Not required at this tier.
- Possible over compliance on Article 50(2) if marking is implemented and later proves unnecessary. Low cost.

## 12. Reclassification triggers

This determination holds only while the design holds. Revisit before deployment if any of the following occur:

1. The system begins to assess anyone other than the provider: screening inbound messages, scoring opportunities, ranking employers. This reverses the assessment direction and puts Annex III(4)(a) genuinely in play.
2. The system is offered to other job seekers as a product. The provider becomes a provider to third party deployers and the self dealing structure disappears. This is the most likely trigger, because it is the obvious next step for a project that works.
3. Voice or video output is added. Article 50(4) engages on a stricter footing.
4. The system starts making or recommending decisions rather than answering questions.
5. A material upstream model change. Not a reclassification in itself, but a prompt to re run the screen.

## 13. Provider response and agreed action

Following review of this memorandum on 18 August 2026, the provider accepted Finding 1 and agreed to add a disclosure at the point of interaction stating that the user is interacting with an AI system built on a large language model. The identity instruction described in Finding 1 was not separately confirmed, so O1 is recorded as agreed and pending implementation rather than closed.

## 14. Appendix: Phase 1 annotated read

Elements marked on the second reading of the source material. **[T]** tier relevant, **[?]** unclear, **[O]** obligation trigger.

- **[T]** "Stands in for a first coffee chat with me (John), so a recruiter can ask about his work history." The system sits inside a recruitment process. The single most tier relevant sentence in the source.
- **[T]** The direction of assessment runs candidate to recruiter. It screens, scores and filters no one.
- **[O]** "Stands in for" plus a cover letter voice and identity corpus. Article 50(1) trigger.
- **[T]** CliftonStrengths results in `kb/facts/`. Psychometric material about a natural person, who is the provider himself. Would be a profiling problem if the subject were anyone else.
- **[?]** Does `kb/narrative/` name third parties?
- **[T]** "A LangChain agent with five tools." Agentic, not merely generative. It takes actions in the world.
- **[O][?]** Resend "sends email on the end user's behalf." The most consequential and least specified line in the source.
- **[?]** Five tools stated, four listed. An unenumerated tool in an agentic system is an audit gap by definition.
- **[?]** No mention of prompt injection handling or input validation. The webhook is public facing.
- **[O]** Every turn logged to `chat_log`, with no retention period, lawful basis or notice stated anywhere.
- **[O]** Five US processors handling end user data.
- **[T][?]** The provider's own admission that a node reporting success on silently wrong output goes undetected. A human oversight question, not just an engineering one.
- Governance posture above the tier: credentials outside the repository, Basic Auth on the widget, centralised error handling, a written limitations section. No written risk classification anywhere.

## 15. What this report is not

This report is not a legal opinion, not a conformity assessment, and not a certification. It was prepared by a non lawyer, from the information available at the time of writing, without access to the running system or its workflow definitions, and with five clarifying questions outstanding at issue. It addresses the EU AI Act; data protection, consumer protection and vendor contractual terms are expressly outside its substantive scope and are flagged rather than analysed. Legal positions reflect the regulation as it stands on 18 August 2026, including the amendments made by Regulation (EU) 2026/1744. Conclusions should be verified with qualified counsel before any EU market placement or public exposure.

**Sources for the timeline in Section 3:** Regulation (EU) 2024/1689; Regulation (EU) 2026/1744 (Digital Omnibus on AI), published in the Official Journal 24 July 2026, in force 27 July 2026; European Commission guidelines on Article 50 transparency obligations, adopted 20 July 2026; Code of Practice on Transparency of AI-generated Content, AI Office.
