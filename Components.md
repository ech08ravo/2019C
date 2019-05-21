# Components

The below Component Diagrams illustrate and explain different elements of the system and how these elements (or components) or organised.

Component diagrams can also be described as a static implementation view of a system. Static implementation represents the organisation of the components at a particular moment.

A single component diagram cannot represent the entire system but a collection of diagrams is used to represent the whole. As such there are several Component Diagrams below illustrating this system.

## Component Diagram 1 based on Use Case Scenario "Adaptive LD System"
This Component Diagram shows the different layers that the system architecture is composed of and it was modelled based on the Use Case Scenario called "Adaptive LD System". 

1. The "Controller Layer" reflects the different human actors involved in decision-making processes (Instructors, Course Designer, Learner, System Designer) and also Stakeholders which do not appear in the Use Case because they do not interact with the system directly but are part of its architecture at a meta-level.

1. The "Personalisation Layer" represents all the components within the Personalisation Engine and these components are the ones the engine feeds from to personalise content and are also the one human actors input into the engine to set boundaries for course generation: Learning Objectives, Monitoring Needs, Pedagogical Patterns, and Monitorable Learning Scripts.

1. The "Tools Layer" involves all the external tools the system feeds from to adapt content and it's composed of: the AI, the Web-search Engine and the Learning Analytics Platform.

1. The "Product Layer" represents the Learning Environment which is the ultimate end-product the system generates. 

2. The "Data Layer" respresents the components that are involved with tracking and storing xAPI and Cloud Repository.

![Component Diagram based on Use Case Scenario](https://www.plantuml.com/plantuml/img/LL9DJyCm3BtdLqJZl0D_06rgTvXKe6ALE4mxU8tf0gazEUwWGlntqZ5OE3x7xoClMKG5qQ4FnZHU0zg2-oCJajhIGoVGsvjRG-pGpWec5Gu1nLOmeimiH5jKzjDi2nuaeYqn-evGTcQxKNZ30mU74XEi4EHoC4R5FbzTKrGPMkK4lYvUTQ8nGV0Hr3DbXZMU7S-2dZhxk7_5Llq99vjx9fzqfla3efj6DJhekFCj15k3AWfbcx1FT_xJshJYZtfDqJ27c7atP-lbEl6VSMytYTSUx8ewJxZBCYrJyb5zcz86q1UM_gfPWa8cMVxq5tXmzWcF7ATKOnBxMDRhh0zXbohAU_XVmufENfZwz78JowHtcJj-f_dTr9YPMll5JMMQAoehKsQxbJ4B99T-n3S0)

```
@startuml

Title Component Diagram #1
node "Controller Layer" as CL {
[Course Designer]
[Stakeholders]
[Learner]
[System Designer]
[Instructor]
}
node "Personalisation Layer" as PeL {
[Learning Objectives]
[Monitoring Needs]
[Pedagogical Patterns]
[Monitorable Learning Script]
}
node "Tools Layer" as TL {
[AI]
[Web Search Engine]
[Learning Analytics Platform]
}
node "Data Layer" as DL {
[Cloud Repository]
[xAPI]
}
node "Product Layer" as PL {
[Learning Environment]
}

CL -down-> PeL
PeL -down-> TL
TL -down-> DL
DL -down-> PL

@enduml
```

## Component Diagram 3 based on the Learning Analytics Platform

This component diagram shows components of the Learning Analytics Platform. The Learning Analytics Platform is an automated authoring engine that collects and filters interaction data from the Instructor and Learner. The Instructor and Learner will engage with the Learning Environment, where the xAPI will collect user experience data and feed back to the Learning Analytics Platform. The Learning Analytics Platform feeds to the Personalisation Engine, which feeds to the Learning Environment.
The System designer manages and adds to the Cloud Repository and Learning Analytics Platform. The Instructor is able to both use and add to the Learning Analytics Platform data. 

![component diagram #3](http://www.plantuml.com/plantuml/png/RP31Qjmm443lynM3xzeFA274jKqn-63gBJc47bJln16LHsOqRhs4_djbTN6tq3r9yzwi7tgAQaNNsOCwzOHLc9V0n1hH_BrWxUmaTWPOxFZTJeH5HrROyOGbMtzLDqRilTNN87E1DcBNzFYECFgmNh1eMKcIY6D89zQif26-0wRVIvMrpxI4w3J8zUlEgwx-GyisfQmI2JyHazXaPA5ignf-0S3BCtt38HMDRzZmv9WoVnuQsFd7iFB5olMkkk4VJWBFkINdtcizIGmfrqMhBl3jFxFO9x4Ah18y5blPjtcw0PHZoi9Yk4Qb6MkARagjcGxrWNF0RTmTqvQZohgVCpW3xCzdBk4dcyVzatrptBecmmVZwLKDReWmr0TDRuOVSBPi9uhGeH4tlUbj3K-dTJcT7d5BJXMyfr6_H99cMqWSyKYrLGldVxRE_zl2c_XWpBgOBFRmH7nPP_yR)

```
@startuml
title Components - Component Diagram

package "Learning Analytics Platform" as LEP { 
cloud "Internal content" as Int {
    [Cloud Repository] as CLD
    [AI Course Generator] as AICD
}


[Web Search Engine] as WSE

}

Boundary "Learning Environment" as LE

Boundary "Personalisation Engine" as PE

Control "xAPI" as x

Actor "System Designer" as SD

Actor "Learner" as L

Actor "Instructor" as T

LEP -down-> PE
PE -down-> LE
LEP <-left- x  
SD -down-> CLD : manages
L -right-> LE
L ..up..> x : CollectUserExperienceData
T -right-> LE
T ..up..> x : Collect Data
T <--up--> LEP
@enduml
```


## Component Diagram 4 based on the Personalisation Engine

This diagram represents the components within the Personalisation Engine. The Course Designer is the main human actor at the controller layer here because he is the one interacting with the Personalisation Engine setting the boundaries of the intended course design. He will also set the learning objectives and the pedagogical patterns he considers suitable for the course. The next component is the Product Layer which contains the Learning Environment where the course will be deployed. 

![Component diagram #4](https://www.plantuml.com/plantuml/img/RP31QiCm38RlVWgHYqzzXL6QvXQeeRcL7RH466-EL6IbOuoz-vmMIWOx2ltw-7vvxvtR5qErPSxEacM2G5g4CQU2beIXuvYOe9NvAaniS4mO5MTtnV438q7p_qK3M21qyEqkFQ5ouWYdjtSQBTsem22INzT8VnhS9T24KM8QCKD0CrBUH4AeaJCP76JX2JLjxy-7mVsuZOtAj8m6FNwHFYJwLQ9vMdHyIoeyrpBDGw63FuXMs5Ho9jrGsZjbNIvQ28vKKkIwknFQumgeaTqadxnxgSLTxVwSUhSddjOdE-_zBm00)

'''

@startuml
title Personalisation Engine Component Diagram
package "Personalisation Engine" as PE {
[Learning Objectives Tool] as LOT
[Pedagogical Patterns Tool] as PPT
[Set Boundaries Tool] as SBT
}

package "Product Layer" as PL {
["Learning Environment"] as LE 
}

package "Controller Layer" as CL {
[ "Course Designer"] as CD
}

CL -down-> PE
PE -down-> PL
@enduml

'''
