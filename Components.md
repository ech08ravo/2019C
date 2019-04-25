# Components

Keep your components in this document, or create further documents of this kind if documents gets too long. Note that when you render the markdown in html you can get an url for any heading by pointing to the left of the heading and then right-click and copy the heading bookmark link. 

[Link to wiki page on component diagrams](https://github.sydney.edu.au/crli/EDPC5022-2019/wiki/Component-Diagrams) 

## Component diagram 1
This component diagrams shows the different layers of which the system architecture is composed of. 

![component diagram #2](https://www.plantuml.com/plantuml/img/dPBFQiCm3CRlUGhJU_CCBSaEWsmKsblPGOb5OkPOGLPAozYxpqupah8Goax-8_q-IP-zym8iVMkJv6J4eigexSYX4vKRg1dQn956jSd82PEroAg06_96VINdZ7hsg7BqfdR87ydvAF293LcDxCEnGE0Xy3tA794lfa8_4tb7r34tLF32O9p4qm4rr5IR2gpgG0JPnUitSaQ8eGojsYXkNArynQQJgSY9oCuhP9PwlIt1erRGIqCSAGbPGN7_Ee4v2Cou73loiTmjZc9AXc5ttHzcp859zvNCiEAthnTtCKok3Mx6_3zsgJHDrMp-fUYZAyiv__1g55ypPYLufvVdNEMsREf61lh1t2UPwGsU1EvFjKEdunSVrny0)

@startuml

Title Component Diagram
node "Controller Layer" {
[Course Designer]
[Stakeholders]
[Learner]
}
node "Services Layer" {
[Needs]
[Constraints]
[Pedagogical patterns]
[Monitorable learning script]
}
node "Tools Layer" {
[Cloud-based authoring tool]
[AI]
}
node "Data Layer" {
[Depository]
[Library]
[xAPI]
}
node "Product Layer" {
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
@enduml
@enduml


## Component diagram 2



## Component diagram n

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.
