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




![model](https://raw.github.sydney.edu.au/crli/EDPC5022-2019/master/resources/images/example-workflow-roles.png?token=AAACh9G6g7rFEsokebHV0e5fJ_3TiuAZks5cpyYcwA%3D%3D)

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


	P -[#0099cc]-> L: use a [[https://www.random.org/sequences/{link to example}random sequence generator]] or other [[https://wheeldecide.com/{wheeldecide}randon method]]\nto assign initial roles for the first meeting - \ntwo defined roles (Facilitator and Knowledge Manager) and others as participants
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
	PKMS -[#ffcc00]> GH: assign action items using Issues, @mentions and Milestones

	```
	Zoom -[#ffcc00]-> UML: review meeting recording against \nmeeting agenda, record and \nassigned action items, and add a summary \nof important points, plus the \ntime index in the recording \nwhere they occur, \nin the meeting record
	UML -[#ffcc00]-> GH: modify meeting notes and \nassigned issues with GH annotations \nthat describe rationale

	```
	P <-[#0099cc]-> GH: complete assigned tasks and use a pull request to Knowledge_Manager in GH for approval
	PKMS -[#ffcc00]-> GH: approve pull requests and merge to appropriate branch
	PM -[#cc66ff]-> GH: follow up action items due \nduring the interval between meetings
	PM -[#cc66ff]-> UML: ensure all items from previous meeting \nhave been updated on the new agenda you are creating


	@enduml
```
