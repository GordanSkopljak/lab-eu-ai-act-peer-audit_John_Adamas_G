# Compliance memorandum: EU AI Act

**To:** John Adams, provider and deployer, Virtual Coffee Chat Bot

**From:** Gordan, external reviewer

**Date:** 18 August 2026

**Re:** EU AI Act compliance position, Virtual Coffee Chat Bot

**Status:** Advisory. Not a legal opinion. See Section 14.

---

## 1. Purpose and scope

This memo records the EU AI Act compliance position for the Virtual Coffee Chat Bot: what the system is under Regulation (EU) 2024/1689, which obligations attach, which are currently met, and what has to happen before public exposure. It is the durable classification artifact that Finding 6 of the accompanying audit report called for.

**Scope is limited to the AI Act.** Data protection is deliberately excluded. That is a scoping decision, not an oversight, and it is stated here so it does not read as one. The system processes third party personal data and the GDPR analysis is material: it is covered in Findings 3 and 4 of `04_audit_report.md` and in Part C1 of `04a_classification_role_map_obligations.md`. Nothing in this memo should be read as a view that the GDPR position is clean. Consumer protection and vendor terms of service are likewise out of scope and are flagged in the audit report.

Evidence base is the public project documentation. No access to the running system or the exported workflow definitions. Five clarifying questions remain outstanding.

## 2. Summary position

The system is **limited risk**. Its obligations arise under Article 50, not under the high risk regime of Chapter III.

Three consequences, and the third is the one most operators get wrong:

1. There is no conformity assessment, no CE marking, no EU database registration, no quality management system, and no notified body in this system's future as currently designed.
2. The Article 50 transparency obligations are **live now**. They began to apply on 2 August 2026, two weeks before the date of this memo. This is not a future compliance project.
3. The classification argument matters less to the immediate action list than it appears. Even on the alternative reading that the system falls inside Annex III(4)(a) and is high risk, Regulation (EU) 2026/1744 deferred the Annex III obligations to 2 December 2027. Article 50 was not deferred. The obligations that bite today are identical under either classification. Resolve the classification for the record, but do not let the argument delay the disclosure work.

## 3. Territorial and material scope

| Question | Answer |
|---|---|
| Is this an AI system within Article 3(1)? | Yes. Machine based system inferring from input how to generate outputs, with a degree of autonomy, taking actions through tools. |
| Is the Act territorially engaged? | Yes. The provider is established in the Union and the system is put into service in the Union. Article 2(1). |
| Does any exemption apply? | No. The research and development exemption in Article 2(8) covers activity prior to placing on the market or putting into service. Once the widget is exposed to third parties for a professional purpose, it is in service and the exemption is spent. A system that only ever runs in a local demo to its own author is arguably still in the exemption; Q1 in the clarifying log resolves this. |
| Personal or household activity exemption? | Not available. There is no household exemption in the AI Act, and the purpose is professional. |

## 4. Regulatory timeline

| Obligation set | Applies from | Relevant here |
|---|---|---|
| Article 5 prohibitions | 2 February 2025 | Screened. Not engaged. |
| Article 4 AI literacy | 2 February 2025 | Yes. Applies to providers and deployers. Not deferred. |
| GPAI model obligations, Chapter V | 2 August 2025 | Sit with OpenAI, not with this operator. |
| Article 50 transparency | 2 August 2026 | **Yes. Live.** |
| Article 50(2) machine readable marking | 2 December 2026 for systems placed on the market before 2 August 2026; from the outset for systems placed on the market on or after that date | Probably. See Obligation O3. |
| Annex III high risk obligations | 2 December 2027, deferred by Regulation (EU) 2026/1744 | Only on the alternative classification. Not the operating assumption. |
| Annex I embedded high risk | 2 August 2028 | Not applicable. |

Regulation (EU) 2026/1744, the Digital Omnibus on AI, was published in the Official Journal on 24 July 2026 and entered into force on 27 July 2026. The European Commission adopted guidelines on the Article 50 transparency obligations on 20 July 2026, complemented by the AI Office's Code of Practice on Transparency of AI-generated Content. Neither has been reviewed in detail for this memo.

## 5. Classification determination

### 5.1 Article 5, prohibited practices

Screened across all eight limbs. Not engaged. The full screen is tabulated in `04a_classification_role_map_obligations.md`, Part A2.

One point deserves recording rather than silent dismissal. The system is designed to speak in the voice of a specific named person to someone who may not know they are talking to software. That adjacency to deception is precisely why Article 50(1) applies with force. It does not reach Article 5(1)(a), which requires a manipulative or deceptive technique that materially distorts behaviour and causes or is likely to cause significant harm. Identity ambiguity in a first contact recruiting conversation does not meet that threshold.

### 5.2 Annex III(4)(a), employment and recruitment

Annex III point 4(a) covers AI systems intended to be used for the recruitment or selection of natural persons, in particular to place targeted job advertisements, to analyse and filter job applications, and to evaluate candidates.

**Determination: not caught.** The reasoning, on the record:

- Every limb of 4(a) describes a system acting on a population of candidates. This system acts on recruiters and presents exactly one candidate.
- The natural persons who interact with the system are not the subjects of any assessment it performs. The only person profiled by the knowledge base is the operator himself.
- The harm the provision targets, an individual subjected to automated evaluation in a decision affecting their livelihood, is structurally absent. The only livelihood affected belongs to the person who built and controls the system.
- Consequence check. If 4(a) caught this system, a job seeker could not lawfully publish a chatbot answering questions about their own CV without a conformity assessment, a declaration of conformity, CE marking, and registration in the EU database. A reading that produces that outcome has taken a wrong turn. This is the most persuasive form of the argument and should be led with.

**Contrary reading, recorded for completeness.** A purposive reading focused on influence over the hiring decision rather than on who is assessed would capture any AI deliberately inserted into a hiring workflow. That reading is not frivolous and has not been tested. This memo does not adopt it, but the operator should know it exists rather than meet it unprepared.

**Article 6(3) fallback.** If the contrary reading were adopted, the derogation applies independently. The system performs a preparatory task ahead of a human assessment; a recruiter reads its output and forms their own view. It produces no score, ranking, or recommendation, and it does not profile natural persons within the meaning of Article 6(3). Two independent routes therefore lead away from high risk. Article 6(4) requires the assessment to be documented before the system is put into service, which this memo satisfies.

### 5.3 Article 50, transparency

| Limb | Engaged | Basis |
|---|---|---|
| 50(1) direct interaction | **Yes** | Public chat interface. The exemption for cases where the AI nature is obvious to a reasonably well informed and observant person cannot be relied on by a system engineered to reproduce one named individual's voice and identity. Engineering the ambiguity forfeits the argument that the ambiguity does not exist. |
| 50(2) marking of synthetic content | **Probably. Open** | The system authors substantive text. The carve out for assistive functions that do not substantially alter input data or its semantics does not fit. Scope for one to one conversational output is unsettled. |
| 50(3) emotion recognition, biometric categorisation | No | Not present. Thumbs up or down feedback is user supplied, not machine inferred. |
| 50(4) deepfakes, public interest text | No | No synthetic audio, image or video. Text is not published to inform the public on a matter of public interest. |

**Conclusion. Limited risk. Article 50 transparency obligations apply. No Chapter III obligations attach.**

## 6. Role determination

| Role | Party | Basis |
|---|---|---|
| Provider | John Adams | Art 3(3). Develops the system and puts it into service under his own name. |
| Deployer | John Adams | Art 3(4). Uses it under his own authority. |
| Importer, distributor | None | No distribution chain. Provider is EU established. |
| Authorised representative | N/A | Art 22 applies to third country providers only. |
| GPAI model provider | OpenAI | Chapter V obligations rest with OpenAI. |
| Affected persons | Recruiters and hiring managers using the widget | Protected by Art 50, not by Chapter III. |

**Relationship to the GPAI model.** The operator builds on gpt-5-mini through an API. He does not fine tune, modify, or place the model on the market under his own name, so Article 25 does not convert him into a provider of the model. He is the provider of the AI system; OpenAI remains the provider of the model. He inherits none of the Chapter V obligations. He should nonetheless record model and embedding versions in use, because a silent model swap upstream changes system behaviour and there is no other record of what the system was running when.

**Structural observation.** Provider and deployer are the same natural person. The Act's architecture assumes these roles sit at arm's length, with the deployer acting as a check on the provider. That check does not exist here. This memo, the audit report, and the peer debrief are the only external scrutiny in the system's lifecycle.

## 7. Obligations register

Status key: **Met**, **Partial**, **Absent**, **Open**, **N/A**.

| ID | Obligation | Source | Status | Required action |
|---|---|---|---|---|
| O1 | Design the system so natural persons are informed they are interacting with an AI system | Art 50(1) | Absent | Persistent disclosure in the chat interface, plus a system prompt instruction forbidding the agent from asserting it is John when asked directly. |
| O2 | Provide the information clearly and distinguishably at the latest at the first interaction or exposure | Art 50(5) | Absent | Visible before the first user message. Not in a footer, not only on request. |
| O3 | Mark outputs in a machine readable format detectable as artificially generated | Art 50(2) | Open | Confirm applicability against the Commission guidelines of 20 July 2026. If in scope, implement per the Code of Practice on Transparency of AI-generated Content. |
| O4 | Ensure a sufficient level of AI literacy among persons operating the system | Art 4 | Met in substance | One line on the record. An unevidenced obligation reads as an unmet one. |
| O5 | Document the Article 6(3) assessment before putting the system into service | Art 6(4) | Met by this memo | Keep it in the repository. |
| O6 | Conformity assessment, declaration of conformity, CE marking, EU database registration | Arts 43, 47, 48, 49 | N/A | Not engaged at limited risk. Recorded to close the question rather than leave it open. |
| O7 | Risk management, data governance, technical documentation, logging, human oversight, accuracy and robustness | Arts 9 to 15 | N/A | Not engaged at limited risk. Note that logging and error handling already exist voluntarily, which is useful evidence if the classification is ever challenged. See Part C2 of the annex. |
| O8 | Quality management system, documentation retention, corrective action, cooperation with authorities | Arts 17 to 21 | N/A | Not engaged at limited risk. |
| O9 | Serious incident reporting | Art 73 | N/A | High risk systems only. |

## 8. Implementing Article 50(1) in this system

The obligation is thin in text and specific in practice. Four concrete requirements:

1. **Placement.** The disclosure must reach the user at or before the first interaction. In a chat widget that means the header or the opening message, not a link the user has to find.
2. **Wording.** It must be clear and distinguishable. "AI assistant" in small grey text under the title is weak. A first message that says plainly that this is an AI trained on John's CV and that John himself is not on the other end is strong, and costs nothing.
3. **Robustness.** The disclosure has to survive the conversation. A user who asks "are you a real person" must get a truthful answer. This is a system prompt constraint, and it is the one most likely to fail, because the same prompt also instructs the agent to speak in John's voice. The two instructions pull against each other and the identity instruction must be given priority explicitly.
4. **Evidence.** A screenshot of the interface at first load, and a transcript of the agent answering an identity challenge. Two artifacts, both cheap, and they are what a reviewer would ask for.

The design tension is worth naming directly. The value of this system is that it sounds like John. The obligation is that it must not be mistaken for John. Those are compatible, but only if the identity boundary is designed in rather than left to the model's discretion.

## 9. Enforcement exposure

Non compliance with Article 50 carries fines up to EUR 15 million or 3 percent of worldwide annual turnover, whichever is higher. For a natural person operating a portfolio project, the practical enforcement risk is negligible and this memo does not pretend otherwise.

The real exposure is different in kind. The system exists to demonstrate professional competence to people who hire. A hiring manager in a regulated industry who notices that an AI Act compliance obligation was missed by a project explicitly built to showcase AI engineering draws a conclusion about the builder. The compliance work here is cheap, and it is part of the demonstration rather than a tax on it.

## 10. Residual risks accepted

Noted and consciously accepted rather than remediated, on proportionality grounds:

- Classification risk on the contrary reading of Annex III(4)(a). Accepted on the strength of the Article 6(3) fallback and the deferral of Annex III obligations to December 2027.
- No formal quality management system and no post market monitoring plan. Not required at this tier.
- Article 50(2) scope for conversational text output is unsettled and the operator may implement marking that later proves unnecessary. The cost of over compliance here is low.

## 11. Remediation roadmap

**Before any public exposure, including a live demo on the public endpoint**

| Action | Obligation | Effort |
|---|---|---|
| Persistent AI disclosure in the chat interface | O1, O2 | Under an hour |
| Identity instruction in the agent system prompt, with priority over the voice instruction | O1 | Minutes |
| Capture the two evidence artifacts in Section 8 | O1 | Minutes |

**Within 30 days**

| Action | Obligation | Effort |
|---|---|---|
| Confirm Article 50(2) applicability against the Commission guidelines | O3 | Two hours |
| Record model and embedding versions in the technical documentation | Section 6 | Fifteen minutes |
| Commit this memo to the repository as the classification record | O5 | Immediate |
| One line AI literacy record | O4 | Minutes |

**By 2 December 2026**

Implement Article 50(2) marking if the system falls in scope and was placed on the market before 2 August 2026. If it was placed on the market on or after that date, the obligation applies from the outset and moves into the 30 day block above.

**Not on the AI Act clock but not optional**

The GDPR actions in the audit report, and the email tool recipient scope in `06_work_plan.md`. Neither is an AI Act obligation. Both are more likely to cause actual harm than anything in this memo.

## 12. Reclassification triggers

This determination holds only while the system's design holds. Any of the following requires the classification to be revisited before deployment:

1. **The system begins to assess anyone other than the operator.** Screening inbound recruiter messages, scoring opportunities, or ranking employers reverses the assessment direction and puts Annex III(4)(a) genuinely in play.
2. **The system is offered to other job seekers as a product or service.** The operator becomes a provider to third party deployers, the self dealing structure disappears, and the recruitment context argument strengthens considerably. This is the single most likely trigger, because it is the obvious next step for a project that works.
3. **Voice or video output is added.** Article 50(4) deepfake disclosure engages on a stricter footing than 50(1), and a synthetic voice of a real named person is squarely within it.
4. **The system starts making or recommending decisions rather than answering questions.** For example, auto declining opportunities below a threshold.
5. **Upstream model change with materially different capability.** Not a reclassification in itself, but a prompt to re run the screen.

## 13. Evidence to retain

A limited risk system has no mandatory technical file. Five artifacts nonetheless make the position defensible if anyone asks:

1. This memo, dated, in the repository.
2. Screenshot of the interface showing the disclosure at first load.
3. Transcript of the agent answering an identity challenge truthfully.
4. Record of model and embedding versions in use, with dates.
5. The peer audit report and debrief note, as evidence of external review in a system where provider and deployer are the same person.

## 14. Limitations

This memorandum is not a legal opinion, not a conformity assessment, and not a certification. It was prepared by a non lawyer, from public project documentation, without access to the running system or its workflow definitions, and with five clarifying questions outstanding at the time of issue. It addresses the EU AI Act only; data protection, consumer protection, and vendor contractual terms are expressly out of scope and are covered, in part, elsewhere in this review. Legal positions reflect the regulation as it stands on 18 August 2026, including the amendments made by Regulation (EU) 2026/1744. Any conclusion should be verified with qualified counsel before the system is placed on the EU market or exposed to the public.

**Sources for the timeline in Section 4:** Regulation (EU) 2024/1689; Regulation (EU) 2026/1744 (Digital Omnibus on AI), published in the Official Journal 24 July 2026, in force 27 July 2026; European Commission guidelines on Article 50 transparency obligations, adopted 20 July 2026; Code of Practice on Transparency of AI-generated Content, AI Office.

## 15. Provider response and agreed action

Following review of this memorandum on 18 August 2026, the builder accepted Finding O1 and agreed to add a disclosure at the point of interaction stating that the user is interacting with an AI system built on a large language model, closing the Article 50(1) gap.