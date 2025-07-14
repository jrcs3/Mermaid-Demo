# Styling

## Style

``` text
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
I don't show it here, but you can stack nodes styles. So you can have something like this `style A, B, C fill:##69BE28,color:#002244`.
## classDef
This is the first way I discovered to style objects in Mermaid. As I researched styling, I am finding that the other approaches are more
flexable and easier to use. 
``` text
graph TB
  %% Styling
  classDef AyeCD fill:red,color:green,font-weight:bold,stroke:green
  classDef BeeCD fill:yellow,color:black
  %% subgraph does not support this
  %%classDef SgCD fill:aliceblue,color:darkgreen,stroke:darkblue

  %% Nodes
  %% subgraph does not support this
  %%subgraph sg:::SgCD
  A:::AyeCD
  %%end
  B:::BeeCD
```

``` mermaid
graph TB
  %% Styling
  classDef AyeCD fill:red,color:green,font-weight:bold,stroke:green
  classDef BeeCD fill:yellow,color:black
  %% subgraph does not support this
  %%classDef SgCD fill:aliceblue,color:darkgreen,stroke:darkblue

  %% Nodes
  %% subgraph does not support this
  %%subgraph sg:::SgCD
  A:::AyeCD
  %%end
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