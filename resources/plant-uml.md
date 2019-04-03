We write models with plantuml 

![example](https://www.plantuml.com/plantuml/svg/SoWkIImgAStDuU9ooazIqBLJSCp9J4wrKl18pSd9L-G2yq32G5cWOAP2IKPgKIeNbqDgNWfG5m00)

The easiest way to do this is to use the [PlantText UML Editor](https://www.planttext.com/) 

There a whole [ebook](http://plantuml.sourceforge.net/PlantUML_Language_Reference_Guide.pdf)  available, and see the [PlantText side](http://blog.planttext.com/about/)  and the [PlantUML site](http://plantuml.com/). 

Of course, the main thing is the text description of an UML diagram:

```
@startuml

Bob -> Alice: Hello!
Alice -> Bob: Hi there

@enduml
```
The **basic pattern** is: 

1. Copy model from GH page into plantuml editor
2. Extend/modify model
3. Copy the text back and 
4. Inset a link to the graph generated on plant.

For more serious use, consider using Visual Studio and the extension such as [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced). Of course, this would require to edit your files locally and sync with the repository. GH support is built into Visual Studio, as it is in many other editors. 

It can get arbitrarily complex, but the  language and pattern stay the same. 

```
@startuml

title Packages - Component Diagram

package "Front End" {
    component [Graphic User\nInterface] as GUI
}

cloud Internet {
}
 
node "Middle Tier" {
    [Business Logic]
    [Data Access] as DA  
    interface IMath as Math
    interface "IItems" as Items
} 

database "PostgreSQL\n" {
    [Stored Procs]
}

GUI -down-> Internet
Internet -down-( Math
[Business Logic] -up- Math
DA -- Items
[Business Logic] --( Items
DA .. [Stored Procs]

@enduml
``` 

produces: 

![this](https://www.plantuml.com/plantuml/img/PP71JiCm44Jl-nMhdBYudu1Q25IHMYcezDJcOEmbjKZioDw80yg_iqbe3i4NM_DMipFoDh6EtBSD03jk24jjldHD2HK-XxOBdZnZxdGTTGlGpHIprnX4V_4smnz0EMOPlkoZxcxEu3bHlFh2CyLFRQX2dN1_Bc00C4teBKx84ul500W-M74-EcibnxkZUFU-FFN9UKe93w5sffh5NBF6dJ6YJzRv3d4YxhuHYwFcsyZ6UyMoec1gKpRYwGK30bWn_T19S1aIrv5ERuUhNuASE4IoMCPWKZKMaJweRFZswd6f0qklcJpCwzSjKFMTcf54L-elnVynCPYHZ6qswn2m9M_b0ty1) 
