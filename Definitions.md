
# Definitions
This file aims to clarify some of the terminology and functionality of various components within this project.

## Component Characteristics:

***Personalisation Engine Characteristics***
Two-fold function: search engine + AI.
Looks for information on the web and repository and also comes up with a suggestion based on that search to include in the Learning Environment.
It has AI.

***xAPI Characteristics***
Only monitors user interactions in the Learning Environment and stores this data in the Learning Analytics Platform.
It doesn’t have AI.

***Learning Analytics Platform Characteristics***
Learning Analytics Platform feeds to the Personalisation Engine, which feeds to the Learning Environment.
Course designer will only engage with the Personalisation Engine, not the Learning Analytics Platform.

## System Function Description

The adaptive course design system offers automated and authoring tools for the designer to adapt the design to the needs of the users. The System designer will manage and add to the cloud repository and both Personalisation and Learning Analytics engines; also offering technical support and administration.

When using the Personalisation Engine, the Course Designer will input all necessary data including desired LMS platform, duration, pedagogical preferences and/or activities.

The Personalisation Engine will search the information through the web and Cloud Repository and generate a suggested Learning Environment appropriate to the boundaries set.

The Instructor and Learner will engage with the Learning Environment, where the xAPI will collect user experience data and feed back to the Learning Analytics Platform. The Instructor is able to engage with the Learning Analytics Platform in order to monitor and administer student data and interactions

Learning Design research shows that the context of learning and the need for systems to be flexible, adaptive and user friendly, as such, the Course Designer has the choice of inputting boundaries or design requirements into the Personalisation Engine. The Course Designer can engage with the Personalisation Engine to determine one or all of the following:
* Learning objectives
* Monitoring needs
* Pedagogical patterns
* Learning platform

Based on the boundaries and requirements set, the AI system will then generate a suggested learning course and environment appropriate to the learning context.

The Learning Analytics Platform is an automated authoring engine that collects and filters interaction data from the Instructor and Learner.

The Instructor engages with the Learning Environment by delivering the content, facilitating learning, monitoring course interactions and approving/amending course design suggestions from the Personalisation Engine.

The Learner engages with the Learning Environment by interacting with the learning content, assessments, user interface and pedagogy activities. The Learning Environment feeds interaction data back through the xAPI to the Learning Analytics Platform database which feeds the Personalisation Engine; which in turn generates web and repository searches for automated coaching courses for the learner.

In a LD with integrated Design Critique process, the following would apply:
* proposed Learning Environment would be generated after the use of a Personalisation Engine
* the various stakeholders and designers will engage in a design critique
* if approved, it will then be deployed as a Learning Environment
* if not approved, adjustments will be made by the Course Designer and re-proposed for critique until approved.

This Use Case Diagram demonstrates system functionality:
![Submit Rule](https://www.plantuml.com/plantuml/img/ZLDBIyD04BxlhvYZFHJlHSHGFHGKYY8UosPtZ0l9J9YPL8lutzqq1LzfpMbX-LxxpUoLcXVhcjevIrOZ52ieecyjRH5kh-5XfuODF2h2Gq3oaXZkE6Bj18DvglQKpG7s3kviZQ9ClaxgBJ713LM9S0ONyyYlDB-4ioSiPoU1ageNwv5BxaHHpszecuIfGJA5PSrTX7jiMPEnx4vfpNkLM_H2YIhu9ZDpNzT59kui1OLrxUsPfJaGZwYwSSM1yrQiLtsYuVpfFsRqNuwkdLw4-t3383RNgAaYb270n1eNWSaabPsXWZ6CYus_VT4ARrFiYHXUGBksPJ5mW_KlYMFJMYZcO2Lt5FEYPIst8ZNfGivtqZplOzvNKV0KeM7g7wH_o5Dh01zZNy1nzx59PLe8gDd0xN7_z9N8K7om8NFWklObYxVVzAcXaIfVvSeIWNDNI37_wKy0)
