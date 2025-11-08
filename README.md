---
layout: mermaid
title: Diagrams demo
permalink: /
---


# pages-klooien


Emoji!

:blush:



Ik ben een zeemeermin:


```mermaid
classDiagram
    class AvailableGame {
        <<enumeration>>
        Blackjack
        Roulette
        Uno
        The Crew
        Love Letter
        High Society
    }

    class Lobby {
        - List<> players
        - Player host
        - AvailableGame chosenGame
        ...
        +join(Player actingPlayer)
        +leave(Player actingPlayer)
        +start(Player actingPlayer)
        +end()
    }
    
    class Player {
        +String username
    }
    note for Player "Je mag aannemen dat username uniek is"

    Lobby "1" --> "*" Player
    Lobby ..> AvailableGame


```


En ik ben een boerenpummel:

{% plantuml %}
@startuml
 class Example {
    - String name
    - int number 
    
    +void getName()
    +void getNumber()
    +String toString()
  }
@enduml
{% endplantuml %}



PlantUML is kennelijk ook nukkig, want dit is **iets anders**??

{% plantuml %}
@startuml
testdot
@enduml
{% endplantuml %}


En is testdot eigenlijk wel goed genoeg?

{% plantuml %}
@startuml
left to right direction

cloud "Azure" {

    node "Some Virtual Machine" {    
        frame "MyApplication.jar" {            
            rectangle "Vite Frontend" as fe             
            rectangle "Backend" as be
        }
        database "Postgres" as pg
        
        ' Dit is echt fucking zwarte chatgpt magie
        fe -[hidden]down-> be
        be -[hidden]down-> pg

        be -> pg
        fe -> be
        
    }
}

@enduml
{% endplantuml %}