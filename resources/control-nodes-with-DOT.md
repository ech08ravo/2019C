## Control nodes with Dot

This code shows how to use ports to let arrows leave/join a node in a particular direction. It also shows the effects of weighing a link so that we get straight lines. 

![Alt text](https://g.gravizo.com/svg?
 digraph Control_nodes {
  rankdir="LR";
 "Start" [shape=doublecircle];
 "Stop" [shape=doublecircle];
 "Test1" [shape=diamond];
 "Test2" [shape=diamond];
 "f1" [shape=rectangle; height=2;width=.1; style=filled];
 "j1" [shape=rectangle; height=2;width=.1; style=filled];
 "Start" -> "Test1";
 "Test1" -> "A" [weight="9"];
 "A" -> "f1" [weight="9"];
 "f1" -> {"B"; "C"};
 {"B"; "C"} -> "j1";
 "j1" -> "Test2" [weight="9"];
 "Test2" -> "D"; -> "Stop";
 "Test1" -> "Test2" [tailport="n"; headport="n"];
}
)