<p align="center">
  <img width="100%" src="https://github.sydney.edu.au/eablack/5022_2019S1/blob/master/images/EDPC5022-session-image.png?sanitize=true">
</p>
<p>Below is the original notation as text. It repeatedly crashed gravizo.com, but http://plantuml.com/ managed it. My code could probably do with some refinement.</p>
<code>
digraph G {
rankdir=TB;
Week_1[shape=box,style=filled,fillcolor="whitesmoke"];
Introduction[shape=oval,style=filled,fillcolor="gainsboro"];
Week_1->Introduction[color="gray",dir="both",style=dotted];
Week_2[shape=box,style=filled,fillcolor="aliceblue"];
Week_1->Week_2[color="gray"];
Designs_as_Knowledge_Objects[shape=oval,style=filled,fillcolor="lavender"];
Introduction->Designs_as_Knowledge_Objects[color="gainsboro",dir="both"];
Week_2->Designs_as_Knowledge_Objects[style=dotted,color="lavender"];
Week_3[shape=box,style=filled,fillcolor="lightcyan"];
Week_2->Week_3[color="gray"];
Instructional_Design[shape=oval,style=filled,fillcolor="lightsalmon"];
Designs_as_Knowledge_Objects->Instructional_Design[color="lavender",dir="both"];
Design_Representations_Overview[shape=oval,style=filled,fillcolor="gold"];
Week_3->Instructional_Design[style=dotted,color="lightsalmon"];
Week_3->Design_Representations_Overview[style=dotted,color="gold"];
Week_4[shape=box,style=filled,fillcolor="snow"];
Week_3->Week_4[color="gray"];
Week_4->Instructional_Design[style=dotted,color="lightsalmon"];
Design_Patterns[shape=oval,style=filled,fillcolor="olivedrab2"];
Week_4->Design_Patterns[style=dotted,color="olivedrab2"];
Design_Representations_Overview->Design_Patterns[style=dotted,color="olivedrab2"];
Instructional_Design->Design_Patterns[dir=both,color="olivedrab2"];
Design_Representations_Overview->Instructional_Design[dir=both,color="lightsalmon"];
Week_5[shape="box",style=filled,fillcolor="azure"];
Week_4->Week_5[color="gray"];
Educational_Modelling_Languages[shape=oval,style=filled,fillcolor="darkkhaki"];
Instructional_Design->Educational_Modelling_Languages[dir=both,color="darkkhaki"];
Design_Patterns->Educational_Modelling_Languages[dir=both,color="darkkhaki"];
Week_5->Instructional_Design[style=dotted,color="lightsalmon"];
Week_5->Educational_Modelling_Languages[style=dotted,color="darkkhaki"];
Week_6[shape=box,style=filled,fillcolor="seashell"];
Week_5->Week_6[color="gray"];
IMS_Learning_Design[shape=oval,style=filled,fillcolor="mediumspringgreen"];
Week_6->Instructional_Design[style=dotted,color="lightsalmon"];
Week_6->Educational_Modelling_Languages[style=dotted,color="darkkhaki"];
Week_6->IMS_Learning_Design[style=dotted,color="mediumspringgreen"];
Instructional_Design->IMS_Learning_Design[color="mediumspringgreen",dir="both"];
Week_7[shape=box,style=filled,fillcolor="aliceblue"];
Week_6->Week_7[color="gray"];
Assessment_Design[shape=oval,style=filled,fillcolor="violet"];
Instructional_Design->Assessment_Design[color="violet",dir="both"];
IMS_Learning_Design->Assessment_Design[color="violet",dir="both"];
Educational_Modelling_Languages->Assessment_Design[color="darkkhaki",dir="both"];
Week_7->Assessment_Design[color="violet",style=dotted];
Week_8[shape=box,style=filled,fillcolor="lightblue"];
Week_7->Week_8[color="gray"];
Collaboration_Design[shape=oval,style=filled,fillcolor="wheat"];
Week_8->Collaboration_Design[color="wheat",style=dotted];
Assessment_Design->Collaboration_Design[dir="both",color="wheat"];
Common_Vacation_Week_Easter
[shape=box,style=filled,fillcolor="ghostwhite"];
Week_8->Common_Vacation_Week_Easter[color="gray"];
Meta_Design[shape=oval,style=filled,fillcolor="plum"];
Collaboration_Design->Meta_Design[dir="both",color="plum"];
Common_Vacation_Week_Easter->Meta_Design[style=dotted,color="plum"];
Week_9[shape=box,style=filled,fillcolor="powderblue"];
Common_Vacation_Week_Easter->Week_9[color="gray"];
Week_9->Meta_Design[style=dotted,color="plum"];
Week_10[shape=box,style=filled,fillcolor="paleturquoise"];
Week_9->Week_10[color="gray"];
Learning_Design_Tools[shape=oval,style=filled,fillcolor="sandybrown"];
Week_10->Learning_Design_Tools[style=dotted,color="sandybrown"];
Meta_Design->Learning_Design_Tools[dir=both,color="sandybrown"];
Week_11[shape=box,style=filled,fillcolor="lightsteelblue"];
Week_10->Week_11[color="gray"];
Uptake[shape=oval,style=filled,fillcolor="turquoise"];
Week_11->Uptake[style=dotted,color="turquoise"];
Learning_Design_Tools->Uptake[dir=both,color="turquoise"];
Week_12[shape=box,style=filled,fillcolor="lightgrey"];
Week_11->Week_12[color="gray"];
Week_13[shape=box,style=filled,fillcolor="gray"];
Week_12->Week_13[color="gray"];
End_of_Session[shape=box,style=filled,fillcolor="whitesmoke"];
Week_13->End_of_Session[color="gray"];
Uptake->End_of_Session[style=dotted,color="gray"];
}
</code>

<p>If you use plantuml.com to test your modelling code - the graph will change in real time. </p>
<p>The encoded URL is too long, which means it's likely the code can be less verbose. It would be useful to do this to be able to embed in a browser.</p>

<p> Keeping it in code is useful because you can immediately see your changes during test encoding, but saving your draft and final versions as SVG means it's easier to paste into applications that don't render systems diagrams well, such as Microsoft Word.</p>
