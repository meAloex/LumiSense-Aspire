# Review Runtime

Runtime path from case input to evidence-linked answer or versioned report, with continuity across follow-up work.

## Diagram

```mermaid
flowchart LR
    subgraph A["Inbound case flow"]
        A1["Case and submission"]
        A2["Uploaded files and follow-up input"]
        A3["Stored source record"]
    end

    subgraph B["Preparation layer"]
        B1["Extraction and structuring"]
        B2["Usable content and anchors"]
        B3["Searchable case layer"]
    end

    subgraph C["Review runtime"]
        C1["Case-aware retrieval"]
        C2["Reviewer chat flow"]
        C3["Report generation flow"]
    end

    subgraph D["Review outputs"]
        D1["Evidence-linked answer"]
        D2["Versioned report"]
        D3["Continued follow-up work"]
    end

    A1 --> A2
    A2 --> A3
    A3 --> B1
    B1 --> B2
    B2 --> B3
    B3 --> C1
    C1 --> C2
    C1 --> C3
    C2 --> D1
    C3 --> D2
    D1 --> D3
    D2 --> D3
```

LumiSense uses the same case state for retrieval, reviewer chat and report output, which keeps follow-up work consistent.
