# Santander Dev Week 2023
Java RESTful API criada para a Santader Dev Week.

## Diagrama de Classes 

``` mermaid
classDiagram
    class User {
        - String name
        - Account account
        - List<Feature> features
        - Card card
        - List<Feature> news
    }

    class Account {
        - String number
        - String agency
        - float balance
        - float limit
    }

    class Feature {
        - String icon
        - String description
    }

    class Card {
        - String number
        - float limit
    }

    User "1"-- "1"Account
    User "1"-- "N"Feature : has features
    User "1" -- "1" Card : has card
    User "1" -- "N" Feature : has news
```
