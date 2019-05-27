# Use Scenarios and Use Cases

> This page contains the meta-design use scenerio, followed by use cases that extrapolate key aspects of the Learning Design (LD) system proposed. It offers a clear break down of the users involved and aspects of the system that are at the core of this proposed adaptive learning design system.

## AI Adaptive LD System Use Scenario Model

The adaptive course design system offers automated and authoring tools for the designer to adapt the design to the needs of the users. The System Designer will contribute to the Courses/Environments Cloud Depository and provides technical support to the Learning Environment. The Course Designer will use the Personalisation Engine user interface to input requirements such as learning objectives, pedagogical patterns, monitoring needs, learning platform, duration and/or activities. The Personalisation Engine will search for information through the Courses/Environments Cloud Depository and web. The Personalisation Engine will then feed back to the Course Designer and generate a Learning Environment appropriate to the boundaries set. The Course Designer will review and approve or modify the Learning Environment produced. The Instructor and and Learner will engage with the Learning Environment, where the xAPI will collect user experience data and feed back to the Learning Analytics Platform which feeds back into the Courses/Environments Cloud Depository and Personalisation Engine. The Instructor is able to access the Learning Analytics Platform to make teaching and learning decisions. To reflect the democratic process of learning design, the System Designer, Instructor and Learner are able to contribute to the Courses/Environments Cloud Repository.

![Submit Rule](https://www.plantuml.com/plantuml/img/ZLDBIyD04BxlhvYZFHJlHSHGFHGKYY8UosPtZ0l9J9YPL8lutzqq1LzfpMbX-LxxpUoLcXVhcjevIrOZ52ieecyjRH5kh-5XfuODF2h2Gq3oaXZkE6Bj18DvglQKpG7s3kviZQ9ClaxgBJ713LM9S0ONyyYlDB-4ioSiPoU1ageNwv5BxaHHpszecuIfGJA5PSrTX7jiMPEnx4vfpNkLM_H2YIhu9ZDpNzT59kui1OLrxUsPfJaGZwYwSSM1yrQiLtsYuVpfFsRqNuwkdLw4-t3383RNgAaYb270n1eNWSaabPsXWZ6CYus_VT4ARrFiYHXUGBksPJ5mW_KlYMFJMYZcO2Lt5FEYPIst8ZNfGivtqZplOzvNKV0KeM7g7wH_o5Dh01zZNy1nzx59PLe8gDd0xN7_z9N8K7om8NFWklObYxVVzAcXaIfVvSeIWNDNI37_wKy0)

```
@startuml

title AI Adaptive LD System Use Scenario Model
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

## Personalisation Engine Use Case Model
As Learning Design research shows that the context of learning and the need for systems to be flexible, adaptive and user friendly, the Course Designer will input boundaries or design requirements into the Personalisation Engine.
The Course designr can engage with the Personalisation user interface to determine one or all of the followingg criterias: learning objectives, monitoring needs, pedagogical patterns and learning platform. Based on the set of boundaries and requirements set, the Personalisation Engine will then generate a learning course and environment appropriate to the learning context for the Course Designer to review.

![Submit Rule](https://www.plantuml.com/plantuml/img/XT51IyD040NW-_wAEIQ7DdSFqf1u49fsYUYrhCcu7KbcP7TI1F6_kv5MX0QzxEaRtdli9geBEes3CKew85WCKTWD59sICDon9qPuZ0YLIqyZFIOSi5F7_lhWS3xu09DjqGKczh1_VasUJXXpMArk8Qk45LbpapN2f19cjKFiB-2zjFT5Ex7IY4bPx9qNJvqRm3fL37oHzHI-W_zMvHnFIXZXgItADl_LpWvENoICPxfj7eeQJzIbjiPy6bF9528UQepa6GEirxDQsdRJ7KLYob01uhT9bs-lDY-pnJd_jFdPOim6kKyV-mK0)

```
@startuml

title Personalisation Engine Use Case Model

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

# Adaptive LD with Design Critique Integrated Use Case Model

In a Learning Design with integrated Design Critique process, the Course Designer engages with th Personalisation Engine user interface. Additionally, the Personalisation Engine will generate a Learning Environment and the various stakeholders and designers will engage in a design critique based on the Proposed Learning Environment. If approved, it will then be deployed as a Learning Environment for the Instructor and Learners to engage in. If not approved, adjustments will be made by the Course Designer using the Personalisation Engine and re-proposed for critique until approved.

![Submit Rule](https://www.plantuml.com/plantuml/img/ZLD1Ri8m4Bpx5Nia1pw0gWgKz10fI95GrIDoawtPAbcdzeOgelrxdK0fq22uH8vtTcOyQy-zQ2TjNIab91N2ejIDq1OXI-2JP0C9UZ8CiIEXZnOXPK7Zj609pnuXrk6pj2K6XbNd1UlrlWCTQ0-hHCMsTHxFTkD4fUp5jONOOIDL6Mftg6QXfQvR9kdiM-vq8LJWq9OhvR0GpQPtcgxtWh03fIOvEczPL-Ira6LuOaEC4JnCfuymYIlRbk4iZVKKDBi8RdMyu6jq7JD0ScS3NmXYC4ziGdbBpdADB47X-zJk8OP5qpYxrHNirEGYsbxPaTb8pxqetrilFP4FDax_u0Hq88jwgLjs1ikNaYCcfkVCVyjVXgQotRX6k099G7sD2C4CsMY37eZtgB6fgFYk_YFgB9TnnD7zlt8_mIlZdHKR6wBqAixlyPFU2nezStQjeER8PNYRFm00)

```
@startuml

title Adaptive LD with Design Critique Integrated Use Case Model

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

## Design Critique Use Case Model

Users include the presenter, facilitator, note-taker and community of practice. The critique Presenter role is assumed by the Course Designer who has the most in depth and context specific knowledge of the model. The critique Facilitator role is assumed by the System Designer who establishes the key goals to assess the design against. The crtitique note-taker can be the Instructor or another participant at the critique. The Community of Practice includes developers, other product managers, stakeholders, pilot students, learning experts and any independent stakeholders invited.

Use case involves the Facilitator setting an agenda, location, goals to critique against, models to be presented, invite critiquers and key roles. The Facilitator also estalishes critique Goals which are the goals established by numerous stakeholders of the business and design process, learning goals, UX and/or UI design goals. Learning critique sessions will involves a discussion that looks at use case scenarios, clarifying questions, avoiding using absolutes and design alternatives. This is different to problem-solving and separate to that of a brainstorm or giving general feedback. Post-meeting actions include presenting feedback notes to keep everyone in the loop and publishing actionable tasks for follow up.

![Submit Rule](https://www.plantuml.com/plantuml/img/XPDDRy8m38Rl-HKvmW5nvp1H5J5LsWSJGzeDXTIKY92ms6L2q_xx77NjMjPgbofr7jlnQtkEf0AL9oi46R8W5u2cS38DXinx2NA385F5dqUV0rC1D2bNDEIs8J_5QAcqiOOKmLXEWYaEDBcJeuQuzyhYMDmQMkZ2e2uHZNUCjNvQoCeZoKGJcsEiJihSVxZ8F7Yj8Z1zzTuEKgi028uWJ3DtYPVH8od0vQhlaRNRcjGH3jxc48OhQbu2AZZZYl_9pTjqazNortH7WffChGfcVurHNqh0MebUDh5Sd-FIBZ3CNBp9PR93RqiQnk8ah3KuJkuZr6d4BxO4o7TA7-MJhu8DS9L5xNYICe8Jarz2hA_8vssb0kix-TlnNgJTtvaqZZNcCyeJ0B5E8lLbGBXnkct5x5mD1Bl5MKUHEQHGQl8_3crPPcVU6wFDEUOHptI0qAn2m1vUTXp4dCUCr-uR)

```
@startuml

title Design Critique Use Case Model

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

## Use Case Model for the Internet of Things

This Use Case Model attempts to show the interactions that occur between the learner and the learning environment when they use different mobile devices. The Learning Environment is dislayed in the learner's mobile devices screens. The xAPI tracks the learner's actions as they interact with different devices such as their Smartphone, their Tablet and/or their Personal Computer. The xAPI then feeds all the tracked data into the Learning Analytics Platform. The Learning Analytics Platform feeds the tracked data to the Personalisation Engine. The Personalisation Engine adapts course content based on the information gathered by the Learning Analytics Platform and deploys it into the Learning Environment. The Instructor accesses the Learning Analytics Platform to monitor the learner's behaviour within the mobile devices. 

This model is not linked to any other models.


![Use Case Model for IoT](https://www.plantuml.com/plantuml/img/ZPBFQiCm3CRlVWgnKtl82vGnMaeFWHqAwyv5YvNMp963fOoLiNUVcdHTj_vX5sDiVJzz-j1K5BDsJNGQD18y2y4SxQXJXZAjN8lLAsu8xafMoamAgORLDl16xW05lf_NgLuFp_01RlJK6BRT9gQn6wtm9PBQPKbP4cE4UMhQpeHZz-dS8w4HCXJ50vmAOT89oU_l0-hIrpdyKEL6xxDbEORxeclFMcYs0GMmqf1O_fOUszqkkzJwig9tsjksg61ccfs6Ic0PKItoneGraHVevUJ1eo84rkHA5irTfId_Xu9LHMBJ0xA7VGmzoRAuAIiYrNewKH3S-uS5RqAVr-3knzNLoaCqntOBVWivSKEypnCzjYfG9LiVrjwafpQcdK3GWUokQ0VmXRsRW0_IHZH6OZSbzhRNNm00)

```
@startuml
title Use Case for IoT
package "Internet of Things" as Internet_of_Things { 
(Smartphone)
(Tablet)
(Personal Computer)
}

Learner --> (Smartphone) :uses
Learner --> (Tablet) :uses
Learner --> (Personal Computer) :uses

(xAPI) <-up-> (Smartphone) :tracks actions
(xAPI) <-up-> (Tablet) :tracks actions
(xAPI) <-up-> (Personal Computer) :tracks actions
(xAPI) --> (Learning Analytics Platform) :feeds tracked data into
Instructor --> (Learning Analytics Platform) :accesses and uses data

(Learning Analytics Platform) -left-> (Personalisation Engine) :feeds data into
(Personalisation Engine) -up-> (Learning Environment) :adapts content and deploys it into

(Learning Environment) -up-> Internet_of_Things : displays on
@enduml

```

## Course Design with Smart Functonality Use Case Model

This is a proposed use case for an automated course generation platform that is activated by the Learner rather than a Course Designer. It relies predominantly on AI to create content and to make adjustements as it learns from user behaviour. The Learner enters the Learning Environment interface and inputs constraints such as duration, requirements, interests etc into the Personalisation Engine (with AI) to generate a bespoke course. The Personalisation Engine gathers data from the Web and the Course Cloud Repository, which is constantly updated and reviewed by a Course Designer and a Community of Practice. The Learner actions the course and the user experience is logged by xAPI, the data is stored in a learning record store on the Learning Analytics Platform which is analysed by the AI in the Personalisation Engine. The Personalisation Engine then updates the course based on the Learners needs.

![Use Case Diagram for Course Design with Smart Functonality](https://www.plantuml.com/plantuml/img/XPB1QiCm38RlUWeTwqFUO9IMf8D1e6Oxx1YyLCqCiLniULiOU_SvIGEx93lPwF_a_xViGnGJ9BaUGApqXALF8H9M56t7-6db7LzSHl0nSIkUJMzb09YnPiOee8bOLhdgNE8CDETheuDfnROqQMSDDPbmHsk0GAqOxhBZLBVSDIV-iC6p8nRyHjXf2d4oZ4QiPpnnPvbKLcPt1Jy0TL7iSGszgmiEEGREbTwd2pxJpKShFWmAocfDMG-orl1FnokzgOth_KsyR8hzxkkedzHcrqXayt6P3ba6YyVC3_af8khUoDK7D_floWzRKuK3yIN_cLy0)

```
@startuml

title Course Design with Smart Functonality

Course_Designer as CD
Community_Of_Practice as COP
Learner as L

rectangle Learning_Environment { 
(Personalisation Engine) 
(Course)
}

L--> (Personalisation Engine)
L--> (Course)

COP --> (Cloud Repository)
CD --> (Cloud Repository)

(Personalisation Engine) --> (Cloud Repository)


(Personalisation Engine) --> (Web) 
(Personalisation Engine) -> (Course)
(Course)->(xAPI)
(Personalisation Engine) -> xAPI


xAPI -> (Learning Analytics Platform) 
(Learning Analytics Platform) <-> (Personalisation Engine)

@enduml
```
