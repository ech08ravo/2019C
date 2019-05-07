# Use Scenarios and Use Cases

> This page contains the meta-design use scenerio, followed by use cases that extrapolate key aspects of the Learning Design (LD) system proposed. It offers a clear break down of the users involved and aspects of the system that are at the core of this proposed adaptive learning design system.

## Use Scenario - AI Adaptive LD System

The adaptive course design system offers automated and authoring tools for the designer to adapt the design to the needs of the users.
- The System designer will manage and add to the cloud depository and both Personalisation and Learning analytics engines. Also offers technical support and administrate.
- The adaptive course design system offers Course designers of using a Personalisation engine or a Learning analytics platform.
- If using the Personalisation engine, the Course designer will input all necessary data including desired LMS platform, duration, pedagogical preferences and/or activities.
- The Personalisation engine will feed the information through the cloud depository and generate a Learning environment appropriate to the boundaries set.
- The Instructor and and Learner will engage with the Learnign environment, where the xAPI will collect use experience data and feed back to the Learning analytics platform.
- If using the Learning analytics engine, the Course designer will activate it and it will use either the Cloud depository/web search engine or both to then generate a suggested Learning environment.

![Submit Rule](https://www.plantuml.com/plantuml/img/bPCnJ-j03CVt-nGUOG3s38YATgZKeL87HkJcJB1qvulEJlMg9xuxJlB4erA1CYLnV3___xRlGGsh3Jc5O6o9O16nDpuGR9QmEwfH3fLQG-d6d-ldEGP_8LnjgMeHJAneN0HMqh7GDTpStCFLOncgajwjvC2rI2OnXSTKXWXBwekobNgyTig6i0fB1mj77OrRXMr2Uoar_qCzqHvsdjM-VfG8vu9JyWVkK-7Boboi-CB4o-ISnASZVnRRzPWoFqyfvyI7jn3cgJmlIRaJghyor63CBAnMqGZEeyxBRVfQ3Xm9Z7mCElHzgGPXhlkVS7lhXA-MfL4os9T18bOc_UBqjmreG2dvZYhWO2MxY-YR2kq4WewSWcuLmbhSvD2Exz-vYfJy0bJ7IOHSPEoJXYdvXtwmcDUQbFZHjgI4-pAsLU7029iLd6Bc4JSa7NQUmpBgrg7pZz74x4312cJoDc6BaJAt84HHGtWWYUFLVGS0)

```
@startuml

title Adaptive LD System
rectangle AI_System { 
(Personalisation Engine) --> (Courses/Environments Cloud Depository) 
(Learning Analytics Platform) --> (Web Search Engine) 
(Web Search Engine) --> (Learning Environment) 
(Learning Analytics Platform) --> (Courses/Environments Cloud Depository) 
(Courses/Environments Cloud Depository) --> (Learning Environment) 
(Learning Environment) --> (xAPI) 
(xAPI) --> (Learning Analytics Platform) 
}

System_Designer --> (Courses/Environments Cloud Depository) :administrate 
System_Designer --> (Learning Environment) :provide tech support 
Course_Designer ..> (Personalisation Engine) :set boundaries 
Course_Designer ..> (Learning Analytics Platform) :selects automated AI course generator 
Instructor --> (Learning Environment) :delivers and monitors
Learner --> (Learning Environment) :interacts and collaborates via LE 
Learner --> (xAPI) :engages in AI suggested courses to meet academic needs

@enduml
```

## Use Case 1 - Personalisation Engine
As Learning Design research shows that the context of learning and the need for systems to be flexible, adaptive and user friendly, the Course designer has the chocie of inputting boundaries or design requirements into the Personalisation Engine.
The Course designr can engage with the Personalisation user interface to determine one or all of the following:
- Learning objectives
- Monitoring needs
- Pedagogical patterns
- Learning platform
Based on the set of boundaries and requirements set, the AI system will then generate a learning course and environment appropriate to the learning context.

![Submit Rule](https://www.plantuml.com/plantuml/img/XT51IyD040NW-_oAEIQ7DdSFqj1u45fT8dWjQpAk8viPsPqKGVpl9cf5QD3xDxptc4qsdsmS8e2nHK97AQluoDaRg-2L11O2IDIPbt0k3by2tn2A7VaaB05l7vudpqVA9QvMbrXiLOp4IYZsAcoQPdL3r9_0Q-skgtOKuu4cvQZtGGDtFgBpPfJa99inVGR_hUevdeqfutrRrMtvgvsBtXur3Tzqjx-h6ZfoDxK5U0VOwfWo7HhA78GIhjUpMjfsqJsfvYd355bUHbk-FTkyp1Rd_DFcPmi0R4Zw-PKV)

```
@startuml

title Personalisation Engine

rectangle Personalisation_Engine { 
(Learning Objectives) --> (Content)
(Monitoring Needs) --> (xAPI/Runtime)
(Pedagogical Patterns) --> (Duration)
(Pedagogical Patterns) --> (Activities VR/AR)
(Learning Platform) --> (LMS/Devices)

}

Course_Designer ..> (Learning Objectives) :chooses to input
Course_Designer ..> (Monitoring Needs)
Course_Designer ..> (Pedagogical Patterns)
Course_Designer ..> (Learning Platform)

@enduml
```

## Use Case 2 - Learning Analytics Platform
The Learning Analytics Platform is an automated authoring engine that collects and filters interaction data from the Instructor and Learner.
- The Instructor engages with the learning environment by delivering the content, facilitating learning, monitoring course interactions and approving/amending course design suggestions from the Analytics Platform.
- The Learner engages with the Learning Environment by interacting with the learning content, assessments, user interface and pedagogy activities.
The Learning Environment feeds interaction data back to the the xAPI database which generatesweb and depository searches for automated coaching courses for the learner.

![Submit Rule](https://www.plantuml.com/plantuml/img/ZP4nRm8n38Lt_mgFTqFKdG61A0DI1oG6HfGcxX4fSP3ZG57R_zxZK2bLQSNwdhzdFtbIr8hM504qQ2Hy8YiSkCCfstZKu0ekezMNB0b0oAdbhX-xk9il5zyGe7cTBXSj6fyFRDx7sApf6LTzfDlYdBl0rEB8Lit9AdcuPN-pbrFcl0-IEH5hYz3CSfL2vU5ABZYBkNfyf5qkGRCSxmcwhPkw6wXpbT-Lxbn_LVC3OC55fRhUGcF-F6cKCf_mWfOz1bOIw_hqGz0jmi3G_m4_6G2O4FlXlPy0)

```
@startuml

title Learning Analytics Platform

rectangle Analytics_Platform { 

(xAPI) -down-|> (Web Search Engine) :automated
(Web Search Engine) -down-|> (Learning Environment) 
(Courses/Environments Cloud Depository) -down-|> (Learning Environment) 
(Learning Environment) -up-|> (xAPI) 
(xAPI) -down-|> (Courses/Environments Cloud Depository) :automated
}

Instructor --> (Learning Environment) :monitors/approves/interacts with 
Learner --> (Learning Environment) :interacts with

@enduml
```

# Adaptive LD with Design Critique Integrated

In a LD with integrated Design Critique process, the following would apply:
- a proposed learning ebvironment would be generated after the use of a Personalisation Engine OR Learning Analytics Platform
- the various stakeholders and designers will engage in a design critique
- if approved, it will then be deployed as a learning environment
- if not approved, adjustments will be made by the course designer and re-proposed for critique until approved.

![Submit Rule](https://www.plantuml.com/plantuml/img/ZLF1Ze8m5BptAzuH3le17ZOIy43YmSGFC0qyQpVmohOF3N7ttxUesnKNLsxmPZepJ1zBnz9oMrT2iEOAOPt1jdECDPmq7o13fnL1QZNhZnQ5k82stbq1j20TR3EHcjOw74pJJEJasBO5cyiW5y9YmPAKzqdotStd32BQe7M6PAMTP6q8LgGqOGopqfnezWPHMfcsz6aQuxINws9Ox15B1vhOY6YDqf8c1OaNwLWN3ZQLvBsnzNIHlt0ukR76Jx64OBIYexQ6QYH-a7d13PhUg3BT1CMl-zvkHITDOyrHLd0MqSCTUGkhrO5xZwHyRnttaYuMWxTxqaqhxfrUnhz67pgEPHWg_px-A3p_UBzacMTzZXZ10ab9XNqpLzROjOfqqld06lGopWZf7-3vtAF_Rj-YE1ZVfmliPxiUYFcKy6A9LFR_xJS0)

```
@startuml

title LD System with Design Critique

Systerm_Designer as SD
Course_Designer as CD
Instructor as I

rectangle AI_System { 
(Personalisation Engine) -down-> (Cloud Depository) :feeds into
(Learning Analytics Platform) -down-> (Cloud Depository) :feeds into
(Cloud Depository) -down-> (Proposed Learning Environment) :feeds into
(Proposed Learning Environment) -down-> (Deploy Learning Environment) :feeds into
}

rectangle Course_Approval {
(Design Critique) -right-> (Adjustments)
(Adjustments) -right-> (Approval)
}

(Proposed Learning Environment) --> (Design Critique)
(Design Critique) --> (Approval)
(Approval) --> (Deploy Learning Environment)

SD --|> (Design Critique) :engages in
SD --> (Cloud Depository)
CD --|> (Design Critique) :engages in
CD --|> (Adjustments) :engages in
CD --|> (Approval) :engages in
CD ..> (Learning Analytics Platform) :chooses
CD ..> (Personalisation Engine) :chooses
I --|> (Design Critique) :engages in

@enduml
```

## Design Critique Use Case

Users:
Presenter (Course designer who has the most in depth and context specific knowledge of the model)
Facilitator (System Designer who establishes the key goals to assess the design against)
Note-taker (Instructor)
Other critiquers (includes developers, other product managers, stakeholders, pilot students, learning experts, etc)
Use case could involve the broader categories of:
a) Facilitate: sets agenda, location, goals to critique against, models to be presented, invite critiquers, set key roles)
b) Critique Goals: these are the goals established by numerous stakeholders of the business and design process, learning goals, UX and/or UI design goals)
c) Discussion: includes ways of discussing that is separate to a brainstorm or giving general feedback. Could include looking at use case scenarios, clarifying questions, avoiding using absolutes, design alternatives (but not problem solving)
d) Post-meeting Actions: presenting feedback notes to keep everyone in the loop, publishing actionable tasks for follow up

![Submit Rule](https://www.plantuml.com/plantuml/svg/XPF1Ri8m38RlUOeSuO2uSvYeG4oLfes98Us6GkgLY12ps652qzvzYRfsBMkrMvf-lnt_jkV4odCuMI7Oi0Mv13AbamjlsBm7a6kF6eY4yA1PkR91TWtoAKOhfOqrh1Z6Sk9DUU39dHmrn3qgIsDnUz52buPq83Be8jRwQ25h99QPvdYTOdLI5lZX4lE0MYLW-e9e1wcr1mB7uAUvkwIVIP6Lu0hLzyXQjc5rX0FQ0lnmHSrBG7bdNFa_kNsTRlFQzvhkM52J2wkyURkcgCy1g7QYbyrihC_5qYump5pG53BR4zh0mzYMG6uqk9WS4zHfn2-s0YZsIX_b8rR11hZgHktZ9EKCfqX-2R6vKZplAXUYlvE_7Uz5slsTIUEYn_5CyWJ0qIUnmE09RaIthPYTgu68CYp0aiWTiG-QyKVGjcLsZWjZj3cdFEA93-2RLV3KmykEGCpZcALz-mO0)

```
@startuml

title Design Critique Process

rectangle Design_Critique {
(Facilitate) -right-> (Critique Goals)
(Critique Goals) -right-> (Discussion)
(Discussion) -right-> (Post Actions)
(Facilitate) -down-> (Location/Tools)
(Facilitate) -down-> (Presenter/Invitation/Agenda)
(Critique Goals) -down-> (Stakeholder Goals)
(Critique Goals) -down-> (Learning Goals)
(Critique Goals) -down-> (UX/UI Design Goals)
(Discussion) -down-> (Clarifying Questions)
(Discussion) -down-> (Alternatives)
(Discussion) -down-> (Avoid Absolutes)
(Discussion) -down-> (Use Scenarios)
(Post Actions) -down-> (Feedback Notes)
(Post Actions) -down-> (Actionable Items)
}

System_Designer --> (Post Actions)
System_Designer --> (Facilitate) : initiates meeting
Course_Designer --> (Critique Goals) :presents models
Instructor --> (Discussion) :participates
Other_Critiquers --> (Discussion) : participates

@enduml
```
