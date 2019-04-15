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

Hey Qang - unsure if this is considered interaction or use case but I guess we will find out on tuesday if you no one else can shed any light. Enjoy!


User decides on key learning objectives of course she/he wishes to automate 



User logs in to system 



AI is analysing decisions made my user 





User accesses search content function within system that links and has subscriptions to services like google, google scholar, educational databases, YouTube



User enters key Bolean phrases representing the exact terms of her/his search, separating terms with the word AND. The more search terms, the more focused the course question.



User can add limitations or more specific options such as researchers, theories and methodologies to focus on Or specific content to link to. However, this is not necessary as system is programmed to produce balanced, well researched content across all multimedia types.



User selects the automate search button. 



System produces a course based on user’s search terms.



User has capability to edit, remove and add content from outside sources As well as via returning to the search function to look up specific content within the system by drag and drop 



AI records users decisions for future uses, providing search suggestions and system function recommendations for creating a more efficient process 





End 

## Use Case 3

https://www.plantuml.com/plantuml/img/ZLD1RiCW4Bpp2ex98H_meKgLzjPAbVA0QWrhXnRlMh14okyBjXD5jME56p0pkpCB-oWG97LUAN7YKRycuGu4hJQSGaHjCRgMT9F8Y6C2x-IYbL8whyq7GY17hURw1_Fz6UDMxtOlUlE55bfkdG6lUn31G74xaZwPd70eD4AqLyPq37NkugPxDC7rCX4NDPybtqudGuOfIW17yhp66cBKE7XETbT3p052ajDeKvZz9B4261LkkkzqTe6fGv9jbRlkFLzY4L7gAF2B9_OMmp_I_HmgYuqZZ7FuV0AL8vjpbINqQdALuQvBD74FmvlvVXk0L_xosAg8FhVwWBCMKzK1GVkesdgtnLlKUSCQJ7xX9Cig2maLfSQrAGnEXpApclSpAvbchv0zQg3odxo7caUwKdiaM_xT7m00


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
Course_Designer --> (Cloud-based authoring tool) :manages
Course_Designer --> (Learning design constraints) :takes into account
Course_Designer --> (Monitoring needs) : configurates
Learner --> (Learning Environment) :interacts and collaborates


@enduml


