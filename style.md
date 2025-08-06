# Styling

## Applying Styling

``` text
graph TB
  %% styles
  style A fill:red,color:green,font-weight:bold,stroke:green
  style B fill:yellow,color:black
  style sg fill:aliceblue,color:darkgreen,stroke:darkblue,font-family:monospace

  %% Nodes
  subgraph sg[Sub Graph]
  A
  end
  B
```

``` mermaid
graph TB
 %% styles
  style A fill:red,color:green,font-weight:bold,stroke:green,font-family:monospace
  style B fill:yellow,color:black
  style sg fill:aliceblue,color:darkgreen,stroke:darkblue

  %% Nodes
  subgraph sg[Sub Graph]
  A
  end
  B
```
I don't show it here, but you can stack nodes styles. So you can have something like this `style A, B, C fill:##69BE28,color:#002244`.
## classDef
This is the first way I discovered to style objects in Mermaid. As I researched styling, I am finding that the other approaches are more flexable and easier to use. 
``` text
graph TB
  %% Styling
  classDef AyeCD fill:red,color:green,font-weight:bold,stroke:green
  classDef BeeCD fill:yellow,color:black
  %% subgraph does not support classDef
  %% To get the subgraph to work I need to resort to style
  style sg fill:aliceblue,color:darkgreen,stroke:darkblue,font-family:monospace
  
  %% Nodes
  %% subgraph does not support this
  subgraph sg[Sub Graph]
  A:::AyeCD
  end
  B:::BeeCD
```

``` mermaid
graph TB
  %% Styling
  classDef AyeCD fill:red,color:green,font-weight:bold,stroke:green
  classDef BeeCD fill:yellow,color:black
  %% subgraph does not support classDef
  %% To get the subgraph to work I need to resort to style
  style sg fill:aliceblue,color:darkgreen,stroke:darkblue,font-family:monospace
  
  %% Nodes
  %% subgraph does not support this
  subgraph sg[Sub Graph]
  A:::AyeCD
  end
  B:::BeeCD
```

## classDef + class

``` text
graph TB
  %% Styling
  classDef AyeCD fill:red,color:green,font-weight:bold,stroke:green
  classDef BeeCD fill:yellow,color:black
  classDef SgCD fill:aliceblue,color:darkgreen,stroke:darkblue,font-family:monospace

  %% Nodes
  subgraph sg[Sub Graph]
  A
  end
  B

  %% Classes (must be below the Nodes)
  class A AyeCD
  class B BeeCD
  class sg SgCD
```

``` mermaid
graph TB
  %% Styling
  classDef AyeCD fill:red,color:green,font-weight:bold,stroke:green
  classDef BeeCD fill:yellow,color:black
  classDef SgCD fill:aliceblue,color:darkgreen,stroke:darkblue,font-family:monospace;

  %% Nodes
  subgraph sg[Sub Graph]
  A
  end
  B

  %% Classes (must be below the Nodes)
  class A AyeCD
  class B BeeCD
  class sg SgCD
```

## Themes
See: [Theme Configuration](https://mermaid.js.org/config/theming.html)
The examples below use this code with with `<<theme name>>` rplaced with the named theme name.
``` text
---
title: Theme Example
displayMode: compact
config:
  theme: <<theme name>>
---
flowchart LR
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C((done))
```
Mermaid has 5 build in themes as of the time. 

### default

``` mermaid
---
title: Theme Example for default
displayMode: compact
config:
  theme: default 
---
flowchart LR
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C((done))
```

### neutral

``` mermaid
---
title: Theme Example for neutral
displayMode: compact
config:
  theme: neutral 
---
flowchart LR
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C((done))
```
### dark

``` mermaid
---
title: Theme Example for dark
displayMode: compact
config:
  theme: dark 
---
flowchart LR
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C((done))
```

### forest

``` mermaid
---
title: Theme Example for forest
displayMode: compact
config:
  theme: forest 
---
flowchart LR
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C((done))
```

### base

``` mermaid
---
title: Theme Example for base
displayMode: compact
config:
  theme: base 
---
flowchart LR
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C((done))
```

### base + Override themeVariables (Christmas)

``` text
---
title: Theme Example
displayMode: compact
config:
  theme: 'base'
  themeVariables:
    primaryColor: '#BB2528'
    primaryTextColor: '#fff'
    primaryBorderColor: '#7C0000'
    lineColor: '#006100'
    secondaryColor: '#006100'
    tertiaryColor: '#fff'
---
flowchart LR
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C((done))
```

``` mermaid
---
title: Theme Example
displayMode: compact
config:
  theme: 'base'
  themeVariables:
    primaryColor: '#BB2528'
    primaryTextColor: '#fff'
    primaryBorderColor: '#7C0000'
    lineColor: '#006100'
    secondaryColor: '#006100'
    tertiaryColor: '#fff'
---
flowchart LR
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C((done))
```

## CSS Properies I use

- **color**:
- **fill**: 
- **stroke**: 
- **font**
  - **font-weight**:
  - **font-family**:

## CSS Properies I have tried and failed to use

- **font**
  - **font-sixe**:

---
Next [List to Mermaid Example](list-to-mermaid-example.md)

Back to [main read md](readme.md).