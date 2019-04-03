<p align="center">
  <img width="100%" src="https://github.sydney.edu.au/eablack/5022_2019S1/blob/master/images/EDPC5022_readings_image.svg?sanitize=true">
</p>
<p>Below is the original notation as text (without the HTML "code" tags), which generates the graph above. I based the code on http://iinozemtsev.net/2015/09/08/gravizo.html, and used http://gravizo.com to test the graph encoding iteratively until I got the result I wanted. Scroll down to see how to do this in your own GitHub repo.</p>
<code>digraph Cluster {
  rankdir=LR;
  node [shape="rect" style="filled"];
Introduction_to_course_technology [fillcolor="gainsboro"];
Introduction_to_course_technology -> Weekly_Readings;
subgraph cluster1 {
label = "Topics";
Weekly_Readings ->
{Designs_as_Knowledge_Objects [fillcolor="lavender"], Instructional_Design [fillcolor="lightsalmon"], Design_Representations_Overview [fillcolor="gold"], Design_Patterns [fillcolor="olivedrab2"], Educational_Modelling_Languages [fillcolor="darkkhaki"],
IMS_Learning_Design [fillcolor="mediumspringgreen"], Assessment_Design [fillcolor="violet"], Meta_Design [fillcolor="plum"], Learning_Design_Tools [fillcolor="sandybrown"],
Collaboration_Design [fillcolor="wheat"], Uptake [fillcolor="turquoise"] }
 }
[dir="forward"];
subgraph cluster2 {
label = "Works"  [color=red] ;
Designs_as_Knowledge_Objects -> {Conole_Jones_2010[fillcolor="lavender"],Nicolini_Mengis_Swan_2012
[fillcolor="lavender"]}
Instructional_Design -> {Seel_Lehmann_Blumschein_Podolskiy_2017 [fillcolor="lightsalmon"]}
Design_Representations_Overview -> {Falconer_Beetham_Oliver_Lockyer_Littlejohn_2007 [fillcolor="gold"]}
Design_Patterns -> {McAndrew_Goodyear_Dalziel_2006 [fillcolor="olivedrab2"]}
Educational_Modelling_Languages -> {CaeiroRodriguez_2008 [fillcolor="darkkhaki"]}
IMS_Learning_Design -> {Tattersall_Sodhi_Burgos_Kopeer_2008 [fillcolor="mediumspringgreen"]}
Assessment_Design -> {Mislevy_Almond_Lukas_2003 [fillcolor="violet"], Riscontente_Mislevy_Hamel_PADI_2005 [fillcolor="violet"]}
Collaboration_Design->{Sobreira_Tchounikine_2012[fillcolor="wheat"],RodríguezTriana_MartínezMonés_AsenioPérez_Dimitriadis_2015 [fillcolor="wheat"]}
Meta_Design -> {Fischer_Hermann_2014 [fillcolor="plum"],Rabardel_Beguin_2005[fillcolor="plum"]}
Learning_Design_Tools -> {Ljubojevic_Laurillard_2010 [fillcolor="sandybrown"]}
Uptake -> {Dagnino_Dimitriadis_AsensioPérez_Pozzi_2018 [fillcolor="turquoise"]}}
} </code></p>
<p>&nbsp;</p>
<p>If you use gravizo.com to test your modelling code - the graph will change in real time. </p>
<p>When your draft is complete, right-click on the graph and open in new tab/window.</p>
<p>You will seee a long encoded URL in the address field. This is the description of your graph a browser will use to display it.</p>

<p>If you continue to use gravizo.com to make changes to your code, each time you right-click the displayed graph it will regenerate the code and give you and updated URL to display the current version. This works because the long URL contains all the information in the code above, but in a hard-for-humans-to-read format. Instructions for testing this are below.</p>

<p>You can test this by copying everything below from and including "http://gravizo.com ... turquoise%22]}}}", then pasting it into a browser window. You will see the same graph display. </p>
<p> Keeping it in code is useful because you can immediately see your changes during test encoding, but saving your draft and final versions as SVG means it's easier to paste into applications that don't render systems diagrams well, such as Microsoft Word.</p>
<code>(
http://www.gravizo.com/svg?digraph%20Cluster%20{%20%20rankdir=LR;%20%20%20node%20[shape=%22rect%22%20style=%22filled%22];Introduction_to_course_technology%20[fillcolor=%22gainsboro%22];Introduction_to_course_technology%20-%3E%20Weekly_Readings;subgraph%20cluster1%20{label%20=%20%22Topics%22;Weekly_Readings%20-%3E%20{Designs_as_Knowledge_Objects%20[fillcolor=%22lavender%22],%20Instructional_Design%20[fillcolor=%22lightsalmon%22],%20Design_Representations_Overview%20[fillcolor=%22gold%22],%20Design_Patterns%20[fillcolor=%22olivedrab2%22],%20Educational_Modelling_Languages%20[fillcolor=%22darkkhaki%22],%20IMS_Learning_Design%20[fillcolor=%22mediumspringgreen%22],%20Assessment_Design%20[fillcolor=%22violet%22],%20Meta_Design%20[fillcolor=%22plum%22],%20Learning_Design_Tools%20[fillcolor=%22sandybrown%22],%20Collaboration_Design%20[fillcolor=%22wheat%22],%20Uptake%20[fillcolor=%22turquoise%22]%20}%20}%20[dir=%22forward%22];subgraph%20cluster2%20{label%20=%20%22Works%22%20%20[color=red]%20;Designs_as_Knowledge_Objects%20-%3E%20{Conole_Jones_2010[fillcolor=%22lavender%22],Nicolini_Mengis_Swan_2012[fillcolor=%22lavender%22]}Instructional_Design%20-%3E%20{Seel_Lehmann_Blumschein_Podolskiy_2017%20[fillcolor=%22lightsalmon%22]}Design_Representations_Overview%20-%3E%20{Falconer_Beetham_Oliver_Lockyer_Littlejohn_2007%20[fillcolor=%22gold%22]}Design_Patterns%20-%3E%20{McAndrew_Goodyear_Dalziel_2006%20[fillcolor=%22olivedrab2%22]}Educational_Modelling_Languages%20-%3E%20{CaeiroRodriguez_2008%20[fillcolor=%22darkkhaki%22]}IMS_Learning_Design%20-%3E%20{Tattersall_Sodhi_Burgos_Kopeer_2008%20[fillcolor=%22mediumspringgreen%22]}Assessment_Design%20-%3E%20{Mislevy_Almond_Lukas_2003%20[fillcolor=%22violet%22],%20Riscontente_Mislevy_Hamel_PADI_2005%20[fillcolor=%22violet%22]}Collaboration_Design-%3E{Sobreira_Tchounikine_2012[fillcolor=%22wheat%22],Rodr%C3%ADguezTriana_Mart%C3%ADnezMon%C3%A9s_AsenioP%C3%A9rez_Dimitriadis_2015%20[fillcolor=%22wheat%22]}Meta_Design%20-%3E%20{Fischer_Hermann_2014%20[fillcolor=%22plum%22],Rabardel_Beguin_2005[fillcolor=%22plum%22]}Learning_Design_Tools%20-%3E%20{Ljubojevic_Laurillard_2010%20[fillcolor=%22sandybrown%22]}Uptake%20-%3E%20{Dagnino_Dimitriadis_AsensioP%C3%A9rez_Pozzi_2018%20[fillcolor=%22turquoise%22]}}}
)</code>
