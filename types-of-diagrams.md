# Types of Diagrams

[Mermaid Live Editor](https://mermaid.live/) is a good tool for exploring the most popular type of diagrams.

## flowchart 

Most of the diagrams I've written are flowchart diagrams. I can stretch visualize most of what I need.

See [Flowchart Syntax | Mermaid](https://mermaid.js.org/syntax/flowchart.html)

``` text
flowchart TB
    A((Start)) --> |It is 6 AM| B[/Alarm Goes Off/]
    B --> C{Ready to<br/>get up?}
    C --> |Yes| E[Get Up]
    C --> |No| D(Snooze)
    D --> |5 minutes<br/>pass| B
    E --> F(((End)))
```
``` mermaid
flowchart TB
    A((Start)) --> |It is 6 AM| B[/Alarm Goes Off/]
    B --> C{Ready to<br/>get up?}
    C --> |Yes| E[Get Up]
    C --> |No| D(Snooze)
    D --> |5 minutes<br/>pass| B
    E --> F(((End)))
```

## stateDiagram-v2

See [State diagrams | Mermaid](https://mermaid.js.org/syntax/stateDiagram.html)

``` text
stateDiagram-v2
    %% Node Defs
    B : Alarm Goes Off
    C : Ready to<br/>get up?
    E : Get Up
    D : Snooze
    %% Relationships
    [*] --> B : It is 6 AM
    B --> C
    C --> E : Yes
    C --> D : No
    D --> B : 5 minutes<br/>pass
    E --> [*]
```
``` mermaid
stateDiagram-v2
    %% Node Defs
    B : Alarm Goes Off
    C : Ready to<br/>get up?
    E : Get Up
    D : Snooze
    %% Relationships
    [*] --> B : It is 6 AM
    B --> C
    C --> E : Yes
    C --> D : No
    D --> B : 5 minutes<br/>pass
    E --> [*]
```

## sequenceDiagram
I think I've used this twice in the wild. 

See [Sequence diagrams | Mermaid](https://mermaid.js.org/syntax/sequenceDiagram.html)

``` text
sequenceDiagram
  participant Alarm as Alarm Clock
  actor me as Me
  participant Up as Reality
  loop every starting at 6 AM<br/>5 minutes<br/> until ready to get up
    Alarm-->>+me: Brrrring!
    me-->>-Alarm: push Snooze
  end
  break Ready?
    me-->>Up: Get up
  end
```
``` mermaid
sequenceDiagram
  participant Alarm as Alarm Clock
  actor me as Me
  participant Up as Reality
  loop every starting at 6 AM<br/>5 minutes<br/> until ready to get up
    Alarm-->>+me: Brrrring!
    me-->>-Alarm: push Snooze
  end
  break Ready?
    me-->>Up: Get up
  end
```
## erDiagram

See [Entity Relationship Diagrams | Mermaid](https://mermaid.js.org/syntax/entityRelationshipDiagram.html)

```text
erDiagram
    direction LR
    BOOK ||--o{ GENRE : "joined to"
    BOOK {
        int id pk
        int genreId fk
        nvarchar(255) title
        nvarchar(255) author
        int yearPublished
    }
    GENRE {
        int id pk
        nvarchar(50) name
    }
```
```mermaid
erDiagram
    direction LR
    BOOK ||--o{ GENRE : "joined to"
    BOOK {
        int id pk
        int genreId fk
        nvarchar(255) title
        nvarchar(255) author
        int yearPublished
    }
    GENRE {
        int id pk
        nvarchar(50) name
    }
```


## classDiagram

See [Class diagrams | Mermaid](https://mermaid.js.org/syntax/classDiagram.html)

```text
classDiagram
    direction LR
    BOOK <-- GENRE : joined to
    class BOOK{
        int id pk
        int genreId fk
        string title
        string author
        int yearPublished
    }
    class GENRE{
        int id pk
        string name
    }
```
```mermaid
classDiagram
    direction LR
    BOOK <-- GENRE : joined to
    class BOOK{
        int id pk
        int genreId fk
        string title
        string author
        int yearPublished
    }
    class GENRE{
        int id pk
        string name
    }
```

---
Next [Shapes](shapes.md)

Back to [main read md](readme.md).