# Benchmarks

LumiSense is developed with a benchmark lane, not only demos. Changes are checked against pinned assets and stored expectations on repeatable runs.

## Pinned sources

The public-core benchmark pack uses material from stable institutional sources:

- GovInfo (US federal documents)
- Library of Congress (images and digitised materials)
- UN Digital Library (multilingual documents)
- NASA (text, audio, video)
- Wikimedia Commons (images, video, Russian-language captions)
- Microsoft sample collections (DOCX, PPTX, XLSX)

Each pinned asset has a recorded checksum, a source URL, a license note and a tolerance file. Extraction expectations are stored alongside the asset rather than generated at run time.

## Oracle truth

Expected outputs for every pinned asset were authored by hand against the product's own extraction contracts rather than taken from a public dataset. Off-the-shelf extraction benchmarks do not map cleanly onto this pipeline — anchors, role assignment, contextualisation modes and evidence posture are product-specific — so each case is built, reviewed and approved one at a time.

This is why the public-core pack is smaller than a lab-grade benchmark at this stage. Authoring oracle data is the most time-consuming part of the work and it scales case by case. The pack will keep growing.

## Coverage matrix

| Modality | Cases pinned | Languages | Status |
|---|---|---|---|
| PDF (digital-born) | 3 | EN, RU | covered end-to-end |
| Office (DOCX, PPTX) | 2 | EN | covered end-to-end |
| Office (XLSX) | 1 | EN | passing golden run |
| Images | 3 | EN, RU | covered end-to-end |
| Audio (speech) | 1 | EN | passing golden run |
| Audio (diarization) | 1 | — | seeded |
| Video | 2 | EN, RU captions | covered end-to-end |
| Plain text | 1 | EN | pinned |

Forty-plus additional cases are registered as planned across extended-fetch and internal-mixed packs. They are not part of the public-core story.

## Retrieval on the development slice

The current retrieval proof runs on a six-case multimodal slice.

| Metric | Value |
|---|---|
| Hit rate @10 | 1.00 |
| Hit rate @5 | 1.00 |
| Hit rate @1 | 0.67 |
| English split @5 | 1.00 |
| Russian split @5 | 1.00 |

Ranks of the correct evidence across the six queries: 1, 7, 1, 2, 2, 3. This is a small slice meant to show retrieval direction and runtime reality, not a full lab benchmark.

## Open work

- Chunking tolerance comparisons still fail on some runs during tuning
- The projection-id bridge for graph-aware retrieval is pending
- The live-runtime retrieval proof is on the development slice, not in production-ready state
- Expansion into tables and forms is in the planned packs rather than in public-core

Parts of the pipeline pass; others are still being tuned. That is kept visible rather than hidden.
