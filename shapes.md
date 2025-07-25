# Shapes

See [Node shapes](https://mermaid.js.org/syntax/flowchart.html#node-shapes)

## flowchart
### Simple Shapes
``` text
---
title: Shapes
---
flowchart LR
    square[Square Corners]
    rounded(Rounded Corners)
    stadium([Stadium Shape])
    database[(Database<br/>Shape)]
    round((round))
    rhombus{Rhombus<br/>Shape}
```

``` mermaid
---
title: Shapes
---
flowchart LR
    square[Square Corners]
    rounded(Rounded Corners)
    stadium([Stadium Shape])
    database[(Database<br/>Shape)]
    round((round))
    rhombus{Rhombus<br/>Shape}
```

### @Shapes

See [Expanded Node Shapes in Mermaid Flowcharts (v11.3.0+)](https://mermaid.js.org/syntax/flowchart.html#expanded-node-shapes-in-mermaid-flowcharts-v11-3-0)

``` text
flowchart RL
    A@{ shape: notch-rect, label: "notch-rect"}
    B@{ shape: das, label: "Direct access storage" }
    C@{ shape: bolt, label: "Communication link" }
```

``` mermaid
flowchart RL
    A@{ shape: notch-rect, label: "notch-rect"}
    B@{ shape: das, label: "Direct access storage" }
    C@{ shape: bolt, label: "Communication link" }
```

### FontAwesome

See [Register FontAwesome CSS](https://mermaid.js.org/syntax/flowchart.html#register-fontawesome-css)

For FawtAwsome to work, you may need to link to it like this:
```html
<link
  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css"
  rel="stylesheet"
/>
```
<link
  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css"
  rel="stylesheet"
/>

``` text
flowchart TB
    B[fa:fa-ban forbidden]
    C[Drive your fa:fa-car!]
    D(Take a picture without fa:fa-camera-retro)
```

``` mermaid
flowchart TB
    B[fa:fa-ban forbidden]
    C[Drive your fa:fa-car!]
    D(Take a picture without fa:fa-camera-retro)
```

Back to [main read md](readme.md).