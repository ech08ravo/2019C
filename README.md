Welcome to the EDPC5022 repo! 

The master branch provides the stakeholders with a complete overview of the current design. This README file provides a concise yet complete description of the design and the main design decisions. These documents get updated frequently. 

## System design overview

Provide here an overview of goals, requirements, high-level design decisions etc. 

### Use cases

![plant uml](https://www.plantuml.com/plantuml/img/jLJ1Ri8m3BtdAto40zgTmmGQErJgBl01AAGUYvGcB7QOqBH_dzC2Mmj3Y6szD8djvsS_9nDY7JdLJYcsx12cYKEj6IiePx3O4MEjb8feMFjrjXVBzXJU5SWtcEFMuXk1zjhjs1eQmcXq3uE7a28XpD64kaPVQRR1mqgJGCl2e_oR6B8qx48Hfmezmsj2ob4Pl8AP9PE86fIWOtLxdlyEQOaTgZ4fnboDQI5oSwFLZi1wg70Jo7A8kzlp55u0FJ949DJHl6J7Vh8XT5jy9QbzYoEsFCAps8bZCiqsg-8afRT-_GqY7slns5gsU6ZWbIp_BD_lC4vvxAdAfdnQm1sKZsSIdN4wpC9UJv6lIh4NS1p_YqwTSPyXsRN72DFD9eQjTjtvEJLteejwur0oSPEZ6zgpTMVvwvAh3wMcnO_MlkdAAwrQ4iiZ_yirmrWtIspGIAPh5P9ScYWQgZAht8Fe5pUsUIn5-9QF2SxfLP3M8y7MQX5G7Zyr4KtaYVm4)
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

### Components

![plant uml](https://www.plantuml.com/plantuml/img/dLFDRu8m5B_thtZXpaNlYvK-IJTeILlS4iA125cMgImA9xF_VQqY0pN6xK9UVX_lgu_PlYbsJRjPawzYzLcyL-3HjgatHLEL4DJjRbz1iglBTjLyr5iF3YIBa2h1HGWCDGy5gXny_mcoG0g3mkIaZyvugZI2d3zZOFWIzL5nYO4FMKmDAauZf_YDBGCPInKrN0hBzA6pzCt8r0Goxf8Fom-JZfb1pZ5nE-brnoDjbm8K9gYCv0f16wbeY1VJFEuQJFguwRhvVxdlg4RFcYZ9qi1r2I7QOpWs35ekp2kr7i-27BsShDPrMy81o1-Dfs8qDTBjaC6LEoSJvYxXdiHMlKlxC6Kacx3pgcBtukxRZKh5aewXM4eMuGYQHpHucKkgc8Mdh5zJd4JuThoWKtJ2DTeDCuZu0eTopPt88btGZQzoyat8hDgMzbVz0G00)



### Interaction sequences

At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. 

* Link to [interactions document](https://github.sydney.edu.au/crli/EDPC5022-2019/blob/master/Interactions.md)  and sections in it as needed. 

Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.

