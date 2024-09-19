
# DDD 
```mermaid
    flowchart LR
        subgraph PublicInternet
            user 
        end
        subgraph LoadBalancingZone
            LoadBalancer
        end
        subgraph WebserverZone
            WebserverA
            WebserverB
        end    

        user --tcp/80--> LoadBalancer
        LoadBalancer --tcp/1337--> WebserverA
        LoadBalancer --tcp/1337--> WebserverB

        WebserverA --> DatabaseserverA
        WebserverA -.-> DatabaseserverB
        WebserverB --> DatabaseserverA
        WebserverB -.-> DatabaseserverB

        style user fill:navy
```

# Test
```mermaid
    flowchart TB
        subgraph My App
            Home(((Home)))==>Review([Review])
            Home --> Edit([Edit])
            Home --> Help[[Help]]
            Edit-->Submit[(Database)]
            Submit-->Review

            style Home fill:navy
            style Review fill:darkgreen
            style Help fill: purple
            style Submit fill:darkred
        end
        
```


```mermaid
gantt
    title A Gantt Diagram
    dateFormat  YYYY-MM-DD
    section Section
    Task A       :a1, 2024-01-01, 30d
    Task B       :after a1  , 20d
    Task C       : 2024-02-01  , 20d
```


```mermaid
graph TD;
    A((A)) --> B((B));
    A-->C;
    B-->D;
    C-->D;
```


```plantuml
    @startuml
    a->b
    @enduml
        
```