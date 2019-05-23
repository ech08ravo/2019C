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

## Component Diagram 2 based on the "Learning Analytics Platform"

This component diagram shows components of the Learning Analytics Platform. The Learning Analytics Platform is an automated authoring engine that collects and filters interaction data from the Instructor and Learner. The Instructor and Learner will engage with the Learning Environment, where the xAPI will collect user experience data and feed back to the Learning Analytics Platform. The Learning Analytics Platform feeds to the Personalisation Engine, which feeds to the Learning Environment.
The System designer manages and adds to the Cloud Repository and Learning Analytics Platform. The Instructor is able to both use and add to the Learning Analytics Platform data. 

![component diagram #2](https://www.plantuml.com/plantuml/img/RPB1JiCm38RlVWghdBi3nscQLjeALUgXeaCS48VGULr4wbH92fictXqtZ0aaUahzVqw_Ejdue5oO1WDR7GnXReVHCd70GglUgG5lRW56rRsfdZ2fIJdMt6F6ofo2xZmsHeMzTKE2ocDTDdX6w8oTTfXK7CW9Y9sL5OU8I17FWF8yvn5xeD5w7QmxlSnvNXVVQLQ9pUGyuJqnEIL41B8gB-0J09wVw1LRCUeEM7AlcMB-r9OmvtTsufrofr_M9RzhPtduSQdBtrX3pblHrLu5RVcoPmGR0NFv2MSD9iUigMBr291reeL9U_A11Yp8wrvSOzeMrpWANChrjLgn3swQrp7O0ipZItVsWzFr_CcclBw9wHokKaFxaE8H4ThYcihCS8c3OZaa3pMcJlU7S6d3nM8Q5ukrD2rbeiPG5nuzkV8uajF47HKgADZ-wTh-ruKNS9McqvX6i84DyMw-Fry0)

```
@startuml
Title Component Diagram #2

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


## Component Diagram 3 based on the "Personalisation Engine"

This diagram represents the components within the Personalisation Engine. The Course Designer is the main human actor at the controller layer here because he is the one interacting with the Personalisation Engine setting the boundaries of the intended course design. He will also set the learning objectives and the pedagogical patterns he considers suitable for the course. The next component is the Product Layer which contains the Learning Environment where the course will be deployed. 

![Component diagram #3](https://www.plantuml.com/plantuml/img/LP2nQiD038RtUmhXpfcwbn3Rco47yHOwg3vnN7kMWavEAANltdC2mHs5Vdryl_R5K6sPinkJPO9MveimiK6NC2hEyFBgBZXzOIHeF6aHnfmAMXA6dcDYQW0B-1v-t7aWL4uSuVZnIPEbAnKOHVBx6XcEepjx2XWbfWapU3GZvKt4-nevaS515WweQNj_EepkrsriLC8o6GpuJVgG65Q9vcdHypMfy5pxD0-57luXMc5JoPbqGsdlb7MvQ27egAJ8TNSdjDqAg95Ta1lltcfnLxi_fy7jYSFwq3y0)

```
@startuml
Title Component Diagram #3
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
```

## Component Diagram 4 based on the Internet of Things

This component model outlines the key system elements for the Internet of Things. At the Devices level, the Learner will utilise a device/series of devices including smartphones, tablets or personal computer to access the course via the internet. This activates the LMS Layer whereby components including data access, course pages and deployment options are provided back to the Learner device, through the internet. This interaction is reciprocal with the Devices layer where data and access is fed back to Learner devices upon request.

Within the internal system of the LMS itself, the authoring tool and formatting support such as SCORM or Tin Can will offer monitoring or modification options to the Instructor.

The Learning Analytics Platform consists of the xAPI data storage and the Analytics processor to to process the data for the Instructor.

![component diagram #5](https://www.plantuml.com/plantuml/img/VL91QiCm4Bph5KjElVW7fSJO10mfCTYtKCp6LX9HMMiakMq8-NjNKkhI7Eg3iMR6gvcHriwZzVEeXLTUIwYnVyUJT911PRoqHdgW8xHdPKuE2XedCj9uA1MUB8vYIdfObV93zT9rMxn8kuAh07xwHR-lfNLaKCSPCqz-0tHG5u-wPcG_qvbNKT3KZu8M3rhwIBRY9dfDy_3hzSeG24C3Mzg-DZz6zWNDreLud2t-MwJ1-n8zGjwpzOIN-HsNawRB6BRSJLwHkTExm2P9FlipMIu6MY8TwRnDr8RiYDu7hfcdYQpFe5K62ZHHjscYJWNRH-mbiDUkMbQiOA0IDn03-pkW2t4aMiCJkvnhl7ZLkwxMw8-yrH9peQ2s539HwZc_f_tAwmeY4hwugp_71jb0doPxMUeKIw_FYNfAllZ520l_yVGmEibV6x6MPk3xzWq0)

```
@startuml
title Packages - Internet of Things Component Diagram
package "Devices_Layer" {
    component [Personal Computer] as PC
    component [Smartphone] as SP
    component [Tablet] as T
}
cloud Internet {
}
 
node "LMS" {
    [Course Pages] as CP
    [Data Access] as DA
    [Deployment Options] as DO    
    [Authoring Tool] as AT
    [Formatting Support- Tin Can] as FS
    interface LMS_Interface as LMSI
} 
database "Learning_Analytics_Platform" {
    [Analytics Processor] as AP
    [xAPI ] as xAPI
}
Devices_Layer -down-> Internet
Internet <-down-( LMSI
LMS <--> Learning_Analytics_Platform
Devices_Layer <--> LMS
@enduml
```
