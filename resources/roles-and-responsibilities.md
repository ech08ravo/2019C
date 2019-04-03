For this project, you will take turns in different roles within your team. An overview of the roles and a sequence diagram showing how they interact each week is below. 

There are two "support roles" that you should take on at least once, Facilitator and Knowledge Manager. 

### Facilitator

The person in this role prepares the weekly team meeting:

* Meeting agenda (--> Template)
* Meeting activities (--> same Template as Agenda)
* Time keeping
* Follow up actions (Issues on Github, Project board updates)
 

### Knowledge Manager: 

* Takes notes during the meeting (--> same Template as Agenda) 
* Makes sure the meeting is recorded
* Reviews the meeting recording and produces a summary of important points other than actions (--> same template as Agenda)

The documents that the two support roles manage should be owned by EB, in each group: She handles pull requests on it, coming from the two roles. 

The other (2-3) group members, but also the two support role members, work in a task-oriented contribution mode: They contribute to pattern and model documents. 

### Group tasks per week

Expressed as **milestones**:

* Vision for conservative scenario
* Vision for progressive scenario
* Next week
* Next week
* Final week

For each of these milestones, it should be clear what kind of artefact should be created/modified, and where. 




![model](https://www.plantuml.com/plantuml/img/hLPDRzms43r7ls8GNn9WFzmU0iGeYYG6R1Vn5aQQe41jOy4bHol25AcIrAutXlzxPqXgRQs3zb9TB7E6y_7cpTD-257usBUc2dVQTiAB5XwgLrilkZ-rYWtyV7nS0JqVPNJ-a_CA_QappiFHMNgIyR6g1DlXAufskS1sXJw02705HyV7xzzBMUndGcgZe-1tDf_1aPJ7z1JxP-ks1jKQbmjXnHgpr-V57t1Kr-nP_7x7-xXy5cnPUzSklxWGovK51txthgwhYfgAMkfEs0YlVxCWZGZXDNjTlXeRptMyw5V9T7unDdrRNCAiLQ2Sx5kqCJdHuTZhet8hN9uwQr5cbx-SQwkgkeBfTK7YTlehN9v07n04N5ytCNRXP3xVRhSpBwnoxSpvzJpWtprQYM7-OBIzW-W0xqNR6NpCNZ1um1ejUWRXzXO86XSRmg35s3W5DvOkKhjwRK5R7RKmu9t103MvaYVKseT8xXYrNSEKRsmTAAorHLLytup6PjNJcA2CwMqwJgdJt9-X4YgQylHwvOoQb64p18JT2Nn2AkEm1cVDxWIk4CTq-GcaHn6f707rSAwTfHhJr6_ibh8Ze90DHE8X1MGUGXHtV2c2GK5fkBtOUni8a8G0zmYkfW3_sIQu3MRO0hPOqhw9ZGwmrSOGR1qo3ZON4FHtV5inTMZwJwsVNz3uE-E4-c4ZD35YNmBj4A-C004mO4L5MKLu4Fi1TPgyWD2HcmeD-J0XMgVGK4547hhyifpdzPHufGJUEtBDcpTKNceOAl0eIHJsUq6WIjChjZ1CETwBPdWhJi2uTPg1WxGtKFOcGS_hmG6q3T7tal59CxonJolJeEdkPuBlpgHhv-bjAdEKUH-eY7cgbbwcmjFUhFcjL1vcJMpDmpZrejZWWc8_dkPMDveKaXPdtp9L7rALEIY24JlNnq0Bc1Oko0PLRt87XOfbNdGfC4MqtPIn1nZ3Cw3J41kI_vuZJw2dtaO0ZqSrnFY_KCn3Pl28Gpl-knBoxb-H_39SALZc_rD370CumC7SXt03Z8LQ1AqVR2CX7ReKCGvRfrlCAGRzYTpy4_m40U6kCRn4ZBdDKW7MiSYetlEDSdFo3F83vjEoKJRIIXJUQFG_ZbmqMAGPWAPj31LNFzwljEGUDngt1sdoiWiU984pNl_9K0ftVcDpAYheUR99vgjIh0zzsmg_8rTIFTrspaV-UdLEarfFQ3nzI8tI41XFRHNUxyLoNysWjtIw0oTbxoTqLjp6nG-QCnOIqYLTx_Qk6VQ35dG8FRAuqY-HymkoabVP6ggk8Ieh3D9hOf5Fvy8WSUINqTSsgPRZRoThvn0wYd2Ny_MTOfwmuYto8l8FX-5cxOnnMt8QuKdyO80AI_AEaNXlI2PM6BU8UzA55r7JbD66dj0JzDN80PE6TpnyH_WFgDpOHcoGObB0N6ScEYMqH9AYrxGYf4K8Wzf1nSy7ij4lkty0)

```
@startuml
skinparam {
	wrapWidth 200
    ActorBorderColor #FFFFFF
    }

actor Team_Members as P #0099cc
actor Facilitator as PF #cc0000
actor Knowledge_Manager as PKMS #ffcc00
actor Next_Facilitator_from_Roster as PM #cc66ff

participant "In class" as L	
participant "GitHub" as GH
participant "UML .md document" as UML
participant "Adobe_Connect" as Zoom


P -[#0099cc]-> L: use a [[https://www.random.org/sequences/{link to example}random sequence generator]] or other method \nto assign initial roles for the first meeting - \ntwo defined roles (Facilitator and Knowledge Manager) and others as participants
PF -[bold,#cc0000]-> UML: Before first meeting only: Peer Facilitator 1 creates a facilitation roster \nwhere each team member takes at least two turns in the role of \nFacilitator and Knowledge Manager over the semester \n(this will depend on team size)
UML -[#cc0000]-> GH: upload facilitation roster to GH
PF -[#cc0000]-> UML: create a meeting agenda from either a spreadsheet or model template
UML -[#cc0000]->  GH: upload agenda to GH
PKMS -[#ffcc00]-> GH: create meeting record document including the agenda
PF -[#cc0000]-> Zoom: log in to Adobe Connect and use the instructions at \n[[https://helpx.adobe.com/adobe-connect/using/creating-arranging-meetings.html{Adobe Connect Meetings Help}Create virtual meeting rooms and arrange layouts]] \nto schedule the team meeting and send invitations 
PF -[#cc0000]> Zoom: host and facilitate meeting using the agenda
PKMS -[#ffcc00]> Zoom: use the instructions at \n[[https://helpx.adobe.com/adobe-connect/using/recording-playing-back-meetings.html{Adobe Connect Recordings Help}Record and play back Adobe Connect meetings]] \nto record your meeting
P -[#0099cc]> Zoom: attend on time and participate in meeting activities
PKMS -[#ffcc00]> GH: take notes during meeting, using the meeting record prepared earlier
PKMS -[#ffcc00]> GH: assign action items
Zoom -[#ffcc00]-> UML: review meeting recording against \nmeeting agenda, record and \nassigned action items, and add a summary \nof important points, plus the \ntime index in the recording \nwhere they occur, \nin the meeting record
UML -[#ffcc00]-> GH: modify meeting notes and \nassigned issues with GH annotations \nthat describe rationale
P <-[#0099cc]-> GH: complete assigned tasks and update GH
PM -[#cc66ff]-> GH: follow up action items due \nduring the interval between meetings
PM -[#cc66ff]-> UML: ensure all items from previous meeting \nhave been updated on the new agenda you are creating 




@enduml
```
