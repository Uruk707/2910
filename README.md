# 2910
clase de SQL
erDiagram
    PASSENGERS {
        int id PK
        string first
        string last
        int flight_id FK
    }
    
    FLIGHTS {
        int id PK
        string origin
        string destination
        int duration
    }
    
    PASSENGERS }o--|| FLIGHTS : "has flight"

    

    
