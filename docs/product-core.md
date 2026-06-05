# Product Core

## What the product does

LumiSense is a review workspace for teams working through incoming materials in a structured way.

A case is opened. Materials are submitted. Missing information is collected through follow-up questions. Content is processed into a usable form. A summary or report is produced, and the reviewer continues working on the same case without losing context.

Not a replacement for judgement. It cuts time spent chasing missing details and re-reading long files.

## First use case

Inbound review:

- startup or project submissions
- application packs
- supporting documents
- mixed files arriving in inconsistent formats

This is the narrowest, clearest wedge and the one used for the ASPIRE application.

## Initial buyer

The first buyer is a review owner with repeated external submissions: a university entrepreneurship programme lead, accelerator manager, grant programme manager, innovation team lead, diligence lead or similar operator.

They already receive forms, decks, financial models, calls and follow-up material. The pain is that evidence, reviewer questions, criteria and decision history become scattered across tools. LumiSense packages that work as review capacity rather than token usage: cases, indexed source material, transcript hours, published review records and bounded advanced review work for heavier scans, images, audio, video or second-pass checks.

## Who uses it

Three roles:

- Submitter — provides materials and answers follow-up questions
- Reviewer or analyst — works through the case, requests outputs and refines conclusions
- Operator — manages configuration, access and runtime

## Content types

The product handles documents, Office files, images, audio and video. Audio and video are processed through transcripts with temporal anchors, so a cited passage points to a specific moment in the source file.

## How it differs from a generic AI chat

Built around case work rather than one-off prompting. A submission is a case rather than a temporary upload. Outputs carry references back to source material. Review work continues over time with versioned outputs, and the same workspace supports chat-style follow-up and structured reports.

## Memory and context continuity

Memory is part of the case, not a hidden assistant profile. LumiSense separates conversation continuity, reviewer intent, retrieved evidence and citable source truth. The context manifest makes this boundary explicit: what history was kept, what was dropped, which evidence refs were available, and which refs are actually citable.

The memory layer is graph-aware: claims, sources, criteria, report drafts, unresolved risks and reviewer feedback can be connected rather than stored as a flat transcript. Feedback and observations attach to stable graph-unit keys, so useful memory can carry forward across rebuilds when identity is preserved, while ambiguous mappings are quarantined rather than silently trusted.

## Product shape

The wider system is built around a shared kernel and client-specific configuration. Core workflow, security and evidence binding are fixed. Forms, questions, report structure and policies change per use case.

For ASPIRE, LumiSense is presented as a product for inbound project and document review, not as a platform for every possible use case.

## What the prototype already supports

- Structured case handling
- Content extraction across documents, Office files, images, audio and video
- Evidence-linked review outputs
- Report and follow-up workflow in the same workspace
- Context manifest and structured case memory
- Kernel and client-configuration separation
