# Use Cases

> Keep your use cases in this document, or create further documents of this kind if documents gets too long. Note that when you render the markdown in html you can get an url for any heading by pointing to the left of the heading and then right-click and copy the heading bookmark link. 

> [Link to wiki page on use cases](https://github.sydney.edu.au/crli/EDPC5022-2019/wiki/Use-case-Diagrams) 

> Use this document for the narrative description as well: What are your main ideas for the functionality of a future LDE (Learning Design Environment)? Why do you think the functionality is needed? What are alternatives? etc.

## Use Case 1

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. 

![Submit Rule](https://www.plantuml.com/plantuml/img/VL193i8m3Bpx5JwsX_O1750vS4M8vG6c2LNKD8aIHwX2_9sqL6KHgW-MDPuPBm1LOF8SEuq0eLN6aQSE7TKjDVB8lPRePSra6Yq1g6RhyHHJdkgDw9HHWJqD6C1CnaFKSYlKGBe3fXXbM61sZ9TECVf4oCVE5uAbi3TJhZ7RMLRN7kbpH8uhPMeTXVoZB7xMMV3Uamzo0XSSP_xP2UAN83t4sJ0Srh-r20-0IXgHNWbF)


```
@startuml 

skinparam packageStyle rectangle

actor Tutor
actor Administrator


rectangle RuleEditor {
    Tutor - (Submit rule)
    (Submit rule) .down.> (Notify administrator) :include
    (Submit rule) - Administrator
    (Submit rule) .down.> (Parse rule) :include
    (Submit rule) .down.> (Update rule repository) :include 
}

@enduml
```

## Use Case 2


(...)

## Use Case n
