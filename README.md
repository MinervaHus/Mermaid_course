# Mermaid_course
Graphs from Mermaid lecture

Just for testing and learning purposes

```mermaid
flowchart TD
    A[Graph] -->|R or Python or even Excel| C{Graphical image}
    A[Graph] -->|Knowledge| B(Guide understanding)
    C -->|2D| D[dot/bar/violin/line/plot etc]
    C -->|3D| E[UMAP etc]
    E[UMAP etc] --> F(Share data)
    D[dot/bar/violin/line/plot etc] --> F(Share data)
    B(Guide understanding) --> F(Share data)
```


```mermaid
flowchart TD
  graphs[Graphs]
  images[Images that convey information]
  subgraph types[Types]
    subgraph self_contained[Self-contained]
    mindmap[Mindmap]
    a_flowchart[Flowchart]
    end
    subgraph need_data[Need data]
      scatter_plot[Scatter plot]
    end
  end
  subgraph tools[Tools]
    mermaid_live[mermaid.live]
    python[Python]
    r[R]
  end

  graphs --> |are| images
  images --> |depend on| types
  graphs --> |have| types
  mindmap --> |usually| self_contained
  a_flowchart --> |usually| self_contained
  scatter_plot --> need_data

  graphs --> |drawn by| tools

  mermaid_live <--> |works on|self_contained
  python --> |works on| need_data
  r --> |works on| need_data
```

```mermaid
flowchart TD

  classDef bjorn_node fill:#ddf,color:#000,stroke:#00f
  classDef lars_node fill:#dfd,color:#000,stroke:#0f0
  classDef richel_node fill:#fdd,color:#000,stroke:#f00

  subgraph day_1[Monday]
    git_basic[git basic workflow]:::bjorn_node
    class_design[Class design]:::lars_node
  end
  subgraph day_2[Tuesday]
    class_diagram[Create project's class diagram]:::lars_node
    pair_programming[Pair programming]:::richel_node
    tdd[TDD]:::richel_node
  end

  git_basic --> pair_programming
  pair_programming --> tdd
  class_design --> class_diagram
  class_diagram --> tdd
  git_basic --> tdd
```
flowchart TD
  classDef graph_node fill:#fdd,color:#000,stroke:#f00
  classDef lars_node fill:#dfd,color:#000,stroke:#0f0
  classDef richel_node fill:#ddf,color:#000,stroke:#00f
  A[Graph]:::graph_node
    A[Graph] -->|R or Python or even Excel| C{Graphical image}
    A[Graph] -->|Knowledge| B(Guide understanding)
    C -->|2D| D[dot/bar/violin/line/plot etc]
    C -->|3D| E[UMAP etc]
    E[UMAP etc] --> F(Share data)
    D[dot/bar/violin/line/plot etc] --> F(Share data)
    B(Guide understanding) --> F(Share data)
    C{Graphical image}:::richel_node
    F(Share data):::lars_node
