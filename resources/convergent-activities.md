![convergent meeting activities](https://www.plantuml.com/plantuml/svg/jLDRQzim57xFhpZetLQQqOTkQ12y9Iyrb9GDHiY3R1tROheXoVMoqly-EV70APGMIjya7VZETzD2oDPpry4M7XVdqxwn9WRv5zdL4iQpuHeP-ObUSCC9r5Oxsnl1ekyHGZmgP8rK2WM4ZZjabVq3LLjRPJqZlr0fEv33mbY1hsBFqGvV5eKr3-XRD17sYbUeW06vjpvAqm8t0WhLXuW-NSbi-GMdCu-jLIFWkeJzZzqj8rsCBdocj9Mnwwiy78N1OuwYptbFQwya_VxjhhXUhbRPQdbrGojbAwhvk8nw3BRtDGQwhgDyaF5O9cqgKDuqqgHhfhdBjI27YJKZwsa29NVknFPCwnQrDKKdc-J5gFV-8-dLt8ii9FSkkHNf6IPJN-1L5izz6uOXrz88ZN9ScgTIq1bccKPPIgz65r_H_BvUh6R5A3poKpFMhKVKOsjE7R4ce0bzU5j5DhkFpA2nwLLadflVYUbb49lJ37RdsN-xxhZ2RT9ZBlz3zXKUKvjJOr8uJx1tQ0OfOiVWqoHEs1YVYviRDo6CsMvsRqPu-WS0)
```
digraph G {
graph [fontsize=10 fontname="Verdana" compound=true style=filled shape=box bgcolor="Yellow"]
node [fontsize=10 fontname="Verdana" style=filled];
Convergent [label = "Sorting and Clustering" shape=box style=filled color=Gold];
AM [URL="https://github.sydney.edu.au/crli/EDPC5022-2019/blob/master/resources/ActivityModels/affinity-map.md"] [label="Affinity Mapping" color=LemonChiffon];
CS [URL="https://github.sydney.edu.au/crli/EDPC5022-2019/blob/master/resources/ActivityModels/card-sort.md"] [label="Card Sorting" color=LemonChiffon];
MCM [URL="https://www.mindmeister.com/"] [label="Mind-Concept Mapping" color=LemonChiffon];
node [fontsize=10 fontname="Verdana" style=filled];
Convergent2 [label = "Creating Agreement and Consensus" shape=box style=filled color=Gold];
FR [URL="https://github.sydney.edu.au/crli/EDPC5022-2019/blob/master/resources/ActivityModels/forced-ranking.md"] [label="Forced Ranking" color=PaleGreen];
Convergent -> {AM CS MCM} [penwidth= 3 style=dotted color=Gold];
Convergent2 -> {AM MCM FR} [penwidth= 3 style=dotted color=Gold];
}
```
