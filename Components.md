# Components

Keep your components in this document, or create further documents of this kind if documents gets too long. Note that when you render the markdown in html you can get an url for any heading by pointing to the left of the heading and then right-click and copy the heading bookmark link. 

[Link to wiki page on component diagrams](https://github.sydney.edu.au/crli/EDPC5022-2019/wiki/Component-Diagrams) 

## Component diagram 1
This component diagrams shows the different layers of which the system architecture is composed of. 

![component diagram #1](https://www.plantuml.com/plantuml/img/JP71JiCm44Jl_WgBUty1jOev81aKARbL7BRnAhLmTgFrfb0X_XqxW9ARn_QR6Q-FMK5qcP8nVTI4jk5fPa9IwoAC0fCX3cWV6YOLJWd5UhYZF5Z8jl7sovmRNYIZTPZZI2XlvjmflEELKq39HNe4MG--_ymwb5iSCE-ikjNg5J5KegHb5OYaLRKOOEGn3f3i3AeeLBTVcAAomANKJZKYqcZp877MBQfdJlkS_hTouYKSBf0nM5Zqob9PBNUBx-bvmnqex6YtqWvdpZNwNXyNBmBhwlFKxiXME2o3xk1sXVr_qoUwHM6QogmhPSem3u4_wF1OXc6wJVNUz9jothXDjTwO8r8eF_W3)

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

This component diagram #2 shows the different layers of which the system architecture is composed of and is directly related to the use case scenario in Phase 1 of the project. 

![component diagram #2](https://www.plantuml.com/plantuml/img/LL9DJyCm3BtdLqJZl0i_06rgTvXKeD8gSPXsy1hJPQJsvBY32l7VISTWuVWSlu-yP14LH8S-6DDu3MWBxazCI6fB3vr0R-_k3R53EokOL3W455l1Y3Ap46rHsK-pBNYGYBR4w3j2sPdjHk4D3nmSIaomGf3hmHWL-tnrJL5bQ9KJ-BfwrOd61C57KC-K6TPuSRm8Ukhiy_w8hVepJZQFJ3xfJFCdH3UDQdJGSUTR2BO6LHJADc6VxlodjMd5d_IMec4ECVDkBjRBTUA_uDvk4gyzs1Lrdd2NPLgcvAFwDgKDeAyi_Ksp18LCilpfB_3WKYSdZbEgCObzBEjrreUmInNbFVolOKLdBqnzUhc9PTAxp1s_q_nXQinChVtYfZBD3PMLARFTofW5aai_uXi0)

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
[Cloud Depository]
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



## Component diagram 3

This component diagram shows components of the Learning Analytics Platform.

![component diagram #3](http://www.plantuml.com/plantuml/png/JP31Qjmm443lynM3xzxUImbnRLCMV30u9OVGmrGxyOhA8pCQjrv2_xso29lgDdhFrcCUav7QjWGmRu6nZSiQXSKIrXy3TfvcfGLW9VUBPiPgO5BnCcCZ56xcNS8naBr6NIgaX4C_uXk22t6xO7KMOyqYkYZ6OaN9b_W6cCzBMxIErvYyHRtzE7WxT51eSyufcoR6Rooib8qYDEUsWxy0yFBCFt5YKdV5NcOlNFZprCF1lyPDBgItZ-fi_VOQPIaj9VT_RMHDCUVwHEQZlF-pY6CMeOrY6WDMUpEUo_KE-JGkbs4rtPBnWXqdFmjhuLDtnwM1zTCJaxk-u-4908wLrPVuH-g7uvcnlqz3N-2NEl2hrRWZmjJTQTuJViQ5X6PEC3nXhNw-Mldk64-dRJsT7d3FLXj3O6VV4sk_hwoUnN57Hl38SjcMy0y0)

```
@startuml
title Components - Component Diagram

package "Learning Analytics Platform" as LEP { 
cloud "Internal content" as Int {
    [Cloud Depository] as CLD
    [AI Course Generator] as AICD
}


[Web Search Engine] as WSE

}

Boundary "Learning Environment" as LE

Boundary "Personalisation Engine" as PE


Control "xAPI" as x



Actor "System Designer" as SD

Actor "Learner/Teacher" as LT


LEP -down-> PE
PE -down-> LE
LEP <-left- x  
SD -down-> CLD : manages
LT -right-> LE
LT ..up..> x : CollectUserExperienceData
@enduml
```


## Component diagram 4

This diagram represents the components of the Personalisation Engine.

![Component diagram #4](https://www.plantuml.com/plantuml/img/RP11QyCm38Nl_XKYz_w5KPhqPgYXkPKTj4GptXofoCh66Fllirie6UmezDxJzxGlXchhafqbomI1j0XZJWKj2SEHOsA2NfQhCB71a30gBkwAqpj6Wkv_HmTO81pXsrqyeNBY2AUNDveiVL21KIG_Dua_ZUuIQCOeCKsO8Q0PAMya8LJ9cGmEilACchR-ys5qFsv3epAlau77Bz8xX6yGtOCYPBHNqQMxtm_mnzyBcqhEf9k8_XRHbgiMWe5AYbntjuH-Q05LiflbatTFjRMhnH-JTtlYkNtO_G80)

```
@startuml
title Personalisation Engine Component Diagram
package "Personalisation Engine" as PE {
[Learning Objectives Tool] as LOT
[Pedagogical Patterns Tool] as PPT
[Set Boundaries Tool] as SBT
}

package "Product Layer" as PL {
["Learning Platform"] as LP 
}

package "Controller Layer" as CL {
[ "Course Designer"] as CD
}

CL -down-> PE
PE -down-> PL
@enduml



```
