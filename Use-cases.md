# Use Cases

> Keep your use cases in this document, or create further documents of this kind if documents gets too long. Note that when you render the markdown in html you can get an url for any heading by pointing to the left of the heading and then right-click and copy the heading bookmark link. 

> [Link to wiki page on use cases](https://github.sydney.edu.au/crli/EDPC5022-2019/wiki/Use-case-Diagrams) 


## Use Case 1 - Ideal Meta Design Model

The proposed next-generation LDE involves:
- The AI using students' prior past achievements to design the entire course starting with needs assessment conducted from analytics and achievemtn aims
- The AI then automates the wide web and depository search to gather and create teaching and learning activities, sets up and designs the course in the Learning Environment / LMS.  
- The cloud based courses and environments depository is managed by online board of contributors ranging from experts in their field
- The human course designer only approves the course and makes changes before the course goes live.
- The course designer can use two functions, (a) approve) or (b) set boundaries: 
Through the tracking and monitoring of student interaction with the LE and progression throughout the course, the adaptive system will build further predictive models of best course pathways, especially for students at risk of completing the course successfully, if they are on track with course expectations, or if they need to study more or require additional instructional and/ or institutional support. 
The more student data is collected but the AI system, the more tailored the courses become.

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

## Use Case 2 - Achievable Micro Design Model

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
```
