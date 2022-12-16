# State Graphs

```{mermaid}

  stateDiagram-v2
    direction LR
    [*] --> Even
    Even --> [*]

    Even --> Even: 1

    Even --> Odd : 0
    Odd --> Even : 0

    Odd --> Odd : 1
    Odd --> [*]
```