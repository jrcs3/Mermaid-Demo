# Styling

## Style

``` text
graph TB
  %% styles
  style A fill:red,color:green,font-weight:bold,stroke:green
  style B fill:yellow,color:black
  style sg fill: aliceblue,color:darkgreen,stroke:darkblue

  %% Nodes
  subgraph sg[Sub Graph]
  A
  end
  B
```

``` mermaid
graph TB
 %% styles
  style A fill:red,color:green,font-weight:bold,stroke:green
  style B fill:yellow,color:black
  style sg fill:aliceblue,color:darkgreen,stroke:darkblue

  %% Nodes
  subgraph sg[Sub Graph]
  A
  end
  B
```

## classDef

``` text
graph TB
  %% Styling
  classDef AyeCD fill:red,color:green,font-weight:bold,stroke:green
  classDef BeeCD fill:yellow,color:black
  classDef SgCD fill:aliceblue,color:darkgreen,stroke:darkblue

  %% Nodes
  subgraph sg[Sub Graph]:::SgCD
  A:::AyeCD
  end
  B:::BeeCD
```

``` mermaid
graph TB
  %% Styling
  classDef AyeCD fill:red,color:green,font-weight:bold,stroke:green
  classDef BeeCD fill:yellow,color:black
  classDef SgCD fill:aliceblue,color:darkgreen,stroke:darkblue

  %% Nodes
  subgraph sg[Sub Graph]:::SgCD
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
  classDef SgCD fill:aliceblue,color:darkgreen,stroke:darkblue

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
  classDef SgCD fill:aliceblue,color:darkgreen,stroke:darkblue

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