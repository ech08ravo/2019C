# Which model should I use?

![](https://github.sydney.edu.au/crli/EDPC5022-2019/blob/master/resources/images/whats-my-graph.png)

```
@startuml
start

skinparam {
	wrapWidth 300
    }

while (Are you documenting business processes?) is  (yes)

#Linen:You might find activity diagrams useful to represent your model. These examples are from the
[[http://plantuml.com/activity-diagram-beta{PlantUML online reference guide} New Activity Diagram Beta syntax and features webpage]] and there are also examples at [[https://tallyfy.com/uml-diagram/#activity-diagram{link to Tallyfy website} All You Need to Know About UML Diagrams: Types and 5+ Examples webpage]].;



note left
For more complexity, or to annotate your model, you can nest sub-graphs as notes.

{{
	digraph G {
	graph [fontsize=10 fontname="Verdana" compound=true style=filled shape=box bgcolor="PaleGreen"]
	node [fontsize=10 fontname="Verdana" style=filled];
	Evaluation [label = "Decision Making and Generating Commitment" shape=box style=filled color=DarkSeaGreen];
	DV [URL="https://github.sydney.edu.au/crli/EDPC5022-2019/blob/master/resources/ActivityModels/dot-voting.md"] [label="Dot Voting" color=DarkSeaGreen];
	RepGrid [URL="http://grid.eilab.ca"] [label="Repertory Grid Technique" color=DarkSeaGreen];
	FR [URL="https://github.sydney.edu.au/crli/EDPC5022-2019/blob/master/resources/ActivityModels/forced-ranking.md"] [label="Forced Ranking" color=DarkSeaGreen];
	Evaluation -> {RepGrid DV FR} [penwidth= 3 style=dotted color=SeaGreen];
	}
}}

{{
start

:foo1;
-> You can put text on arrows;
if (test) then
  -[#blue]->
  :foo2;
  -[#green,dashed]-> The text can
  also be on several lines
  and **very** long...;
  :foo3;
else
  -[#black,dotted]->
  :foo4;
endif
-[#gray,bold]->
:foo5;


stop
}}

end note

endwhile (no)

while (Are you documenting use cases or system requirements?) is  (yes)

#Turquoise:Try the use case model, which can indicate outside actors as well as system configuration. This example uses the built-in template for a Use Case Package Diagram from [[https://www.planttext.com/?text=VLBDJeGm4BxtAUO81tW0OynorxZ9hWzGwG0DtHRRgOh6TtU0NLmMTozDslb-9zq4afxYmO0GeTMsaruUe9DbAslSKMyGF9OaRMrG2DB43qNeRTbuPrqCaF0u-g3VCOKAKRqoLGXPalEmZPrcuUcoZtpkaTM5c0QPrtL3sIZXl8BWJ2JjR2h4x0b5rnbTok4TlWN0KJHZMYEj0ctFU3nUYK6ct8VD7lx1mvt5JnfPwra-fikPPntfgWSQ2WGcCQuqKU50XAImqlHVU6veiE9QS-49jtQOWwqbvc2Gx1hfSLvjEZHVAlyjv19wDU39-99mm_O-PwNGmbl4SCp8MBGgJFYNJab2U7vyohOtGow0LogUyYr5ftG__7ysxCj_zXS0{link to plantuml.com}PlantText.com]] and there is also an example in the class GitHub site [[https://github.sydney.edu.au/crli/EDPC5022-2019/blob/master/resources/multiPAL-use-case.md {link to class GitHub} labelled multiPAL-use-case.md]].;


note right
Use styling or notes to highlight the difference in a sub-processes.

{{

	title Package - Use Case A


	rectangle Features {
	    (Login)
	    (Create / Delete User) as CDU
	}

	:Employee:
	:Client:
	:Supervisor:

	Employee --> (Login)
	Supervisor --> (Login)
	Client ..> (Login) : NO!!!!
	Supervisor ---> CDU: I am god

	}}

{{

	title Package - Use Case B


	rectangle Features {
	    (Login)
	    (Create / Delete User) as CDU
	}

	rectangle "Management Layer" {
			(Enable User Database) as EUD
	}
	:Client:
	:Supervisor:

	Supervisor --> (Login)
	Client ..> (CDU) #blue : At my convenience
	Client ..> (Login) #blue : YES!!!!
	Supervisor ---> EUD #turquoise : I am good
	EUD ---> CDU #turquoise
	CDU ..> (Login) #blue
	Login <---> CDU #turquoise

}}

end note



endwhile (no)

while (Are you documenting system configurations?) is  (yes)

#Lavender:Try the component model, which can show interaction between components on different layers. There are both simple and complex examples at
[[http://plantuml.com/component-diagram{link to plantuml.com} plantuml.com]], the PlantUML Reference Guide [[http://plantuml.com/guide{link to PlantUML Reference Guide} PlantUML Reference Guide pp 77-78]] and [[https://tallyfy.com/uml-diagram/#component-diagram{link to tallyfy component diagram anchor} tallyfy.com component diagram]].;

note left #cornflowerblue


{{
	package "Some Group" #yellowgreen {

	HTTP - [First Component]
	[Another Component]
	}
	node "Other Groups" #navajowhite {
	FTP - [Second Component]
	[First Component] --> FTP
	}
	cloud {
	[Example 1]
	}
	database "MySql" {
	folder "This is my folder" #palegoldenrod {
	[Folder 3]
	}
	frame "Foo" {
	[Frame 4]  #grey
	[Another Component] --> [Example 1]
	[Example 1] --> [Folder 3]
	[Folder 3] ..> [Frame 4]  #Indigo

}}

end note


endwhile (no)

#Linen:Take a look at  [[https://tallyfy.com/uml-diagram/{link to tallyfy UML diagrams details} the different kinds of UML diagrams to find one suitable for your project.]];

stop
@enduml

```
