# Evidence Pipeline

Internal flow at a public-safe level: raw material is retained, canonical content becomes the working review surface, and outputs are verified against sources before publish.

## Diagram

```mermaid
flowchart LR
    subgraph A["Case inputs"]
        A1["Form answers"]
        A2["Documents and slides"]
        A3["Images, audio, video"]
        A4["Follow-up messages"]
    end

    subgraph B["Source and extraction layer"]
        B1["Stored original materials"]
        B2["Structured extraction across lanes"]
        B3["Quality gate"]
        B4["Anchors and usable content"]
    end

    subgraph C["Review layer"]
        C1["Searchable case workspace"]
        C2["Case-aware retrieval"]
        C3["Reviewer chat and report flow"]
    end

    subgraph D["Output layer"]
        D1["Citation guard"]
        D2["Evidence-linked summary"]
        D3["Versioned report output"]
        D4["Follow-up with continuity"]
    end

    A1 --> B1
    A2 --> B1
    A3 --> B1
    A4 --> B1
    B1 --> B2
    B2 --> B3
    B3 --> B4
    B4 --> C1
    C1 --> C2
    C2 --> C3
    C3 --> D1
    D1 --> D2
    D1 --> D3
    D2 --> D4
    D3 --> D4
```

## Quality gate

Extraction runs across multiple lanes. The quality gate reviews coverage, anchor presence and warnings, and routes weak output through augmentation or rescue lanes without discarding the original submission.

## Citation guard

Before an output is finalised, each cited passage is checked: the quote must exist in the source, the anchor must resolve, and the reference must belong to the current case. Claims without verified evidence do not enter a formal report.

LumiSense keeps review outputs tied to stored source material and verifies citations before publishing, rather than trusting prompt context alone.
