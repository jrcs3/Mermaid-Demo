# Introduction to Mermaidjs

[Mermaid | Diagramming and charting tool](https://mermaid.js.org/) is the projects site, and the [Github site](https://github.com/mermaid-js/mermaid) if you want to see the source code.

[Mermaid Live Editor](https://mermaid.live/) is a good tool to experiment with Mermaid.

[Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced) is a VS Code extension that supports Mermaid.

- [Compared to Visio](vs-visio.md)
- [Types of Diagrams](types-of-diagrams.md)
- [Shapes](shapes.md)
- [Connectors](connectors.md)
- [Styling](style.md)
- [Trial &amp; Error](Trial-and-error.md)

---

## Agenda

```mermaid
---
config:
  look: handDrawn
  theme: neutral 2
---
flowchart TD
    %% Nodes with shapes
    A(("Why Mermaid?<br/>(Pain Points)")):::startClass
    B{{"Compared<br/>to Visio"}}:::compareClass
    C(["Types of<br/>Diagrams"]):::typeClass
    D[/"Shapes"\]:::shapesClass
    E(["Connectors"]):::connectClass
    F(("Styling")):::stylingClass
    G{{"Trial & Error"}}:::trialClass
    H["Resources &<br/>Live Demo"]:::finalClass
 
    %% Flow
    A --> B
    B -.-> |"Decision"| C
    C --> D
    D --> |"Visual"| E
    E --> F
    F -.-> |"Experiment"| G
    G --> H

    %% Styling
    classDef startClass fill:limegreen,stroke:green,stroke-width:2px,color:white
    classDef compareClass fill:yellow,stroke:gold,stroke-width:2px,color:black
    classDef typeClass fill:skyblue,stroke:blue,stroke-width:2px,color:navy
    classDef shapesClass fill:pink,stroke:red,stroke-width:2px,color:black
    classDef connectClass fill:silver,stroke:black,stroke-width:2px,color:black
    classDef stylingClass fill:lightgreen,stroke:green,stroke-width:2px,color:darkgreen
    classDef trialClass fill:bisque,stroke:saddlebrown,stroke-width:2px,color:brown
    classDef finalClass fill:mediumpurple,stroke:indigo,stroke-width:2px,color:white

    click E href "./connectors.md"
```
