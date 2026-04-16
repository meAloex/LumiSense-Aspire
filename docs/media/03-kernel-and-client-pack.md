# Kernel and Client Pack

Shared kernel, client pack and configured product. Kernel rules are fixed; the pack adapts the product for a specific review use case.

## Diagram

```mermaid
flowchart TB
    subgraph A["Shared LumiSense kernel"]
        A1["Case and submission workflow"]
        A2["Security and access rules"]
        A3["Evidence and audit model"]
        A4["Review and reporting flow"]
        A5["Stored continuity across the case"]
    end

    subgraph B["Client pack"]
        B1["Forms and validation"]
        B2["Question sets and prompts"]
        B3["Report structure"]
        B4["Policy settings"]
        B5["Workflow emphasis for a specific use case"]
    end

    subgraph C["Configured product"]
        C1["Inbound review workspace"]
        C2["Case-specific workflow"]
        C3["Evidence-linked outputs"]
    end

    A1 --> C1
    A2 --> C1
    A3 --> C3
    A4 --> C2
    A5 --> C2
    B1 --> C1
    B2 --> C2
    B3 --> C3
    B4 --> C2
    B5 --> C1
```

The shared LumiSense core stays the same, while the client pack shapes the workflow for a specific use case.
