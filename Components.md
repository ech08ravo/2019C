# Components

Keep your components in this document, or create further documents of this kind if documents gets too long. Note that when you render the markdown in html you can get an url for any heading by pointing to the left of the heading and then right-click and copy the heading bookmark link. 

[Link to wiki page on component diagrams](https://github.sydney.edu.au/crli/EDPC5022-2019/wiki/Component-Diagrams) 

## Component diagram 1
This component diagrams shows the different layers of which the system architecture is composed of. 

![component diagram #2](https://www.plantuml.com/plantuml/img/JP71JiCm44Jl_WgBUty1jOev81aKARbL7BRnAhLmTgFrfb0X_XqxW9ARn_QR6Q-FMK5qcP8nVTI4jk5fPa9IwoAC0fCX3cWV6YOLJWd5UhYZF5Z8jl7sovmRNYIZTPZZI2XlvjmflEELKq39HNe4MG--_ymwb5iSCE-ikjNg5J5KegHb5OYaLRKOOEGn3f3i3AeeLBTVcAAomANKJZKYqcZp877MBQfdJlkS_hTouYKSBf0nM5Zqob9PBNUBx-bvmnqex6YtqWvdpZNwNXyNBmBhwlFKxiXME2o3xk1sXVr_qoUwHM6QogmhPSem3u4_wF1OXc6wJVNUz9jothXDjTwO8r8eF_W3)


```
@startuml

Title Component Diagram
node "Controller Layer" as CL {
[Course Designer]
[Stakeholders]
[Learner]
}
node "Services Layer" as SL {
[Needs]
[Constraints]
[Pedagogical patterns]
[Monitorable learning script]
}
node "Tools Layer" as TL {
[Cloud-based authoring tool]
[AI]
}
node "Data Layer" as DL {
[Depository]
[Library]
[xAPI]
}
node "Product Layer" as PL {
[Learning Environment]
}
[Course Designer] ... [Needs]
[Course Designer] ... [Constraints]
[Course Designer] ... [Pedagogical patterns]
[Monitorable learning script] ... [Cloud-based authoring tool]
[Cloud-based authoring tool] ... [Learning Environment]
[Cloud-based authoring tool] -right... [Depository]
[Cloud-based authoring tool] -right... [Library]
[Cloud-based authoring tool] -right... [xAPI]

CL -down-> SL
SL -down-> TL
TL -down-> DL
DL -down-> PL

@enduml
```
## Component diagram 2


![Component diagram #2](https://www.plantuml.com/plantuml/img/RP3FQiCm3CRlUWgHUrvWZD8rwM5GgA4v3CeEMg8QhuvKR7L_67ltEUbMUfXFjlHzFttoCXibEuyHm895HiSfgr0CcIoeu5fy4CP6nvCAYs4Ro2SQ0KxK7yapLlzRAgICRerViDym9GdYSVloohs5DyxOgSRdIRBPTh1tF91N7tgAwCYCazn8d2kI7Hkkz2m3fN3htwqw-0RuRNrYTPtc8jb1qpWdsJW4Q5GiQSJguy4zpkMdKgNUD67Lw3bbnfPpyC9fRZTjCRLO3_ekzMBEEZqNSwJBRPfVrhol8n-iBi0x75L2GUOByG-O9zcLvA2S9Sim_VqF)

```
@startuml

title Personalisation Engine Component Diagram

package "Personalisation Engine" as PE {
[Learning Objectives Tool] as LOT
[Pedagogical Patterns Tool] as PPT
[Set Boundaries Tool] as SBT
}

Boundary "Learning Platform" as LP 

Control "xAPI" as X 

actor "Course Designer" as CD

CD -down-> LOT
CD -> PPT
CD -> SBT
PE <-left- X : monitorsCourseDesigners
PE -down-> LP

@enduml
```


## Component diagram n

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.
