![example shared approval workflow](https://www.plantuml.com/plantuml/svg/ZLDTI-j047tE_eg1WjY7rc1ziOXO2mNn1WeAFeZ8T3DD5pUxSNVJKkJ-TtUoyHC5zod9cJddp9dDXG_eGbjh42BpJyeqwB265v5bEuVDdIh31expN6GGpqm6wowjAydDhROE1elk9BH1-OGLtOIz9d0a0vfAa_Wl1AF8lN1BM3yMLA_8UK0FInZa-Ucfb29B1GkKIgk0_Cpu0WPIvZaxI0NNnkuqbHKz5cYYN2gxBcvWi5vpgH3lsd1bL50Ob3LnfCFb44RtlTx3w1mEvxQkLO1WmT0ELWwDt0nXEdU4WVftsAaOGGoc3KUrBTLQoOxGTrDzqferZRDRr569aL_8lnfOjbh7g9vRyY4AooJCl1t5L_XiVD-F-33ctZXpx9cPFLX3ODTmp68e9JK13W0xF_GRKqerCIt-pjE9diKf9YUhoUI4fqW4C2sLbwttRpBGUcKga346Ci734IZl8z0HzPVY8xq2VOYxVFd9xlXTZTqMv2gAXkysbhQy_iuebMowPYnHz6KZZlcVsXAKLhRiPDXBf1ZwPOo_5y6qu6NlGVDdhz9QucBuFb-GAUC_yme0)

```
@startuml 

	skinparam {
		wrapWidth 200
	    ActorBorderColor #FFFFFF
	    packageStyle rectangle
}

    actor Team_Members as P #0099cc
	actor Facilitator as PF #cc0000
	actor Knowledge_Manager as PKMS #ffcc00

rectangle Initiation {
(P) -[#0099cc]-> (Commit to new branch) :Create branch with input/modifications
    
rectangle Approval {
    (Commit to new branch) -[#0099cc]-> (Pull request) :create    
    (Pull request) <.[#ffcc00].> (PKMS) :Any one of 2 to accept & approve
    (Pull request) <.[#cc0000].> (PF) :Any one of 2 to accept & approve
    (PKMS) <-[#34b334]->  (PF)  :discuss request using comments / issues
    }

    rectangle Master {
    (Pull request) .[#34b334].> (Merge) :Whoever accepted to merge
    (Merge) --> (Live document)
    (P) <.[#0099cc]. (Live document) :Modify live site      

}

@enduml
```
