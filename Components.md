# Components

Keep your components in this document, or create further documents of this kind if documents gets too long. Note that when you render the markdown in html you can get an url for any heading by pointing to the left of the heading and then right-click and copy the heading bookmark link. 

[Link to wiki page on component diagrams](https://github.sydney.edu.au/crli/EDPC5022-2019/wiki/Component-Diagrams) 


## Component Diagram 1 based on Use Case Scenario "Adaptive LD System"
This Component Diagram shows the different layers that the system architecture is composed of and it was modelled based on the Use Case Scenario called "Adaptive LD System". 

1. The "Controller Layer" reflects the different human actors involved in decision-making processes (Instructors, Course Designer, Learner, System Designer) and also Stakeholders which do not appear in the Use Case because they do not interact with the system directly but are part of its architecture at a meta-level.

1. The "Personalisation Layer" represents all the components within the Personalisation Engine and these components are the ones the engine feeds from to personalise content and are also the one human actors input into the engine to set boundaries for course generation: Learning Objectives, Monitoring Needs, Pedagogical Patterns, and Monitorable Learning Scripts.

1. The "Tools Layer" involves all the external tools the system feeds from to adapt content and it's composed of: the AI, the Web-search Engine and the Learning Analytics Platform.


## Component Diagram 2 based on Use Case Scenario
1. The "Product Layer" represents the Learning Environment which is the ultimate end-product the system generates. 
2. The "Data Layer" respresents the components that are involved with tracking and storing xAPI and Cloud Repository.


![Component Diagram based on Use Case Scenario](https://www.plantuml.com/plantuml/img/LL9DJyCm3BtdLqJZl0i_06rgTvXKe6ALE4mxU8tf0gazEUwWGlntqZ5OE3x7xoClMKG5qQ4FnZHU0zg2-oCJajhIGoVGsvjRG-pGpWec5Gu1nLOmeimiH5jKzjDi2nuaeYqn-evGTcQxKNZ30mU74XEi4EHoC4R5FbzTKrGPMkK4lYvUTQ8nGV0Hr3DbXZMU7S-2dZhxk7_5Llq99vjx9fzqfla3efj6DJhekFCj15k3AWfbcx1FT_xJshJYZtfDqJ27c7atP-lbEl6VSMytYTSUx8ewJxZBCYrJyb5zcz86q1UM_gfPWa8cMVxq5tXmzWcF7ATKOnBxMDRhh0zXbohAU_XVmufENfZwz78JowHtcJj-f_dTr9YPMll5JMMQAoehKsQxbJ4B99T-n3S0)

```
@startuml

Title Component Diagram #2
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

![component diagram #3](http://www.plantuml.com/plantuml/png/RP31Qjn038RlUWhXk_S1IWXnRLCMV33rbXn23wfNyGuTQun6Rhs4ldjdfsRJGdNJ_tsQ4NgAHchhxC6SUSOwp4iG5ejOlZVOE9gKPe25nkyqCHOTaugJ2IiXVpKtHkmzsMlGkK2AsBKzlY6CFgndB8vYh4d4COYnM5PIY6-0gLxgh7tc9KHdGQzVRxpkcZ-qEc8TLesCdrXOAHbPg8vr0xy0uEMPl-70fEC5MvcSSERFGmit_Z6iSYQzlc-Th1zEWymijg_xjzQpnY3aNIHpGVOtizWd4UeWfi5ZiLNzCSSRfAf62uh5S8t6CpOStIIicG_DZlSTzhYxfoUcyRAd9u3R-Sfp-2dbu-tBlhrtNPlXG-dvrKhS465exZJT33_WJ48JH-YmL3TTR1_3ms5T3eT7t99J1-zvj2-HjTqMLiSoSaD6SFfdwlI_ATp5Xx9SbpABFJondDVP_mO0)

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

Actor "Teacher" as T

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
