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