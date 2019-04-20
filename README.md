Welcome to the EDPC5022 repo! 

The master branch provides the stakeholders with a complete overview of the current design. This README file provides a concise yet complete description of the design and the main design decisions. These documents get updated frequently. 

## System design overview

Provide here an overview of goals, requirements, high-level design decisions etc. 

### Use cases

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

### Components

At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. 

* Link to [component document](https://github.sydney.edu.au/crli/EDPC5022-2019/blob/master/Components.md)  and sections in it as needed. 

Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.

### Interaction sequences

At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. 

* Link to [interactions document](https://github.sydney.edu.au/crli/EDPC5022-2019/blob/master/Interactions.md)  and sections in it as needed. 

Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.

