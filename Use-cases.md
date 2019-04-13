# Use Cases

> Keep your use cases in this document, or create further documents of this kind if documents gets too long. Note that when you render the markdown in html you can get an url for any heading by pointing to the left of the heading and then right-click and copy the heading bookmark link. 

> [Link to wiki page on use cases](https://github.sydney.edu.au/crli/EDPC5022-2019/wiki/Use-case-Diagrams) 


## Use Case 1

The proposed next-generation LDE involves:
- Cloud based courses and environments depository managed by the system designer. This is constantly updated and managed with technical support for the course designer and student.
- The course designer can use two functions: 
(a) A predictive/adaptive analytics engine to automate the selection of the learning system, platform used, collaboration and teaching tools, learning content and duration. The AI system will use the user’s context (setting, audience, etc), previous behaviours and previous courses to analyse and select from the database to build the best suited model; or 
(b) A personalisation engine to set one or more boundaries to filter from the courses/environments depository.
- The system will then generate the bespoke learning environment that students will interact with.
- CoachU: Through the tracking and monitoring of student interaction with the LE and progression throughout the course, the adaptive system will build further predictive models of best course pathways, especially for students at risk of completing the course successfully, if they are on track with course expectations, or if they need to study more or require additional instructional and/ or institutional support. The course designer will play a managing role rather than design.


![Submit Rule](https://www.plantuml.com/plantuml/img/jP8nJmCn38Nt_0gFxL2ntu1QjHsGEY0XvifDJB2KE5NiAvmG_vsKemXGGJ2GBR7pFRydpzMmMf-JSyQM21O1zyO7WiqARWOroiwvIjvGuh5yjHrVuSb1EvDhgbe44oiQ5u6rH1QQmcns2PDbwQkINgpbmBL89Z65PIfzW1NjYxALEan7qBlmej46Ow__mHhhlsEDkXl2AYmHFZI_OSwMJjEYlx-T7jlSitDZPjiLAKUX-XT7q6KKZEJ6zY-Cx-Blb0nsfPU0bKdFV_uXyWumfV80s5l9Q1JWBj4ZxpYn3UxL-8boFeMEnQYYRvPG0lYI4kvARIY50oDirfyffy0wajZSAh2qPGFjOxiSzVsO5bY1JCqSUWoKsOCG1MrBEYS9RP5V0000)


```
@startuml

title Adaptive LD System


rectangle AI_System {
    (Personalisation Engine) --> (Courses/Environments Cloud Depository)
    (Adaptive Analytics Engine) --> (Courses/Environments Cloud Depository)
    (Adaptive Analytics Engine)
    (Courses/Environments Cloud Depository) --> (Learning Environment)
    (Learning Environment) --> (CoachU)    
}

System_Designer --> (Courses/Environments Cloud Depository) :manage
Course_Designer --> (Personalisation Engine) :set boundaries
Course_Designer --> (Adaptive Analytics Engine) : allow automated flexibility
Learner --> (Learning Environment) :interacts and collaborates via LE
Learner --> (CoachU) :engages in AI suggested courses to meet academic needs


@enduml
```

## Use Case 2


(...)

## Use Case n
