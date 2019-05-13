# Use Scenarios and Use Cases

> This page contains the meta-design use scenerio, followed by use cases that extrapolate key aspects of the Learning Design (LD) system proposed. It offers a clear break down of the users involved and aspects of the system that are at the core of this proposed adaptive learning design system.

## Use Scenario - AI Adaptive LD System

The adaptive course design system offers automated and authoring tools for the designer to adapt the design to the needs of the users.
- The System designer will manage the Cloud Depository and Personalisation Engine. Also offers technical support and administrate.
- The Course Designers will use the Personalisation Engine user interface to input requirements such as duration, pedagogical preferences and/or activities.
- The Personalisation Engine will feed the information through the cloud depository and web, then generate a Learning environment appropriate to the boundaries set.
- The Course Designer will review and approve or modify the LE produced
- The Instructor and and Learner will engage with the Learnign environment, where the xAPI will collect use experience data and feed back to the Learning Analytics Platform which feeds back into the Cloud Depository and Personalisation Engine

![Submit Rule](https://www.plantuml.com/plantuml/img/bPCnQyCm48Lt_OeRao5q3wKa91a26G8TEeQBT7KFx9FHdTs6qlzUsORIj4dZJaBItVkUdgI56YPhgj8vOoi9bW5huvPWjuR7anfLBf4tbABRt1w6DNW7DzbJqYXOig9n5DX8mK9Jk9-5-2gp1vYiOfEKz6uZBQSe5OafhChO15XJ7PKjfjDqbDGJ7Rl27M4IbWAMkVfax1Ns9TfpJDKKPlzYtfQwuigDPVGYNvXlnMVui_M-vMsvttObmtYkSici-t1kk9V3cfGBeVIlBEOOAXPMIsW4bwKksvtNAROS28py2sXJrp4Pk87xG-7Q7S-L38wnaO29IS5j9JjfVFRs9pfGcTzfKa09K4Nf3gE_ciT5u7h6ZREo62NqDX1zB4iynYuoXPOHTXiubncRFac1HHPXoHyiXrZaYL57wFl18bIKCqAFWIhs84H1dLkGXFnpFm40)

```
@startuml

title Adaptive LD System
rectangle AI_System { 
(Personalisation Engine) <-down-> (Courses/Environments Cloud Depository) 
(Personalisation Engine) <-down-> (Web) 
(Learning Analytics Platform) --> (Courses/Environments Cloud Depository) 
(Learning Analytics Platform) --> (Personalisation Engine)
(Courses/Environments Cloud Depository) --> (Learning Environment) 
(Learning Environment) --> (xAPI) 
(xAPI) --> (Learning Analytics Platform) 
}

System_Designer --> (Courses/Environments Cloud Depository) :administrate 
System_Designer --> (Learning Environment) :provide tech support 
Course_Designer --> (Personalisation Engine) :set boundaries 
Instructor --> (Learning Environment) :delivers and monitors
Instructor --> (Courses/Environments Cloud Depository)
Learner --> (Learning Environment) :interacts and collaborates via LE 
Learner --> (Courses/Environments Cloud Depository) :engages in AI suggested courses to meet academic needs

@enduml
```

## Use Case 1 - Personalisation Engine
As Learning Design research shows that the context of learning and the need for systems to be flexible, adaptive and user friendly, the Course Designer will input boundaries or design requirements into the Personalisation Engine.
The Course designr can engage with the Personalisation user interface to determine one or all of the following:
- Learning objectives
- Monitoring needs
- Pedagogical patterns
- Learning platform
Based on the set of boundaries and requirements set, the Personalisation Engine will then generate a learning course and environment appropriate to the learning context for the Course Designer to review.

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

# Adaptive LD with Design Critique Integrated

In a LD with integrated Design Critique process, the following would apply:
- The Course Designer engages with th Personalisation Engine user interface
- The Personalisation Engine will generate a Learning Environment
- The various stakeholders and designers will engage in a design critique
- If approved, it will then be deployed as a Learning Environment for the instructor and learners to engage in
- If not approved, adjustments will be made by the Course Designer using the Personalisation Engine and re-proposed for critique until approved.

![Submit Rule](https://www.plantuml.com/plantuml/img/ZLFDReCm3BxxANmiXxv0DKsjO0Sa3aWzx5Xbu55FaB34gOIwlVi2T5sxfLfF1FlxYwsidIWhlci1XAKbtDIg5puG5Xbk1oVK0SpVNKQE6qqMbSDj1gdnrj5LDSqWrqwihyHCXHmAKlRKBGAbwxnc6SnhQLKbND54Am4iLQ9qCoR8TxCX7X5WKP9rHgkMdH8s6fzqmveIV5Wk7t6HjiRNc55l70VF8S7_6C_qaa24DpLBQqA5QfnYisu2-S3Mw8wq1EtFow2d0Mpwtfg3Ql48YtaOc5eMVlUJf-LcBwFsfdxpJaOX5m9S_k45w2IMZ5R_nPaY_xQCX5XUA_ySlnNwrWnnZx3yBA0-8aQu8jseXXoodb6nVK1w5_-CkffB775E_wSzRl36ybVLteHHEaZBU_BazuAYTovkDM1DkXvVsnS0)

```
@startuml

title Adaptive LD System

System_Designer as SD
Course_Designer as CD
Instructor as I
Learner as L
CommunityofPractice as CP

rectangle AI_System { 

(Personalisation Engine) <--> (Cloud Depository) 
(Personalisation Engine) <--> (Web)
(Cloud Depository) --> (Proposed Learning Environment) 
}

rectangle Course_Approval {
(Design Critique) <-right-> (Adjustments)
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
CD --> (Personalisation Engine) :chooses
CP --|> (Design Critique) :engages in
I --|> (Design Critique) :engages in
I --> (Cloud Depository)
L --> (Cloud Depository)

@enduml
```

## Design Critique Use Case

Users:
###Presenter (Course designer who has the most in depth and context specific knowledge of the model)
###Facilitator (System Designer who establishes the key goals to assess the design against)
###Note-taker (Instructor)
###Community of Practice (includes developers, other product managers, stakeholders, pilot students, learning experts, etc)

Use case could involve the broader categories of:
- Facilitate: sets agenda, location, goals to critique against, models to be presented, invite critiquers, set key roles)
- Critique Goals: these are the goals established by numerous stakeholders of the business and design process, learning goals, UX and/or UI design goals)
- Discussion: includes ways of discussing that is separate to a brainstorm or giving general feedback. Could include looking at use case scenarios, clarifying questions, avoiding using absolutes, design alternatives (but not problem solving)
- Post-meeting Actions: presenting feedback notes to keep everyone in the loop, publishing actionable tasks for follow up

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
