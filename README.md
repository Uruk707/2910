# Project Title

## Entity-Relationship Diagram

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
---
### Data Dictionary

#### Table: `PASSENGERS`

| Field Name  | Data Type | Constraints                               | Description                                             |
|-------------|-----------|-------------------------------------------|---------------------------------------------------------|
| `id`        | INT       | PRIMARY KEY, NOT NULL                     | Unique identifier for each passenger.                    |
| `first`     | VARCHAR   | NOT NULL                                  | First name of the passenger.                            |
| `last`      | VARCHAR   | NOT NULL                                  | Last name of the passenger.                             |
| `flight_id` | INT       | FOREIGN KEY (references `FLIGHTS.id`), NOT NULL | References the flight ID for the passenger's flight.     |

#### Table: `FLIGHTS`

| Field Name    | Data Type | Constraints                     | Description                                          |
|---------------|-----------|---------------------------------|------------------------------------------------------|
| `id`          | INT       | PRIMARY KEY, NOT NULL           | Unique identifier for each flight.                   |
| `origin`      | VARCHAR   | NOT NULL                        | The city or location from which the flight departs.  |
| `destination` | VARCHAR   | NOT NULL                        | The city or location where the flight arrives.       |
| `duration`    | INT       | NOT NULL                        | Duration of the flight in minutes.                   |



### Summary
- The **`PASSENGERS`** table stores individual passenger data, including their assigned flight through the `flight_id` foreign key.
- The **`FLIGHTS`** table stores details about each flight, including its origin, destination, and duration.


    

    
