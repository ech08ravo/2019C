![example of a full team collaboration workflow](https://www.plantuml.com/plantuml/svg/ZLHDRzim33r7lu90BWsmPC7QIuEYQvOXxT1b2DOEEmn38SkChSMMF4bkK1JxxwFaZpYDLqmN6nBVU-GZfIlhk75bdW5Z0xkLgk26v_3C1eETuSLt6RiKtasdR02qvi9fyq6R6Cr2Pzh0S1bMTLfmiUK9thcd3C6WS5mb6R8_Z76FWoKNCfEE-tzkORs4eH1JMi2KTWWPRXnR6EGEBUI8Jgha3H2ZYZbzLUn9IRmzP7JYaOt0hTAx3EC47rPS4QwIkLtTTVZl-NRF3dxV1kfOMcTaL7QqOTlmlHIwHvu_h32FqDYW0SFfzFnSY8xGcdoLGXQX6gaQqafDQDMgEGqkHOZHoaJvo0ZT3b7vtNolp5f7OPrnfNo2p-naFOBnZrhzv_WIJkQnZX0MMYcA7y4CsaIKinI_383A-7x0gYv_aN9f2446Zk22G9kDX_M0zfYs1L2tu23nZw76AlEUrB_W3YB3bKYz3TStbCn2vxbqWB5q0U3JE3sBJa_F0kBw1ZvPMwAbq777_6yMwmDlB_LMb9P-qz20nj-c8wt7mPnN5Jfc_3EcM_2yA8n-h0hsLwIdn4CBY6fTPXbD-c_Yy-seBeG7Lmnz6K3876OU-huAEoAwcBGDd5msDBEv45Yujr_n5-KChq3hWGdGvKlWmN2MKIPjsgdvY6_IvZwfIbwXIT2J1him_YySJSEiaky0QgOZXS_oaQwO5cMEoksLZ1-Ft6DgSwjYwuPCUg5rG-WPo7KiDq_KS7hYs1LD4RsZVm40)

```
@startuml

	skinparam {
		wrapWidth 200
	    ActorBorderColor #FFFFFF
	    packageStyle rectangle
}

actor Facilitator as PF #cc0000
note left
Creates meeting, agenda, and records meeting
endnote

actor Knowledge_Manager as PKMS
note left
Takes meeting notes and distributes meeting knowledge
endnote

actor Team_Members as P #0099cc
note left
Participates in meetings and contributes to the design in between them
endnote


rectangle Planning {
(P) -[#0099cc]-> (Adobe Connect) : Participants
(PF) -[#cc0000]-> (Adobe Connect) : Meeting Chair
(PKMS) <-[#ffcc00]-> (Adobe Connect): Meeting Knowledge Manager


rectangle Designing {

(P) -[#0099cc]-> (New branch in GH) :Commit edit
(P) <-[#34b334]-> (GH Issues) :-
note left
Use Issues to discuss things between meetings
endnote
(PF) <-[#34b334]-> (GH Issues) :-
(PKMS) <-[#34b334]-> (GH Issues) :-


rectangle Approving {
    (New branch in GH) -[#0099cc]-> (GH Pull request) :Create    
    (PKMS) <-[#34b334]->  (PF)  :Pull?
    (GH Pull request) <.[#ffcc00].> (PKMS) :Accept/Reject
    (GH Pull request) <.[#cc0000].> (PF) :Accept/Reject

rectangle Publishing {
    (GH Pull request) .[#34b334].> (GH Merge) :Approved
    (GH Pull request) .[#34b334].> (P) :Rejected
    (GH Merge) .[#34b334].> (GH Live document) :Approver to merge
    (P) <.[#0099cc]. (GH Live document) :Create or modify


}


@enduml
```
