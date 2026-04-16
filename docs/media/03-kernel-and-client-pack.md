# Kernel and Client Pack

Shared kernel, client pack and configured product. Kernel rules are fixed; the pack adapts the product for a specific review use case.

## Diagram

```mermaid
flowchart LR
    subgraph K["Shared kernel"]
        direction TB
        K1[Case and submission workflow]
        K2[Security and access rules]
        K3[Evidence and audit model]
        K4[Review and reporting flow]
        K5[Stored continuity across the case]
    end
    subgraph P["Client pack"]
        direction TB
        P1[Forms and validation]
        P2[Question sets and prompts]
        P3[Report structure]
        P4[Policy settings]
        P5[Workflow emphasis for a use case]
    end
    subgraph C["Configured product"]
        direction TB
        C1[Inbound review workspace]
        C2[Case-specific workflow]
        C3[Evidence-linked outputs]
    end
    K --> C
    P --> C
```

The shared LumiSense core stays the same, while the client pack shapes the workflow for a specific use case.
