# Project Title

## Entity-Relationship Diagram

![ER Diagram](diagram.png)

## ER Diagram Code

```mermaid
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

    

    
