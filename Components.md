# Components

The below Component Diagrams illustrate and explain different elements of the system and how these elements (or components) or organised.

Component diagrams can also be described as a static implementation view of a system. Static implementation represents the organisation of the components at a particular moment.

A single component diagram cannot represent the entire system but a collection of diagrams is used to represent the whole. As such there are several Component Diagrams below illustrating this system.

## Component Diagram 1 based on Use Case Scenario Adaptive LD System
This Component Diagram shows the different layers that the system architecture is composed of and it was modelled based on the Use Case Scenario called "Adaptive LD System". The "Controller Layer" reflects the different human actors involved in decision-making processes (Instructors, Course Designer, Learner, System Designer) and also Stakeholders which do not appear in the Use Case because they do not interact with the system directly but are part of its architecture at a meta-level. The "Personalisation Layer" represents all the components within the Personalisation Engine and these components are the ones the engine feeds from to personalise content and also the human actors' input into the engine to set boundaries for course generation: Learning Objectives, Monitoring Needs, Pedagogical Patterns, and Monitorable Learning Scripts. The "Tools Layer" involves all the external tools the system feeds from to adapt content and it's composed of: the AI, the Web-search Engine and the Learning Analytics Platform. The "Product Layer" represents the Learning Environment which is the ultimate end-product the system generates. The "Data Layer" represents the components that are involved with tracking and storing xAPI and Cloud Repository.

The Component Diagram based on the Use Case Scenario "Adaptive LD System" aligns with:

The Use Case Scenario "Adaptive LD System" (Parent Use Case) found [*here*](https://www.plantuml.com/plantuml/img/ZLDBIyD04BxlhvYZFHJlHSHGFHGKYY8UosPtZ0l9J9YPL8lutzqq1LzfpMbX-LxxpUoLcXVhcjevIrOZ52ieecyjRH5kh-5XfuODF2h2Gq3oaXZkE6Bj18DvglQKpG7s3kviZQ9ClaxgBJ713LM9S0ONyyYlDB-4ioSiPoU1ageNwv5BxaHHpszecuIfGJA5PSrTX7jiMPEnx4vfpNkLM_H2YIhu9ZDpNzT59kui1OLrxUsPfJaGZwYwSSM1yrQiLtsYuVpfFsRqNuwkdLw4-t3383RNgAaYb270n1eNWSaabPsXWZ6CYus_VT4ARrFiYHXUGBksPJ5mW_KlYMFJMYZcO2Lt5FEYPIst8ZNfGivtqZplOzvNKV0KeM7g7wH_o5Dh01zZNy1nzx59PLe8gDd0xN7_z9N8K7om8NFWklObYxVVzAcXaIfVvSeIWNDNI37_wKy0)

The Interactions Diagram "Adaptive LD System" found [*here*](https://www.plantuml.com/plantuml/img/ZPHFYzim4CNl-XGYUywXrrBAUcqN32wOfCMvAjQi8v0b8ut3-jjt9F_jRhRqPfv-ysRcIVZPet0uT9enLAY15mR1YGQLDPvdIhHETFpf2p_oH8eUrHrucJ56X7NyaDh1UU0PUDKQS0SkF4ypThM3aSAD_521yzO8hRm8bZmthJ8GkIfdKg2u2Z9OZ59j1ybFq5klgC4u6QOdbgra3TUzIvtlkfKWd56c9U2kd3KT68nKcIyJdqUFqFqzyJbRJWlZqGtXEnuKYnwDPxfaZJNehEQ7jwGgedPXr4dXVeI4jXvHDRIe5lXgNJTL9nLZvumVluUz-5Skf3o1f_KRyApuH2y_qTDeLEMaUy2NAGX51oIj5OtL6XeC4GRzst6IfVAz5kCY4rxdx-WwoD7z8rm6kGLAHI1CryVAU59i_9RdHCJwOYsNeEb1kSJ8dzQebPfzoirdLrskrTChdKkcIAFUEtjN4dv1SpiFVMyTpeQN41Dr0V_RWmjkd5rYML9DTPIftwO9r0lSn5rH3nQW9Unvh02izxmFqTChQ6u_h4kaL65AeRTBgxVy73IserSg7t7xE_odOK3-o_53hW-XTm4_OXXxfXRqs_W3)

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

## Component Diagram 2 based on the Learning Analytics Platform

This component diagram shows components of the Learning Analytics Platform. The Learning Analytics Platform is an automated authoring engine that collects and filters interaction data from the Instructor and Learner. The Instructor and Learner will engage with the Learning Environment, where the xAPI will collect user experience data and feed back to the Learning Analytics Platform. The Learning Analytics Platform feeds to the Personalisation Engine, which feeds to the Learning Environment.
The System designer manages and adds to the Cloud Repository and Learning Analytics Platform. The Instructor is able to both use and add to the Learning Analytics Platform data. 

The Learning Analytics Platform Component Diagram aligns with:

The Learning Analytics Platform Interactions Diagram found [*here*](https://github.sydney.edu.au/crli/EDPC5022-2019-TeamC/blob/master/Interactions.md#interactions-diagram-2-based-on-learning-analytics-platform)

The Learning Analytics Platform Use Case Diagram found [*here*](https://www.plantuml.com/plantuml/img/VP6nRiCm34HtVSN17JfbwPYXYE5cCE11o9ILjHbNg2CL8eqsVrzQTe2WGpU2ztHtaWwYb7M-Jivfq8dHHkLClOOK1M-1nanNFBrWXuufnn17r96ccuPUu2VIIyfNE6T7KaRLHj4yBtC54hIEe_dUKFtKlYshCzn0IkyaZEeVpm9tjN-WFMT91WQXfH-ESGoH2-YF3rmpfNd0YR-I16joAqHpkdSieRmMx9phi7j5TyGUORkxu3leXxETAMSJBio3kFCAxg46VGgcrUTPiBtNHjH-3x4aVaIMTfPL-mNnbbOyongQxa9p-YkqcwMreBvd4NEbE61UXjNqm76m7_m5)

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


## Component Diagram 3 based on the Personalisation Engine

This diagram represents the components of the Personalisation Engine. The Controller Level is linked to the Personalisation Level via the Course Designer. The Personalisation Engine contains the Set Boundary Tool, the Learning Objective Tool, the Pedagogical Patterns Tool, Course Generation Function, AI, Repository Integration and Learning Analytics Platform. The Web Engine and Course Cloud Repository feeds into the Repository Integration in the Personalisation Engine. User data stored by xAPI in the Data layer is processed in the Learning Analytics Platform which is viewed through the Learning Analytics Platform Integration in the Personalisation Engine. The Personalisation Engine interacts with the Product Layer which contains the Learning Environment through the Course Generation Function. 

The Personalisation Engine Component Diagram aligns with:

The Personalisation Engine Use Case Model found [*here*](https://github.sydney.edu.au/crli/EDPC5022-2019-TeamC/blob/master/Use-cases.md#personalisation-engine-use-case-model)

The Personalisation Engine Interactions Diagram found [*here*](https://www.plantuml.com/plantuml/img/RLF1QkCm4BthAuRqqFPGUkafXwN6Ri7W1PEo9DUfD4b4RIchaNQRl-z8iRDUg4_clQStRvxbPuuOOXe75MqS25eNAQ2ErZk6nk8Xu0WtJ_00FGNs3WVBc5buSGVh29HI8lS1LhLFWGaQOdjm55Q037MZ34PyHo5MtpiKNV-oqDM3JmOsTF9inVbySTei55jwB-1sWNM4mLbtW4f6dAFLuZfWtFim5crNzOgSR7c6rMVLjmNSmPo-79zITpFOEeuXvVU2jqhL3JpyaBYmbgfEAJ84-frie56yMGaXTBqH-aqCzP5cRBk4jbTLPGp3tZeZoLa9b8b6Y9_uGImbQ3-AjIcDJTExFBqwdOB_8v8x2OfPmlU0pe0EX55coDDTrNRwh0n_RJoghaJQ2R4dCgns5-4QeeW-68PB6RSCqrMO55M_1fOsQ2d9dq2rrr6_MDZeOUxkyHMr7MoKKBd3gIwZn6okieGeFd9mxl1V2I6NC7SWRSd2TYpRbzBX4VOffa2WomtasJeN_BzrEsqXrgWrSOwQEqlvfUpnB7FaR_W2)

![Personalisation Engine Component Diagram](https://www.plantuml.com/plantuml/img/RLF1Rjim3BthAuXSTiel34rjjmWWe49g80MC7XYRyxJ9L239tO9X_pvAILC7tIal8FaU-Pvy5nE6D4zE9PiSWQ4GFQEp4PFr30sFbWagFnqz4oUeBOu19wMEsF_4aM1LUKx1EqS1D9ueh00ZL1h-g2uNvn09QefsPAczbcAj_YerOC83Id7rVz72OvhCema3MnxXwV23-cJVA4BhlIji-gbLdQ41Hp_Q7XqOJ8a2BrgCaPPdId3lPnumsENyytsxKDZ87gTaUnbocBxvCC6M4ydDURMpuCPiLRUZeuys-N3wrB2JykNmHvAhprSzpDnVMwh71zLjjWLljhTsr88MLjR5oZqTBhwKcNsZkj-oH_dpSfMhd9y7-5Zjh5Njii0rC1FyCFTf8M6AnEfgGiDlDdYU9F1pOhg16ufiNbmGjFecfiyclXkNMRxaGJ-dB2jnoBkfj987i-w-ss4WVbrBx1zTxNjNhLLzqzLg9UzZFVXVlFugR4AIVnib5uCWoM7VN80Odf5kb6nHK4xnvOBK7V4WNy4_)

```
@startuml
title Personalisation Engine Component Diagram

package "Controller Layer" as CL {
[ "Course Designer"] as CD
}

database "Personalisation Engine" as PE {
[Learning Objectives Tool] as LOT
[Pedagogical Patterns Tool] as PPT
[Set Boundaries Tool] as SBT
[Learning Analytics Platform Integration] as LAPI
[Repository Integration] as RI
[Course Generation Function] as CGF
[AI] as AI
}

database "Data Layer" as DL {
[Web Engine] as WE
[xAPI] as X
[Course Cloud Repository] as CCR
}

package "Product Layer" as PL {
["Learning Environment"] as LE 
}

package "Tools Layer" as TL {
[Learning Analytics Platform] as LAP
}

' Layout PL under CL
CL -[hidden]- PE
' Layout TL under DL
DL -[hidden]- TL
PE -down-> PL
CL-> PE
CCR -> RI
WE -> RI
CGF -> LE
LAP -> LAPI
X -> LAP
@enduml
```

## Component Diagram 4 based on the Internet of Things

This component model outlines the key system elements for the Internet of Things. At the Devices level, the Learner will utilise a device/series of devices including smartphones, tablets or personal computer to access the course via the internet. This activates the LMS Layer whereby components including data access, course pages and deployment options are provided back to the Learner device, through the internet. This interaction is reciprocal with the Devices layer where data and access is fed back to Learner devices upon request. Within the internal system of the LMS itself, the authoring tool and formatting support such as Tin Can will offer monitoring or modification options to the Instructor. The Learning Analytics Platform consists of the xAPI data storage and the Analytics processor to process the data for the Instructor.

The Component Diagram based on the Internet of Things aligns with:

The Use Case Model based on the Internet of Things found [*here*](https://www.plantuml.com/plantuml/img/ZPBFQiCm3CRlVWgnKtl82vGnMaeFWHqAwyv5YvNMp963fOoLiNUVcdHTj_vX5sDiVJzz-j1K5BDsJNGQD18y2y4SxQXJXZAjN8lLAsu8xafMoamAgORLDl16xW05lf_NgLuFp_01RlJK6BRT9gQn6wtm9PBQPKbP4cE4UMhQpeHZz-dS8w4HCXJ50vmAOT89oU_l0-hIrpdyKEL6xxDbEORxeclFMcYs0GMmqf1O_fOUszqkkzJwig9tsjksg61ccfs6Ic0PKItoneGraHVevUJ1eo84rkHA5irTfId_Xu9LHMBJ0xA7VGmzoRAuAIiYrNewKH3S-uS5RqAVr-3knzNLoaCqntOBVWivSKEypnCzjYfG9LiVrjwafpQcdK3GWUokQ0VmXRsRW0_IHZH6OZSbzhRNNm00)

![component diagram #4](https://www.plantuml.com/plantuml/img/VL91QiCm4Bph5KjElVW7fSJO10mfCTYtKCp6LX9HMMiakMq8-NjNKkhI7Eg3iMR6gvcHriwZzVEeXLTUIwYnVyUJT911PRoqHdgW8xHdPKuE2XedCj9uA1MUB8vYIdfObV93zT9rMxn8kuAh07xwHR-lfNLaKCSPCqz-0tHG5u-wPcG_qvbNKT3KZu8M3rhwIBRY9dfDy_3hzSeG24C3Mzg-DZz6zWNDreLud2t-MwJ1-n8zGjwpzOIN-HsNawRB6BRSJLwHkTExm2P9FlipMIu6MY8TwRnDr8RiYDu7hfcdYQpFe5K62ZHHjscYJWNRH-mbiDUkMbQiOA0IDn03-pkW2t4aMiCJkvnhl7ZLkwxMw8-yrH9peQ2s539HwZc_f_tAwmeY4hwugp_71jb0doPxMUeKIw_FYNfAllZ520l_yVGmEibV6x6MPk3xzWq0)

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
