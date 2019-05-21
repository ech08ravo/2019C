Welcome to the EDPC5022 Group C repo!
=========================================
Our group project seeks to envision and design the future learning design environments. 

We are figuring out what kind of learning environments will designers have to create in five years more. And which methods and technologies are they going to need in support of their work.

To address these questions, we are working on different design prototypes that you can explore in our repo. 

This README.md provides you with the weekly updates of the project and also gives you an orientation about how to navigate through the repo.


## System design overview

This week we are working on two issues ([#32](https://github.sydney.edu.au/crli/EDPC5022-2019-TeamC/issues/32) and [#33](https://github.sydney.edu.au/crli/EDPC5022-2019-TeamC/issues/33))related to developing ideas for integrating Design Critique into a scalable, distributed Learning Design and Authoring process. 

You can check our designs in the following sections.

### Use cases

Here is showed the use cases that we have modelled to capture the system’s high-level requirements. 

* Link to [use case document](https://github.sydney.edu.au/crli/EDPC5022-2019-TeamC/blob/master/Use-cases.md)  

### Interaction sequences

Here is depicted the structure of the system. 

* Link to [interactions document](https://github.sydney.edu.au/crli/EDPC5022-2019-TeamC/blob/master/Interactions.md)

### Components

Here is stated an overview of the elements that make up the system.

* Link to [components document](https://github.sydney.edu.au/crli/EDPC5022-2019-TeamC/blob/master/Components.md)


#### Definitions:

Here is a description of the various components and clarification on their functionality within the system.

* Link to [definitions document](https://github.sydney.edu.au/crli/EDPC5022-2019-TeamC/blob/master/Definitions.md)

#### System Function Description

The adaptive course design system offers automated and authoring tools for the designer to adapt the design to the needs of the users. The System designer will manage and add to the cloud repository and both Personalisation and Learning Analytics engines; also offering technical support and administration.

When using the Personalisation Engine, the Course Designer will input all necessary data including desired LMS platform, duration, pedagogical preferences and/or activities.

The Personalisation Engine will search the information through the web and Cloud Repository and generate a suggested Learning Environment appropriate to the boundaries set.

The Instructor and Learner will engage with the Learning Environment, where the xAPI will collect user experience data and feed back to the Learning Analytics Platform. The Instructor is able to engage with the Learning Analytics Platform in order to monitor and administer student data and interactions

Learning Design research shows that the context of learning and the need for systems to be flexible, adaptive and user friendly, as such, the Course Designer has the choice of inputting boundaries or design requirements into the Personalisation Engine. The Course Designer can engage with the Personalisation Engine to determine one or all of the following:

Learning objectives
Monitoring needs
Pedagogical patterns
Learning platform
Based on the boundaries and requirements set, the AI system will then generate a suggested learning course and environment appropriate to the learning context.

The Learning Analytics Platform is an automated authoring engine that collects and filters interaction data from the Instructor and Learner.

The Instructor engages with the Learning Environment by delivering the content, facilitating learning, monitoring course interactions and approving/amending course design suggestions from the Personalisation Engine.

The Learner engages with the Learning Environment by interacting with the learning content, assessments, user interface and pedagogy activities. The Learning Environment feeds interaction data back through the xAPI to the Learning Analytics Platform database which feeds the Personalisation Engine; which in turn generates web and repository searches for automated coaching courses for the learner.

In a LD with integrated Design Critique process, the following would apply:

proposed Learning Environment would be generated after the use of a Personalisation Engine
the various stakeholders and designers will engage in a design critique
if approved, it will then be deployed as a Learning Environment
if not approved, adjustments will be made by the Course Designer and re-proposed for critique until approved.
