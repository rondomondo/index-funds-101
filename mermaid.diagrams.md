# A note on the diagrams/graphs

Below you'll find several diagrams illustrating potential investment growth over time based on different monthly contributions.

These markdown versions below represent the actual source of what you see and so complement the actual image renders in [README.md](README.md)

These visuals were created using [Mermaid Markdown](https://mermaid.js.org), a text-based syntax for generating diagrams.

For more details on creating your own diagrams with Mermaid, checkout the official documentation: [mermaid.js.org](https://mermaid.js.org).

## Investment Growth In Pictures

### Growth Over Time

```mermaid

graph LR
    subgraph "Growth Over Time"
    TimeScale["Years"] --- Y0[0] --- Y10[10] --- Y20[20] --- Y30[30]
    
    %% €100/month
    Y0 -.-> A10[€17K]
    A10 -.-> A20[€49K]
    A20 -.-> A30[€120K]
    
    %% €250/month
    Y0 -.-> B10[€43K]
    B10 -.-> B20[€123K]
    B20 -.-> B30[€299K]
    
    %% €500/month
    Y0 -.-> C10[€87K]
    C10 -.-> C20[€246K]
    C20 -.-> C30[€599K]
    
    %% €1000/month
    Y0 -.-> D10[€173K]
    D10 -.-> D20[€492K]
    D20 -.-> D30[€1.2M]
    
    %% Labels
    style A10 fill:#e6f7ff,stroke:#1890ff
    style A20 fill:#e6f7ff,stroke:#1890ff
    style A30 fill:#e6f7ff,stroke:#1890ff
    
    style B10 fill:#fff7e6,stroke:#fa8c16
    style B20 fill:#fff7e6,stroke:#fa8c16
    style B30 fill:#fff7e6,stroke:#fa8c16
    
    style C10 fill:#f6ffed,stroke:#52c41a
    style C20 fill:#f6ffed,stroke:#52c41a
    style C30 fill:#f6ffed,stroke:#52c41a
    
    style D10 fill:#f9f0ff,stroke:#722ed1
    style D20 fill:#f9f0ff,stroke:#722ed1
    style D30 fill:#f9f0ff,stroke:#722ed1
    
    classDef blue fill:#e6f7ff,stroke:#1890ff;
    classDef orange fill:#fff7e6,stroke:#fa8c16;
    classDef green fill:#f6ffed,stroke:#52c41a;
    classDef purple fill:#f9f0ff,stroke:#722ed1;
    
    L100[€100/month] ~~~ A10
    class L100 blue
    
    L250[€250/month] ~~~ B10
    class L250 orange
    
    L500[€500/month] ~~~ C10
    class L500 green
    
    L1000[€1000/month] ~~~ D10
    class L1000 purple
    end
```



### Investment Growth Comparison After 30 Years

```mermaid

%%{init: {'theme': 'default', 'themeVariables': { 'primaryColor': '#42b983', 'primaryTextColor': '#fff', 'primaryBorderColor': '#42b983', 'lineColor': '#ff9900', 'tertiaryColor': '#fff' }}}%%
graph TD
    subgraph "Monthly Investment: 100€" 
    style A1 fill:#e6f7ff,stroke:#1890ff
    style A2 fill:#e6f7ff,stroke:#1890ff
    style A3 fill:#e6f7ff,stroke:#1890ff
    A1[10 Years: 17,300€] --> A2[20 Years: 49,200€]
    A2 --> A3[30 Years: 119,700€]
    end
    
    subgraph "Monthly Investment: 250€"
    style B1 fill:#fff7e6,stroke:#fa8c16
    style B2 fill:#fff7e6,stroke:#fa8c16
    style B3 fill:#fff7e6,stroke:#fa8c16
    B1[10 Years: 43,250€] --> B2[20 Years: 123,000€]
    B2 --> B3[30 Years: 299,250€]
    end
    
    subgraph "Monthly Investment: 500€"
    style C1 fill:#f6ffed,stroke:#52c41a
    style C2 fill:#f6ffed,stroke:#52c41a
    style C3 fill:#f6ffed,stroke:#52c41a
    C1[10 Years: 86,500€] --> C2[20 Years: 246,000€]
    C2 --> C3[30 Years: 598,500€]
    end
    
    subgraph "Monthly Investment: 1,000€"
    style D1 fill:#f9f0ff,stroke:#722ed1
    style D2 fill:#f9f0ff,stroke:#722ed1
    style D3 fill:#f9f0ff,stroke:#722ed1
    D1[10 Years: 173,000€] --> D2[20 Years: 492,000€]
    D2 --> D3[30 Years: 1,197,000€]
    end

```

### Growth Over Time - different initial principle

```mermaid

gantt
    title Investment Growth Comparison (30 Years)
    dateFormat X
    axisFormat %s
    
    section €100/month
    30-Year Growth (€120K): 0, 120
    Growth Beyond Contributions (€84K): 120, 204
    
    section €250/month
    30-Year Growth (€300K): 0, 300
    Growth Beyond Contributions (€209K): 300, 509
    
    section €500/month
    30-Year Growth (€600K): 0, 600
    Growth Beyond Contributions (€419K): 600, 1019
    
    section €1,000/month
    30-Year Growth (€1.2M): 0, 1200
    Growth Beyond Contributions (€837K): 1200, 2037
```


### Investment Comparison After 30 Years

```mermaid

graph TD
    subgraph "Comparison After 30 Years"
    
    A[Investment Amounts]
    A --> A1[€100/month<br>Total: €36,000]
    A --> A2[€250/month<br>Total: €90,000]
    A --> A3[€500/month<br>Total: €180,000]
    A --> A4[€1,000/month<br>Total: €360,000]
    
    A1 --> B1[Final Value:<br>€119,700]
    A2 --> B2[Final Value:<br>€299,250]
    A3 --> B3[Final Value:<br>€598,500]
    A4 --> B4[Final Value:<br>€1,197,000]
    
    B1 --> C1[Growth:<br>€83,700<br>+233%]
    B2 --> C2[Growth:<br>€209,250<br>+233%]
    B3 --> C3[Growth:<br>€418,500<br>+233%]
    B4 --> C4[Growth:<br>€837,000<br>+233%]
    
    style A1 fill:#e6f7ff,stroke:#1890ff
    style A2 fill:#fff7e6,stroke:#fa8c16
    style A3 fill:#f6ffed,stroke:#52c41a
    style A4 fill:#f9f0ff,stroke:#722ed1
    
    style B1 fill:#e6f7ff,stroke:#1890ff
    style B2 fill:#fff7e6,stroke:#fa8c16
    style B3 fill:#f6ffed,stroke:#52c41a
    style B4 fill:#f9f0ff,stroke:#722ed1
    
    style C1 fill:#e6f7ff,stroke:#1890ff
    style C2 fill:#fff7e6,stroke:#fa8c16
    style C3 fill:#f6ffed,stroke:#52c41a
    style C4 fill:#f9f0ff,stroke:#722ed1
    
    end
```

