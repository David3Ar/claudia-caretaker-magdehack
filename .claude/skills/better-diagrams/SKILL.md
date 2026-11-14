---
name: better-diagrams
description: Use this whenever you need to create or revise a diagram (Mermaid, architecture, flow, sequence, ASCII) in docs, issues, or replies. Structure, label and color rules.
---

# Better Diagrams

## Structure

1. State what the diagram shows in one line: a concise title ("Request path from edge to SonarQube"). Put it as `accTitle`/`accDescr` or in the sentence above the block.
2. Pick one reading direction. `TB` whenever boundaries are nested (it stays readable at column width), `LR` only for flat pipelines. No arrows against it except the one that tells the story.
3. Draw boundaries first (nested subgraphs: cloud / host / VM), then nodes, then edges. Grouping carries more meaning than arrows.
4. Keep the main path straight and emphasized (`==>`). Secondary concerns (DNS, certificates, secrets, monitoring, backups) get their own group or dotted edges (`-.->`) and never cross the main path. Dotted edges carry no label.

## Labels

- Node label: name on the first line, role on the second. Never a sentence.
- Never emoji. If a marker helps, use node shapes or icon syntax (`fa:fa-server`).
- Edge label only when the protocol or port is the point. Otherwise none.

## Style

Calm, not loud: lightly tinted fills, one colored stroke per role, neutral boundaries. Every node gets exactly one of the four role classes, every subgraph gets `boundary`. Define no others, no other `%%{init}%%` block.

```
classDef ingress  fill:#eff6ff,stroke:#2563eb,stroke-width:1.5px,color:#0f172a
classDef service  fill:#f0fdf4,stroke:#15803d,stroke-width:1.5px,color:#0f172a
classDef storage  fill:#f1f5f9,stroke:#64748b,stroke-width:1.5px,color:#0f172a
classDef external fill:#fef3c7,stroke:#b45309,stroke-width:1.5px,color:#0f172a
classDef boundary fill:none,stroke:#cbd5e1,stroke-width:1px,color:#475569
```

Concept sketches use rounded nodes (`id("label")`) and start with exactly this line:

```
%%{init: {"look":"handDrawn","theme":"neutral","themeVariables":{"fontFamily":"Excalifont, Virgil, Chalkboard SE, Comic Neue, cursive","fontSize":"14px"}}}%%
```

Escalate to a real Excalidraw file only when the sketch needs freeform shapes.

## Gate before delivery

Render if a renderer is available (`mmdc`, browser, preview) and look at it. Then say in one line in your reply: title, direction, and which classes you used. Check that every edge attaches to a node, not floating in space (the most common break). If a node or subgraph has no class or a secondary edge crosses the main path, revise first.

Syntax, GitHub light/dark and accessibility rules: [Mermaid Style Guide](../../../.skills/scientific-markdown-mermaid-writing/references/mermaid_style_guide.md). Its emoji rules do not apply.
