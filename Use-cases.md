# Use Cases

> Keep your use cases in this document, or create further documents of this kind if documents gets too long. Note that when you render the markdown in html you can get an url for any heading by pointing to the left of the heading and then right-click and copy the heading bookmark link. 

> [Link to wiki page on use cases](https://github.sydney.edu.au/crli/EDPC5022-2019/wiki/Use-case-Diagrams) 


## Use Case 1 - Automated Course Design Model

The automated course design system is pitched at the metadesign level where the instructor also assumes the roles of course designer.
The top-down use case is as follows:
- System designer will manage and maintain the overall system, especially the automated course design engine which collects data from xAPI learner and instructor experiences. The System Designer also adds to and builds on the cloud depository.
- The Course designer will activate the automated course design engine and approve, set limitations or personalise the automated designs prior to delivering it to learners.
- Once the Automated design engine is activated, it will search through the depository to generate a learning environment appropriate to use needs (monitored by the Course designer)
- Once the Learning environment is deployed, the Learner and Course designers will engage with the LE. The xAPI engine will collect, filter and feed the experience data back into the Automated course design engine. The Automated course design engine will use the xAPI data to automate supplementary courses for the Learner which the Course designer will authorise or refine. 
- The Learner may wish to engage with the suggested supplementary courses or choose to ignore. Any additional Learner interaction will add to the xAPI data collection and improve the specificity of the Automated course design engine for the user (personalisation).

![Submit Rule](https://www.plantuml.com/plantuml/img/bLBBQWCn3BpxAtJCGfFSzr0IaXm2EHJo0K5T2sEmvSNIXeRIVwytJX-7q6rEnj9eD3De9OfPXnYCKQ-1O3reYgXauR25uqMKeZ4cKwV8RkplJxKAxsRs0zwa8Gl1biGxXXqxpzJ0VFuCizgIvOxFFYUEn2gm2Mcm1TudyPhofPaaC_yagaiFX9azE_W5BXHtotNYRVsoRy3StcjfKj6K_yMYi1o7lWyqRi9ykG6bCH_6r21FTOZo8t51YzQ2fliSKxfQYCZeoDJsezCnyQZY2R3lSpeJ8DjboY2a47pqYkeJYxcc_SLwF_hMirB6hdWi9D2b4F0rvR9TuEmH3hjlbZ_2X9RO5Jy2dik5WWokV4O7NKMKf21IaOSTMeg-0oQoKYvxHMp7y_y4)

```
@startuml

title Automated LD System


rectangle AI_System {
(Automated Course Design Engine) --> (Courses/Environments Cloud Depository)
(Automated Course Design Engine)
(Courses/Environments Cloud Depository) --> (Learning Environment)
(Learning Environment) --> (xAPI) 
(xAPI) --> (Automated Course Design Engine)
(Automated Course Design Engine) ..> (Supplementary Courses)
}

System_Designer --> (Courses/Environments Cloud Depository) :add to
System_Designer --> (Automated Course Design Engine) : manage
Course_Designer --> (Automated Course Design Engine) :monitor, approve and/or set limitations
Learner --> (Learning Environment) :interacts and collaborates via LE
Learner ..> (Supplementary Courses) :engages in AI suggested courses to meet academic needs


@enduml
```

## Use Case 2 - Adaptive Course Design System

The adaptive course design system offers automated and authoring tools for the designer to adapt the design to the needs of the users.
- The System designer will manage and add to the cloud depository and both Personalisation and Learning analytics engines. Also offers technical support and administrate.
- The adaptive course design system offers Course designers of using a Personalisation engine or a Learning analytics platform.
- If using the Personalisation engine, the Course designer will input all necessary data including desired LMS platform, duration, pedagogical preferences and/or activities.
- The Personalisation engine will feed the information through the cloud depository and generate a Learning environment appropriate to the boundaries set.
- The Instructor and and Learner will engage with the Learnign environment, where the xAPI will collect use experience data and feed back to the Learning analytics platform.
- If using the Learning analytics engine, the Course designer will activate it and it will use either the Cloud depository/web search engine or both to then generate a suggested Learning environment.

![Submit Rule](https://www.plantuml.com/plantuml/img/hLCxJyD03DxlLtXi1s3FWAXeXqeTAdLWhDoS2POINtHsAYh4VyTDU5LA2qXCbtDyt-C-tvqQPkkQEWHZgmbc4LlZFS5g3fk36ZKXX4obeLJ7tyljK8MNC5bJrYHOiw9n4bX8nK9JkBgwXSbzwhAItYnappb9Gs8AztNg8iofJSgMyc4Q9Yl2B2mLp1pfO5mgh6kqnvIRALnVEz83xM3ZNUNJ1qCOgGszdsZVQ7z5yYzoU-Dd9FoEu2B4Q7auyJnRBwSGtjTJa36buJM48SZjd9GheVoNsA30sB2mMaQZSQHnjKMRqvuZWP5dfrtRfcnXOFq2w2CvDrw5ai4kTH8nC-duuOlk2r2gVQOLiBFKk8Neamrb3mGLEGgwpx0KDzYL_dafbxxwWsiMSyoUKQ8JrJNkql7k5FQCi5gSeWmn5YGLLjx2SfIdNUMRezP1g88bQCWl0qkCr709GXJL7-mTIUmVzHi0)

@startuml

title Adaptive LD System


rectangle AI_System {
(Personalisation Engine) --> (Courses/Environments Cloud Depository)
(Learning Analytics Platform) ..> (Web Search Engine)
(Web Search Engine) ..> (Learning Environment)
(Learning Analytics Platform) ..> (Courses/Environments Cloud Depository)
(Learning Analytics Platform) --> (Learning Environment)
(Courses/Environments Cloud Depository) --> (Learning Environment)
(Learning Environment) --> (xAPI) 
(xAPI) --> (Learning Analytics Platform) 
}

System_Designer --> (Courses/Environments Cloud Depository) :administrate
System_Designer --> (Learning Environment) :provide tech support
Course_Designer ..> (Personalisation Engine) :set boundaries
Course_Designer ..> (Learning Analytics Platform) : selects automated AI course generator
Instructor --> (Learning Environment)
Learner --> (Learning Environment) :interacts and collaborates via LE
Learner --> (xAPI) :engages in AI suggested courses to meet academic needs


@enduml

## Use Case 3 - Authoring Course Design System

The stakeholders will define the learning objectives, communicate learning constraints and monitor the needs of the learner.
The course designer will select pedagogical patterns, configurate the learning design and take into account the established learning constraints. The Course designer will feed this information and make choices within the cloud-based authoring tool to design the Learning Environment and administrate the learning experience.
The System designer will manage the authoring tool and learning environment.

![Submit Rule](https://www.plantuml.com/plantuml/img/ZPFFRi8m3CRlVGeVuS0Bv30niTqsQH8FCBc9ATbIkqeS9Dv-wH_G15r7Ratz-sn_ZhT9CMfkGrMfrq3md5LQL79W9ST4u2ZvXk6GsQeNnk3r35K5vQpU22DxRa3gBog_JvJMiDaymUg373RIU8i1EbIbo6azGk_2NYNs61Ev2p5TOrsAkEhkRVITJk2ivgFmzNRgnmedZUXP7zTOYXWrTa6oszIOYd-OzJYsgI9XabW861Mkkgzyyb6u9TQrALLtGSwf5wdsYjzqbE0etZ2_ns0S7JnJkW-_7u3nx8gjEXUzQ9onqhQP9tOtl9ZFbo7mmizFpIGAfTIIxvoKsXjcoINJ8cD3Vv2pze612pHRudABlI49oeS0sh8KhFCgCxRsIWVVv3ZOCwJvfz2IXY8MOm2vNy4Gi9OHhxR4hj_K7m00)

@startuml

title Automated course design functionality 

    (Learning objectives) --> (Pedagogical patterns)
    (Monitoring needs) --> (Monitorable Learning Script)
    (Pedagogical patterns) --> (Monitorable Learning Script)
    (Learning design constraints) --> (Monitorable Learning Script)
    (Monitorable Learning Script) --> (Cloud-based authoring tool)
    (Cloud-based authoring tool) --> (Learning Environment): deploys
   
Stakeholder --> (Learning objectives) :defines
Stakeholder --> (Monitoring needs) :indicates
Stakeholder --> (Learning design constraints) :communicates
Course_Designer --> (Pedagogical patterns) :selects
System_Designer --> (Cloud-based authoring tool) :manages
System_Designer --> (Learning Environment) : manages
Course_Designer --> (Learning design constraints) :takes into account
Course_Designer --> (Monitoring needs) : configurates
Learner --> (Learning Environment) :interacts and collaborates

@enduml
```
