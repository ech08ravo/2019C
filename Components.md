# Components

Keep your components in this document, or create further documents of this kind if documents gets too long. Note that when you render the markdown in html you can get an url for any heading by pointing to the left of the heading and then right-click and copy the heading bookmark link. 

[Link to wiki page on component diagrams](https://github.sydney.edu.au/crli/EDPC5022-2019/wiki/Component-Diagrams) 

## Component Diagram 1
This component diagrams shows the different layers of which the system architecture is composed of. 

![component diagram #1](https://www.plantuml.com/plantuml/img/dPF1QiCm38RlVWhJU_e8eoNPOP2DiEHMTb1haPevLf2LRcNitMUd7KbPAMMt_94__V9lUnK4M8REATLOSQXpwdhow4KN5bg6Jdaog1SvUM5o3bcNS4HUQ0WwB_MNskGqS41TOB2jHtvJcrhW7VVa37A8iaJWiV1zRbOZ7-mEmwnLFRPwGJI9Y6v16AoNf2eqq59hT-1q3oB8Flr-9c-56BPnR9Sih6zrsB7jPR9gYDpSfpcDx6WmsHO26Ws3x8aJAt5jxBj-cl0216PqCTAls5D8riUqERjb6By-rzMCh9ZCi9CPN8rm-JlfepzO9j_5h1Fr9qQzN2xrB95hrSkShg_vHthdvhT2kb4yqTVtUPFBsBPx6UcBYEzaffEu4pWTc8gtE3FquRE7U0jLFQccLCsaYb8LawfAfLReJNmwFm00)

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
[Repository]
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
[Cloud-based authoring tool] -right... [Repository]
[Cloud-based authoring tool] -right... [Library]
[Cloud-based authoring tool] -right... [xAPI]

CL -down-> SL
SL -down-> TL
TL -down-> DL
DL -down-> PL

@enduml
```

## Component Diagram 2

This component diagram #2 shows the different layers of which the system architecture is composed of and is directly related to the use case scenario in Phase 1 of the project. 

![component diagram #2](https://www.plantuml.com/plantuml/img/LL9DJyCm3BtdLqJZl0i_06rgTvXKe6ALE4mxU8tf0gazEUwWGlntqZ5OE3x7xoClMKG5qQ4FnZHU0zg2-oCJajhIGoVGsvjRG-pGpWec5Gu1nLOmeimiH5jKzjDi2nuaeYqn-evGTcQxKNZ30mU74XEi4EHoC4R5FbzTKrGPMkK4lYvUTQ8nGV0Hr3DbXZMU7S-2dZhxk7_5Llq99vjx9fzqfla3efj6DJhekFCj15k3AWfbcx1FT_xJshJYZtfDqJ27c7atP-lbEl6VSMytYTSUx8ewJxZBCYrJyb5zcz86q1UM_gfPWa8cMVxq5tXmzWcF7ATKOnBxMDRhh0zXbohAU_XVmufENfZwz78JowHtcJj-f_dTr9YPMll5JMMQAoehKsQxbJ4B99T-n3S0)

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



## Component Diagram 3

This component diagram shows components of the Learning Analytics Platform. The Learning Analytics Platform is an automated authoring engine that collects and filters interaction data from the Instructor and Learner. The Instructor and Learner will engage with the Learning Environment, where the xAPI will collect user experience data and feed back to the Learning Analytics Platform. The Learning Analytics Platform feeds to the Personalisation Engine, which feeds to the Learning Environment.
The System designer manages and adds to the Cloud Repository and Learning Analytics Platform.


![component diagram #3](https://www.plantuml.com/plantuml/img/JPB1ReCm38RlUGgBE-nUJLKPe0c90nfCFLGxPAbBemK79M43LNlt6TPrvPJu-nq-77O-I1V6teYWWq78R3zOGWeUulyDv5fsJlP2359zo0uXgb0wqjH1IjBCGIiFjP7XP5qVWVHG5JLSG2XZnoD49GLq70HbUKLXZN0HBWBuEMHhx0K7wtMmRdvRU5RblpGjMMLq7k4P2Ptan1f8oomNtqA8mnxVeM4ZTOQ2EasuydrJY8K_sP6EqirtrWLzQcUf_tEfYljOZSvRrjLU1ctfUkOQh3aeCluAPmr4KrgNQtdYgaWLcq7Kp3vW3pbwtR7koflyXbS7T0yjIdM-ughbzcLayT5-KRnTNbCNjntRBV0nDdWACKm0eiblbES46-WbySLuKRKGEzsTmxMlXIGPXoJPSjk6vsWCgl3gqHNJW4uZASnba6A7TEJ_u0S0)

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
