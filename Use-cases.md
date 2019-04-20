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


![Submit Rule](https://www.plantuml.com/plantuml/img/jLJ1Ri8m3BtdAto40zgTmmGQErJgBl01AAGUYvGcB7QOqBH_dzC2Mmj3Y6szD8djvsS_9nDY7JdLJYcsx12cYKEj6IiePx3O4MEjb8feMFjrjXVBzXJU5SWtcEFMuXk1zjhjs1eQmcXq3uE7a28XpD64kaPVQRR1mqgJGCl2e_oR6B8qx48Hfmezmsj2ob4Pl8AP9PE86fIWOtLxdlyEQOaTgZ4fnboDQI5oSwFLZi1wg70Jo7A8kzlp55u0FJ949DJHl6J7Vh8XT5jy9QbzYoEsFCAps8bZCiqsg-8afRT-_GqY7slns5gsU6ZWbIp_BD_lC4vvxAdAfdnQm1sKZsSIdN4wpC9UJv6lIh4NS1p_YqwTSPyXsRN72DFD9eQjTjtvEJLteejwur0oSPEZ6zgpTMVvwvAh3wMcnO_MlkdAAwrQ4iiZ_yirmrWtIspGIAPh5P9ScYWQgZAht8Fe5pUsUIn5-9QF2SxfLP3M8y7MQX5G7Zyr4KtaYVm4)


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

![Submit Rule](https://www.plantuml.com/plantuml/img/ZLD1RiCW4Bpp2ex98H_meKgLzjPAbVA0QWrhXnRlMh14okyBjXD5jME56p0pkpCB-oWG97LUAN7YKRycuGu4hJQSGaHjCRgMT9F8Y6C2x-IYbL8whyq7GY17hURw1_Fz6UDMxtOlUlE55bfkdG6lUn31G74xaZwPd70eD4AqLyPq37NkugPxDC7rCX4NDPybtqudGuOfIW17yhp66cBKE7XETbT3p052ajDeKvZz9B4261LkkkzqTe6fGv9jbRlkFLzY4L7gAF2B9_OMmp_I_HmgYuqZZ7FuV0AL8vjpbINqQdALuQvBD74FmvlvVXk0L_xosAg8FhVwWBCMKzK1GVkesdgtnLlKUSCQJ7xX9Cig2maLfSQrAGnEXpApclSpAvbchv0zQg3odxo7caUwKdiaM_xT7m00)


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


## Use Case 4 - Futuristic Case
In this case, the AI creates the entire course starting with needs assessment conducted from analytics and prior students.  Then the AI gathers and creates teaching and learning activities, sets up and designs the course in the Learning Environment / LMS.  The human course designer only approves the course and makes changes before the course goes live.

![Submit Rule](https://www.plantuml.com/plantuml/img/jLJ1Ri8m3BtdAto40zgTmmGQErJgBl01AAGUYvGcB7QOqBH_dzC2Mmj3Y6szD8djvsS_9nDY7JdLJYcsx12cYKEj6IiePx3O4MEjb8feMFjrjXVBzXJU5SWtcEFMuXk1zjhjs1eQmcXq3uE7a28XpD64kaPVQRR1mqgJGCl2e_oR6B8qx48Hfmezmsj2ob4Pl8AP9PE86fIWOtLxdlyEQOaTgZ4fnboDQI5oSwFLZi1wg70Jo7A8kzlp55u0FJ949DJHl6J7Vh8XT5jy9QbzYoEsFCAps8bZCiqsg-8afRT-_GqY7slns5gsU6ZWbIp_BD_lC4vvxAdAfdnQm1sKZsSIdN4wpC9UJv6lIh4NS1p_YqwTSPyXsRN72DFD9eQjTjtvEJLteejwur0oSPEZ6zgpTMVvwvAh3wMcnO_MlkdAAwrQ4iiZ_yirmrWtIspGIAPh5P9ScYWQgZAht8Fe5pUsUIn5-9QF2SxfLP3M8y7MQX5G7Zyr4KtaYVm4)

```
@startuml

title Automated LD System


rectangle AI_System {
    (Reviews analytics) --> (Course Recommendation based on need analysis)
    (Reviews student questions and Discussion board) --> (Course Recommendation based on need analysis)
    (Course Recommendation based on need analysis)
    (Course Recommendation based on need analysis) --> (Reviews current course materials in depository)
    (Course Recommendation based on need analysis) --> (Internet research on course materials) 
    (Reviews current course materials in depository) --> (Creation of instruction and learning materials and activities)
    (Internet research on course materials) --> (Creation of instruction and learning materials and activities)
    (Creation of instruction and learning materials and activities) --> (Creation of course on LMS / LE)
    (Creation of course on LMS / LE) --> (Recommended duration of course)
    (Recommended duration of course) --> (Course Designer Approval)
    (Course Designer Approval) --> (Course Implementation)
    (Course Implementation) --> (Reviews analytics)
}

AI --> (Reviews analytics)
AI --> (Reviews student questions and Discussion board)
Course_Designer --> (Course Designer Approval) :approve and set boundaries
Learner --> (Course Implementation) :interacts and collaborates via LE



@enduml
```
