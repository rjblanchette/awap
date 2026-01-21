AWAP v1.0
Document: Architecture Overview: AI-Assisted Work Admissibility Packet (AWAP)
Version: v1.0
Author: RJBlanchette
Date: 2025-12-21
License: Creative Commons Attribution 4.0 International (CC-BY 4.0)

Architecture Overview: AI-Assisted Work Admissibility Packet (AWAP)
Purpose
A minimal institutional format gate for work products that used a Large Language Model (LLM), so downstream reviewers can determine provenance, responsibility, and source legibility—without the tool judging content, quality, correctness, or outcomes.

System Shape (What It Is)
A single, closed “packet” of artifacts that must travel with any LLM-assisted work product at the moment it enters an official institutional workflow
(e.g. committee review, grants office, legal review, records system, external release preparation).
    • The tool is not software-first; it may be implemented as a PDF bundle, folder convention, or document attachment with a one-page checklist.
    • It remains useful even if models regress, change, or stagnate, because it is fundamentally documentation + responsibility + source legibility.
    • The system does not evaluate or interact with the work product itself—only with the presence and legibility of the packet.
Trigger condition (self-attested):
AWAP is required when the submitter attests that an LLM was used to generate or materially rewrite any portion of the work product.

Core Components
(The only objects the system recognizes)
AWAP Packet = 8 artifacts (fixed, closed set):
    1. Cover Sheet
What the work product is, and which institutional workflow it is entering.
    2. Use Declaration
How the LLM was used (e.g., drafting, summarization, translation, ideation) or explicitly not used.
Describes how, not why.
    3. Model & Session Log
Model name/version, date(s), and access context (local, institutional account, external service).
    4. Prompt Context (Minimal)
The minimum prompt excerpts required to establish provenance.
Only what is necessary; redactions are permitted and must be explicitly marked.
If fully redacted, a marked stub indicating prompt category (e.g., “drafting,” “summarization”) is sufficient.
    5. Source Trace
Citations used by the human author or an explicit declaration that the draft is unsourced and not intended for external factual reliance.
This is a disclosure artifact, not a sufficiency or accuracy test.
    6. Human Responsibility Statement
A named human accepts responsibility for authorship, representations made, and compliance with applicable institutional requirements.
    7. Edit / Change Note
What was materially altered after the LLM output (additions, removals, rewrites).
    8. Disposition Tag
Draft / Internal Record / External Release Candidate.
Closed set invariant:
If an item is not one of these eight artifacts, it is outside the scope of AWAP.

Single Choke Point
(Where admissibility is checked)
Official Intake — the moment a work product is submitted into an institutional workflow.
Admissibility check is purely clerical and format-based:
    • Are all 8 artifacts present?
    • Are required fields non-empty and legible?
Fail-by-default behavior (non-punitive):
    • Missing or illegible packet ⇒ submission is treated as “not received” and returned for completion.
    • No scoring, no commentary, no evaluation of merit, correctness, or adequacy.
Constraint:
Intake may verify presence and legibility only; it may not request additional artifacts or assess substantive adequacy.

Data Flow (Lifecycle)
    1. Drafting occurs anywhere; LLM use may be extensive, limited, or unknown.
    2. When the work product is ready to enter an official workflow, the submitter attaches an AWAP packet.
    3. Intake checks packet completeness only.
    4. If complete, the work proceeds through normal institutional review processes.
    5. The packet is retained only to the extent the associated work product is retained, under existing records rules
(especially for record copies or external release candidates).

Security and Administrative Posture
(What skeptical readers care about)
    • No automation, monitoring, or model access required.
    • No new data collection beyond what the submitter provides.
    • Redactions are permitted and must be explicitly marked.
    • The tool introduces no new decisions—only a legibility requirement for entry into official workflows.
    • AWAP does not compel disclosure of confidential research, privileged communications, or protected data; marked redactions are sufficient.

Non-Goals
(Explicit guardrails against authority creep)
    • Not a fact-checker, plagiarism detector, or quality gate.
    • Not a policy regime, incentive system, or compliance score.
    • Not an approver; it cannot authorize publication, funding, or action.
    • Not an AI governance program; it standardizes documentation, not behavior.
Invariant:
AWAP completeness does not imply accuracy, approval, endorsement, or institutional responsibility.

Architectural Risk to Watch (Drift)
The primary failure mode is authority creep: intake staff using AWAP to evaluate content, reasoning, or merit rather than packet completeness.
If this occurs, AWAP ceases to be an artifact gate and becomes a governance mechanism—at which point the architecture has been violated.

DXG Pattern Compliance (Declarative)

The AI-Assisted Work Admissibility Packet (AWAP) is a canonical instantiation of the Declared-X Gate (DXG) Pattern.

AWAP instantiates the DXG pattern as follows:

Boundary-based: applies only at the moment a work product enters an official institutional workflow

Declarative: records disclosures of AI assistance and responsibility without evaluation

Non-evaluative: performs no assessment of content, merit, correctness, or adequacy

Authority-preserving: requires a singular named human accepting responsibility

Phase-specific: emitted once, terminally, at a single admissibility boundary

The declared dimension (“X”) instantiated by AWAP is:

Assistance (AI involvement and provenance)

AWAP does not:

verify the accuracy of disclosures

evaluate appropriateness of AI use

authorize publication, funding, or action

AWAP remains a closed, read-only packet whose completeness does not imply endorsement, approval, or institutional responsibility.

DXG compliance explains AWAP’s structure; it does not expand AWAP’s authority or scope.
