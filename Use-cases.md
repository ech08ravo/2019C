# Use Scenarios and Use Cases

> This page contains the meta-design use scenerio, followed by use cases that extrapolate key aspects of the Learning Design (LD) system proposed. It offers a clear break down of the users involved and aspects of the system that are at the core of this proposed adaptive learning design system.

## Use Scenario - AI Adaptive LD System

The adaptive course design system offers automated and authoring tools for the designer to adapt the design to the needs of the users.
- The System Designer will contribute to the Courses/Environments Cloud Repository and provides technical support to the Learning Environment.
- The Course Designer will use the Personalisation Engine user interface to input requirements such as learning objectives, pedagogical patterns, monitoring needs, learning platform, duration and/or activities.
- The Personalisation Engine will search for information through the Courses/Environments Cloud Repository and web.
- The Personalisation Engine will then feed back to the Personalisation Engine and generate a Learning Environment appropriate to the boundaries set.
- The Course Designer will review and approve or modify the LE produced.
- The Instructor and and Learner will engage with the Learning Environment, where the xAPI will collect user experience data and feed back to the Learning Analytics Platform which feeds back into the Courses/Environments Cloud Depository and Personalisation Engine.
- The Instructor is able to access the Learning Analytics Platform to make teaching and learning decisions.
- To reflect the democratic process of learning design, the System Designer, Instructor and Leaerner are able to contribute to the Courses/Environments Cloud Depository.

![Submit Rule](https://www.plantuml.com/plantuml/img/ZLCxJmCn3DxpAposGyLU8TIgxL2fGmK3OvLBp3NIdNsoVOKAyT_9SKX0kJwcI8w_XpydCpKlrjQLSvQiGfX7trWw86oMy7HKmze91lDKTfVhNL-3Tt2ZBOeo-IgfjyG4AoeJuHZk9v5VQV80esSinXSR9PLxwpeNt8gYtgtea8IfHZA5HSLjX4TiM9En72znJJgM3NgXH2NyeXcxd_8y0u-MWiAsylR2Kdy3px2wOSOUypRVhZj7_VbNVqZece-skJq8z-7wHUoMgAaabDx0ZJ5E0vD9Abf31MCO9XkUVTe87rBiW1Zse6tJi1YuNlg4ujosfehPMC4jHIyfSxargKaRih-BuX6h_3X5mLE4cgaRIF-1Ruq1V8nT0EVLXpQLOI6WPW7trNSbhqI6ueFrdWDNbIzOl9t2RpMDLFeoHvO8d9iXnVnxFm40)

```
@startuml

title Adaptive LD System
rectangle AI_System { 
(Personalisation Engine) <-down-> (Web) 
(Personalisation Engine) <-right-> (Courses/Environments Cloud Repository) 
(Personalisation Engine) --> (Learning Environment)
(Learning Analytics Platform) --> (Personalisation Engine)
(Learning Environment) --> (xAPI) 
(xAPI) --> (Learning Analytics Platform) 
(Learning Analytics Platform) -up-> (Courses/Environments Cloud Repository)
}
System_Designer --> (Courses/Environments Cloud Repository) :contributes to 
System_Designer --> (Learning Environment) :provides tech support 
Course_Designer --> (Personalisation Engine) :sets boundaries 
Instructor --> (Learning Environment) :delivers and monitors
Instructor --> (Courses/Environments Cloud Repository) : adds to
Instructor --> (Learning Analytics Platform) : accesses
Learner --> (Learning Environment) :interacts and collaborates
Learner --> (Courses/Environments Cloud Repository) :engages in 

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
- The various stakeholders and designers will engage in a design critique based on the Proposed Learning Environment
- If approved, it will then be deployed as a Learning Environment for the instructor and learners to engage in
- If not approved, adjustments will be made by the Course Designer using the Personalisation Engine and re-proposed for critique until approved.

![Submit Rule](https://www.plantuml.com/plantuml/img/ZPF1ReCm38RlVWeVow4lK4rJAzW1YGDI3pjM6NYf9qXOubH2tTvz0RgktQZM4n3__lyF6zPUb9FGDW32qX1kQjK97mYB3BUz5se1fkik8y_Qa4FbSPj1QeFpT7MQPf0RBovKOiU370fIxbGjOalR1iFIszVIgKgueh6j171KYJ9w8CXtKo0U4M1HalFMg8Qz4hO6duncGma-B9UFk4WR6shCgBEUOsQVu7yTp_IItDQCajBPw4SrZl1iT2mVs5dJaf6Oy7c9Unh3fkkSFQW6Zx2OHeAfO-7tC2OxrdiPl3VrM_0o6Fc8SVc45wAJMJ94_OSp8l-Ed85ONZl_t7uxT8tjvpFY9v15rSTC4Ax8QAN98vj9DRSLIE_gFwkkvZAlEDF_AGyRlB7ULRMtSPGUql8UdlnUqUmx5xSAi2PJnt_k2m00)

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
(Personalisation Engine) --> (Proposed Learning Environment) 
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
