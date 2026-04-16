# System Context

High-level view: submitter, reviewer and operator around the review workspace.

## Diagram

```mermaid
flowchart LR
    A["External submitter"] --> B["Case submission and follow-up"]
    C["Reviewer or analyst"] --> D["LumiSense review workspace"]
    E["Operator or admin"] --> F["Configuration and oversight"]

    B --> D
    F --> D

    D --> G["Stored source material"]
    D --> H["Extracted and structured case content"]
    D --> I["Search and review surface"]
    D --> J["Evidence-linked summary or report"]
    J --> C
```

LumiSense sits between incoming materials and reviewer decisions, keeping the workflow structured and the outputs tied to case evidence.
