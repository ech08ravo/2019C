# Meeting activities overview

<a href="https://raw.github.sydney.edu.au/crli/EDPC5022-2019/master/resources/images/activities-overview.png?token=AAAChz4FBAtmXWAvP4CGxKR776Q8P9veks5cockTwA%3D%3D" target="_blank"> <img src="https://raw.github.sydney.edu.au/crli/EDPC5022-2019/master/resources/images/activities-overview.png?token=AAAChz4FBAtmXWAvP4CGxKR776Q8P9veks5cockTwA%3D%3D"></img></a>

```
digraph G {

graph [fontsize=10 fontname="Verdana" compound=true];
node [fontsize=10 fontname="Verdana"];

bgcolor="Gainsboro";
label="Meeting Activities for Participatory Decision-Making";
fontcolor="Black";

      subgraph cluster_0 {
         style=filled;
         color=DodgerBlue;
         label = "Divergent";

         subgraph cluster_Ideation{
           color=SkyBlue;
               label="Idea Generation and Mental Model Alignment";
               node [style=filled,color=white,shape=box];
               "RepGrid" [color=SpringGreen] "Mind-Concept Mapping" [color=LemonChiffon] "Five Whys" [color=PowderBlue] "Brainwriting" [color=PowderBlue]  "3-12-3 Brainstorming" [color=PowderBlue];   
          }
        }
      subgraph cluster_1 {
         style=filled;
         color=Yellow;
         label = "Convergent";

         subgraph cluster_Creating_Agreement{
             color=Gold;
              label="Creating agreement and Consensus";
             node [style=filled,color=white,shape=box];
           "Forced Ranking" [color=PaleGreen];    
}

          subgraph cluster_Sorting_Clustering{
            color=LemonChiffon;
            label="Sorting and Clustering";
            node [style=filled,color=white,shape=box];
           "Affinity Mapping" [color=Gold] "Card Sorting" [color=Gold];
            }
}

    subgraph cluster_2 {
         style=filled;
         color=SpringGreen;
         label = "Evaluation";

         subgraph cluster_Decision_Making {
                color=PaleGreen;
                label="Decision Making and Generating Commitment";
                    node [style=filled,color=white,shape=box];
                   "Dot Voting" [color=SpringGreen] ;
       }
  }
}

 "RepGrid"  -->  "Affinity Mapping"  [ltail=cluster_0,lhead=cluster_1];
 "Card Sorting" --> "Dot Voting"  [ltail=cluster_1 l,head=cluster_2];
 }

 ```
