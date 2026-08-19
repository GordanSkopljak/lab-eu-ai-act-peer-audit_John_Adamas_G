# Classification, role map and obligation checklist

**System:** Virtual Coffee Chat Bot · **Builder:** John Adams · **Reviewer:** Gordan · **Date:** 18 August 2026
**Relationship to other files:** working annex to `04_audit_report.md`. The report states the conclusions in prose; this file shows the determination step by step and screens the system against every obligation, including those that do not apply. A determination that only lists what applies cannot be checked. One that lists what was ruled out, and why, can be.

Status key: **Met** · **Partial** · **Absent** · **N/A** (obligation does not attach) · **Open** (cannot be assessed on available evidence)

---

# Part A: Risk classification

## A1. Decision table

| Question | Answer | Governing provision |
|---|---|---|
| Prohibited practice? | No | Art 5 |
| Annex III area? | Contested. Determination: no | Annex III(4)(a) |
| If Annex III: significant influence or narrow / preparatory? | Preparatory. Derogation available independently | Art 6(3) |
| Interacts directly with natural persons? | Yes | Art 50(1) |
| Generates synthetic content? | Yes, text | Art 50(2) |
| Deepfake or public interest text? | No | Art 50(4) |
| **Determination** | **Limited risk. Article 50 transparency obligations** | |

## A2. Article 5 screen

| Prohibited practice | Engaged? | Note |
|---|---|---|
| Subliminal, manipulative or deceptive techniques causing significant harm, Art 5(1)(a) | No | The system speaks in a named person's voice to someone who may not know they are talking to software. That adjacency to deception is why Art 50(1) applies with force. It does not reach Art 5(1)(a), which requires material distortion of behaviour plus significant harm. |
| Exploiting vulnerability, Art 5(1)(b) | No | |
| Social scoring, Art 5(1)(c) | No | |
| Criminal risk prediction, Art 5(1)(d) | No | |
| Untargeted facial scraping, Art 5(1)(e) | No | |
| Emotion inference in workplace or education, Art 5(1)(f) | No | Sentiment is not inferred. Thumbs up or down feedback is user supplied, not machine inferred, so it does not engage this limb. |
| Biometric categorisation, Art 5(1)(g) | No | |
| Real time remote biometric identification, Art 5(1)(h) | No | |

## A3. Annex III(4)(a) analysis

The provision covers AI systems intended to be used for the recruitment or selection of natural persons, in particular to place targeted job advertisements, to analyse and filter job applications, and to evaluate candidates.

| Limb | Does the system do this? | Reasoning |
|---|---|---|
| Place targeted job advertisements | No | It markets a candidate, not a vacancy. No targeting of any audience segment. |
| Analyse and filter job applications | No | It receives no applications. |
| Evaluate candidates | No | It evaluates no one. It answers questions about one person, who is the operator. |

**Determination: not caught.** Every limb describes a system acting on a population of candidates. This system acts on recruiters and presents exactly one candidate. The natural persons it interacts with are not the subjects of any assessment. The harm the provision targets, an individual subjected to automated evaluation in a decision affecting their livelihood, is structurally absent: the only livelihood affected belongs to the person who built and controls the system.

**Contrary reading, recorded.** A purposive reading focused on influence over the hiring decision rather than on who is assessed would capture any AI deliberately inserted into a hiring workflow. Not frivolous. Untested. Not adopted here.

**Article 6(3) fallback.** If the contrary reading were adopted, the derogation applies independently: preparatory task ahead of a human assessment, no score or ranking produced, no profiling of natural persons. Two independent routes lead away from high risk.

## A4. Article 50 screen

| Limb | Engaged? | Basis |
|---|---|---|
| 50(1) direct interaction with natural persons | **Yes** | Public chat interface. The exemption for cases where the AI nature is obvious cannot be relied on by a system engineered to reproduce one named individual's voice. |
| 50(2) machine readable marking of synthetic content | **Probably. Open** | The system authors substantive text. The exception for assistive functions not substantially altering input does not fit. Scope for one to one conversational output is not settled and the Commission guidelines of 20 July 2026 have not been reviewed. |
| 50(3) emotion recognition or biometric categorisation | No | Not present. |
| 50(4) deepfakes and public interest text | No | No synthetic audio, image or video. Text is not published to inform the public on a matter of public interest. |

## A5. Uncertainty and what would resolve it

| Uncertainty | Resolved by | Effect if resolved the other way |
|---|---|---|
| Annex III(4)(a) scope | Q1 and Q5 in the clarifying log; ultimately regulatory guidance | Tier becomes high risk. See Part C2. Practical effect on the current action list is nil, because the Annex III obligations are deferred to 2 December 2027. |
| Article 50(2) applicability | Commission Art 50 guidelines, adopted 20 July 2026 | Adds a marking obligation with a 2 December 2026 deadline for systems already on the market at 2 August 2026. |
| Whether the system is publicly reachable | Q1 | Private demo only would reduce the GDPR obligations to near nil and make Art 50 a formality. |

---

# Part B: Role map

## B1. Roles

| Role | Party | Basis | Note |
|---|---|---|---|
| Provider | John Adams | Art 3(3). Develops the system and puts it into service under his own name. | |
| Deployer | John Adams | Art 3(4). Uses it under his own authority. | Same natural person as provider. |
| Importer / distributor | None | | Provider is EU established and there is no distribution chain. |
| Authorised representative | N/A | Art 22 | Provider is established in the Union. |
| GPAI model provider | OpenAI | Chapter V | Obligations rest with OpenAI. None flow downstream to this operator. |
| Affected persons | Recruiters and hiring managers using the widget; any third party named in the knowledge base | | Their protections arise under GDPR and Art 50, not under Chapter III. |
| Controller (GDPR) | John Adams | Art 4(7) GDPR | |
| Processors (GDPR) | OpenAI, Pinecone, Cohere, Calendly, Resend, n8n hosting | Art 28 GDPR | |

## B2. Obligations by role

| Role | Obligations that attach at this tier |
|---|---|
| Provider | Art 50(1) disclosure by design. Art 50(2) marking, subject to A4. Art 4 AI literacy. No conformity assessment, registration, CE marking, or quality management system. |
| Deployer | Art 50 disclosure at the point of interaction. Art 4 AI literacy. |
| GPAI model provider | Not this operator's concern. Record model versions in use so the dependency is documented. |
| Processors | Art 28 GDPR contracts and a Chapter V transfer basis, evidenced by the controller. |
| Controller | Full GDPR stack. See Part C1. |

## B3. Structural note

Provider and deployer are the same natural person. The Act's architecture assumes these roles sit at arm's length, with the deployer acting as an external check on the provider. That check does not exist here. This review, the audit report, and the debrief are the only external scrutiny in the system's lifecycle, which is an argument for keeping them on file rather than treating them as coursework.

---

# Part C: Obligation checklist

## C1. Obligations that apply

### AI Act

| ID | Obligation | Source | Applies from | Status | Action |
|---|---|---|---|---|---|
| A1 | Inform natural persons they are interacting with an AI system, by design | Art 50(1) | 2 Aug 2026 | Absent | Persistent disclosure in the interface. Prompt level instruction forbidding the agent from asserting it is John. |
| A2 | Disclosure given clearly and distinguishably at the first interaction | Art 50(5) | 2 Aug 2026 | Absent | Visible before the first user message, not on request only. |
| A3 | Mark synthetic content in machine readable form | Art 50(2) | 2 Dec 2026 if placed on market before 2 Aug 2026; otherwise from placement | Open | Confirm scope, then implement per the Code of Practice on Transparency of AI-generated Content. |
| A4 | AI literacy among persons operating the system | Art 4 | 2 Feb 2025 | Met in substance | Record it in one line. An unevidenced obligation reads as an unmet one. |

### GDPR

| ID | Obligation | Source | Status | Action |
|---|---|---|---|---|
| G1 | Lawful basis identified and documented | Art 6(1)(f) | Absent | Legitimate interests assessment, one page. Consent is a poor fit; the processing is not optional to the service. |
| G2 | Transparency notice at collection | Art 13 | Absent | Short notice linked from the interface: controller, purposes, basis, recipients, transfers, retention, rights including Art 21 objection. |
| G3 | Purpose limitation and minimisation | Art 5(1)(b), 5(1)(c) | Partial | Transcript logging is proportionate. Forwarding user content into error alert emails is not. Truncate or hash. |
| G4 | Storage limitation | Art 5(1)(e) | Absent | Stated retention for `chat_log` and `error_log`. Twelve months is a defensible default. Evidence the deletion. |
| G5 | Processor contracts | Art 28 | Absent | One page register: which published DPA is in force per vendor. No negotiation required. |
| G6 | International transfer mechanism | Chapter V | Absent | Record DPF certification or standard contractual clauses per vendor. All five are US established. |
| G7 | Data subject rights route | Arts 15 to 22 | Absent | A contact address in the notice is sufficient at this scale. |
| G8 | DPIA screening | Art 35 | Absent as a record; not required in substance | Not large scale, no systematic monitoring of a public area, no third party special category data. Record the screening conclusion. |
| G9 | Security of processing | Art 32 | Partial | Credentials held outside the repository and Basic Auth on the widget are good. No documented handling of prompt injection or of the email tool's recipient scope. |
| G10 | Records of processing | Art 30 | Absent | Art 30(5) likely exempts an operation of this size, but the processor register in G5 covers the same ground for less effort. |

### Adjacent

| ID | Issue | Status | Action |
|---|---|---|---|
| X1 | Accuracy of claims about a real person made to prospective employers | Partial | Constrain the agent to retrieved context with an explicit refusal path. Add accuracy checks to the existing sample conversations. |
| X2 | Consequential actions taken without human review | Partial | Log tool call inputs and outputs alongside the conversation so a wrong booking is reconstructable. |
| X3 | Email recipient scope | Open, treated as high severity | Pin the recipient at the node. See `06_work_plan.md`. |
| X4 | Vendor terms of service, Calendly and Resend | Open | Not reviewed. Flagged. |

## C2. Contingency: the high risk provider obligations

Run as a contingency only. These do **not** apply on the determination in Part A. They are screened here because a determination that has never been tested against the obligations it avoids is an assertion, not an analysis, and because John may have classified the system high risk in his self audit. If he did, this is the table to work through together at the debrief.

Note on timing: even on the high risk reading, none of these bite until **2 December 2027**, following the deferral introduced by Regulation (EU) 2026/1744. Nothing in this column is urgent under either classification.

| # | Provider obligation | Source | Would the current build satisfy it? |
|---|---|---|---|
| 1 | Meet the Chapter III Section 2 requirements | Art 16(a) | No. See rows 12 to 18 below. |
| 2 | Indicate name and contact details on the system or its documentation | Art 16(b) | Partial. Author named in the README, no contact point in the interface. |
| 3 | Quality management system | Art 17 | Absent. Disproportionate for a portfolio project. |
| 4 | Keep technical documentation and QMS documentation for 10 years | Art 18 | Partial. Documentation is unusually good for the tier; no retention commitment. |
| 5 | Keep automatically generated logs | Art 19 | Partial and better than expected. `chat_log` and `error_log` already exist voluntarily. This is the strongest evidence in the build. |
| 6 | Corrective action and duty to inform | Art 20 | Absent. No withdrawal or recall path, which is close to meaningless for a single operator system. |
| 7 | Cooperate with competent authorities | Art 21 | N/A until asked. |
| 8 | Conformity assessment before placing on the market | Art 43 | Absent. Blocking on the high risk reading. |
| 9 | EU declaration of conformity | Art 47 | Absent. |
| 10 | CE marking | Art 48 | Absent. |
| 11 | Registration in the EU database | Art 49 | Absent. |
| 12 | Risk management system | Art 9 | Absent as a system. The written known limitations section is a fragment of one. |
| 13 | Data and data governance | Art 10 | Partial. Knowledge base is curated and split into facts and narrative with separate chunking, which is more governance than most builds at this scale. |
| 14 | Technical documentation per Annex IV | Art 11 | Partial. |
| 15 | Record keeping | Art 12 | Partial. See row 5. |
| 16 | Transparency and information to deployers | Art 13 | N/A in substance. Provider and deployer are the same person. |
| 17 | Human oversight | Art 14 | Absent, and the material gap. The system takes consequential actions with no oversight point, in a design whose author states that silently wrong tool output goes undetected. |
| 18 | Accuracy, robustness, cybersecurity | Art 15 | Absent as evidence. Cohere reranking improves retrieval quality but no accuracy measurement exists, and no injection defence is documented. |

**Reading this table.** If the high risk classification were correct, the system could not be placed on the market: rows 8 through 11 are unmeetable for a solo builder, and row 17 is a genuine design gap rather than a paperwork one. That consequence is itself an argument for the limited risk determination. A reading of Annex III that makes it unlawful for a job seeker to build a chatbot about their own CV is a reading that has taken a wrong turn somewhere. Worth saying out loud at the debrief, because it is the most persuasive form of the argument.

---

## Enumeration note

The Article 16 provider obligations are enumerated differently across sources; some course materials count 11, others 12 or 13 depending on how Article 16(a) is unpacked against Articles 9 to 15. This table lists them all rather than forcing a count. If your course material uses a fixed list of 11, map rows 1 to 11 to it and treat rows 12 to 18 as the expansion of row 1.
