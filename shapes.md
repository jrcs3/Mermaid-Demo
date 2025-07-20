# Shapes

See [Node shapes](https://mermaid.js.org/syntax/flowchart.html#node-shapes)

## Simple Shapes
``` mermaid
---
title: Shapes
---
flowchart LR
node
square[Square Corners]
rounded(Rounded Corners)
stadium([Stadium Shape])
database[(Database<br/>Shape)]
round((round))
rhombus{Rhombus<br/>Shape}
```

## @Shapes

See [Expanded Node Shapes in Mermaid Flowcharts (v11.3.0+)](https://mermaid.js.org/syntax/flowchart.html#expanded-node-shapes-in-mermaid-flowcharts-v11-3-0)

``` mermaid
flowchart RL
    A@{ shape: notch-rect, label: "notch-rect"}
    B@{ shape: das, label: "Direct access storage" }
    C@{ shape: bolt, label: "Communication link" }
```

## FontAwesome

See [Register FontAwesome CSS](https://mermaid.js.org/syntax/flowchart.html#register-fontawesome-css)

<link
  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css"
  rel="stylesheet"
/>

``` mermaid
flowchart TB
    B[fa:fa-ban forbidden]
    C[Drive your fa:fa-car!]
    D(Take a picture withour fa:fa-camera-retro)
```