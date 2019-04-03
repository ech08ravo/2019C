# An illustration of a UML use  case diagram

Describes a use case for a system  that supports multiple tutors online to 'teach' a tutee/pupil. 

## Scenario One: Generic

The communication between the tutors amongst each other and with the pupil is sort of "real time", but could be delayed as well. 

 

```
@startuml

title multiPAL use case diagram (basic)

skinparam packageStyle rectangle
scale 2/3

rectangle Web-Application {
    (Log in)
    (Display OLM-P)
    (Configure Tutor Team)
    (Notify Tutors)
    (Present Exercise/Tutorial)
    (Solve Exercise/Think out loud)
    (Ask Question)
    (Diagnose Pupil Action)
    (Decide on Feedback/advise)
    (Communicate Feedback/advise)
    (Adjust Exercise) 
    (Update OLM-P)
   
}

(Log in) .left.|> (Display OLM-P) : include
(Log in) -down-> (Configure Tutor Team)
(Configure Tutor Team) .left.> (Notify Tutors)
(Configure Tutor Team) -down-> (Present Exercise/Tutorial)
(Present Exercise/Tutorial) -down-> (Solve Exercise/Think out loud)
(Ask Question) .left.|> (Solve Exercise/Think out loud) : extends
(Solve Exercise/Think out loud) -down-> (Diagnose Pupil Action)
(Diagnose Pupil Action) -down-> (Decide on Feedback/advise)
(Decide on Feedback/advise) -down-> (Communicate Feedback/advise)
(Adjust Exercise) .left.|> (Communicate Feedback/advise) : extends
(Communicate Feedback/advise) -down-> (Update OLM-P)

Communicator --|> TutorTeam
Diagnoser --|> TutorTeam
InfoSearcher -right-|> TutorTeam

Pupil -right- (Log in)
TutorTeam -left- (Present Exercise/Tutorial)
Pupil -right- (Solve Exercise/Think out loud)
TutorTeam -- (Diagnose Pupil Action)
TutorTeam -- (Decide on Feedback/advise)
TutorTeam -- (Communicate Feedback/advise)
TutorTeam -- (Update OLM-P)
Pupil -- (Update OLM-P)

@enduml
```
![](https://www.plantuml.com/plantuml/img/XLJBRjim4BppA_OO7nW3pIq78qAR0WNSne5Jz4oJQtbZYXJuI6Aq_VTIiQA7NT4w2D3CBBaxiz2T3yA5M6d60WMDK4KTQ5Ki8Ne4AT9BaIYTgE1g8pp96MD-JwOM3LGBkHSbhiCXLJgKGPXI8_DIfEzFynl6EX1-uOONTQr9Ya3Mm6y6wRbQsXB8p8uVNyZNMXpWOVcThrhiipLRAgD3U8h1EdX2KRNK3njeUpZYliLM3ZsQ0FTlw2HvdB-p97JBhwr-mG6x8xC76mDe6rMhAVmU7YFwfi-kCr4QcznOnPeq57B8eII5a6RwYgWsoPEvK2_fz6w2gegccHid58LwZhxlUGP7-6UjcfhU3VQNiG_7u5hZDbp_MPpQ1hU9bZegxBLSsLV35rDk_XzkRrYS6JqXxox9P93X-leB6Otp6VYGhqk-u5j0epoxfEmwcOXz0X_KJQz4XXl6b5cPytNfBSWL3Wt8whesnWl8-gAKEUVfllVmclJPXoDdn3UpjMiKJkuQpb6v2sC1EthOKlqVeLC0RyRZsRqwEUF21WsEvfCXduYc4nqBiz6DfMDxsn7ES7QN8cl-qFy0)


## Scenario Two: Add recursive feedback (at the same time asynchronous variant)
The student in the pupil role uses the knowledge from the last tutoring session and applies in outside the tutorial setting. S/he records the application event and contacts the tutors for feedback. 

```
@startuml 

skinparam packageStyle rectangle

title Asynchronous (recursive) feedback

actor Pupil 
actor TutorTeam 

Pupil -right- (record solution)

rectangle Application {
   Pupil -- (hand in solution)
   (record solution) -down-> (hand in solution) :next
   (hand in solution) .right.> (notify tutors) : include
    (Analyze solution) -left- TutorTeam
    (hand in solution) -down-> (Analyze solution) :next
    (Share feedback) -- TutorTeam
    Pupil -- (Share feedback) 
    (Analyze solution) -down-> (Share feedback) :next
    (Share feedback) <. (Ask question) :extends
    (Update OLM-P) -- TutorTeam
    Pupil -- (Update OLM-P)
    (Share feedback) -down-> (Update OLM-P) :next
} 

@enduml
```

![](https://www.plantuml.com/plantuml/img/VLBDJeGm4BxtAUO81tW0OynorxZ9hWzGwG0DtHRRgOh6TtU0NLmMTozDslb-9zq4afxYmO0GeTMsaruUe9DbAslSKMyGF9OaRMrG2DB43qNeRTbuPrqCaF0u-g3VCOKAKRqoLGXPalEmZPrcuUcoZtpkaTM5c0QPrtL3sIZXl8BWJ2JjR2h4x0b5rnbTok4TlWN0KJHZMYEj0ctFU3nUYK6ct8VD7lx1mvt5JnfPwra-fikPPntfgWSQ2WGcCQuqKU50XAImqlHVU6veiE9QS-49jtQOWwqbvc2Gx1hfSLvjEZHVAlyjv19wDU39-99mm_O-PwNGmbl4SCp8MBGgJFYNJab2U7vyohOtGow0LogUyYr5ftG__7ysxCj_zXS0)

## Scenario 3: Teachable Tutor

### Display existing rules on access

```
@startuml 

skinparam packageStyle rectangle

actor Tutor

rectangle RuleEditor {
    Tutor - (Access editor)
    (Access editor) .down.> (Render rule repository) :include
    note right of (Render rule repository) 
        Will not be rendered 
        if there are no
        existing rules
    end note
}

@enduml
```
![](https://www.plantuml.com/plantuml/svg/TP112a8n34JtESKiTQ47S26wy08gkAvj_1Ph-sbJLCIxssQX81X8eFDc4kYgYCbIhm54vUBZQBAvOZJsOWRUoICmCbinSGXCPAoaZ7rjauW-0DiQUEDyXqz2AxLWXidQMYu5h72gx4V3tALRd2ynsN9qd96h7XrJwVmnnS976wfZJSSaZVhXB4Yd_ndrzZhu47e8nsxePdPVwa-GSvDWMiVqqVdkY_WuwEAYSilgSNeHhTgZ_Hcz0G00)

### Edit a tutoring rule

```
@startuml 

skinparam packageStyle rectangle

actor Tutor


rectangle RuleEditor {
    Tutor - (Edit rule)
}

@enduml
```

![](https://www.plantuml.com/plantuml/img/FOqn3eGm40Dxly8b5Fo1XW_SyO5LM2544j2oAKud_awWmCKK7alk3nVpaYA1OrtoBYQ9kuHLPltwBofDWqkUem8IV3EEfHB0A_WfKOTfkUKVh7acxDZSBQtg5YVGQvxg5ou0) 

### Save the rule

```
@startuml 

skinparam packageStyle rectangle

actor Tutor


rectangle RuleEditor {
    Tutor - (Save rule)
    (Save rule) .down.> (Parse rule) :include
    (Save rule) <.up. (Show error message) :extends
}

@enduml
```

![](https://www.plantuml.com/plantuml/svg/PK_D2i8m3BxdANAS1_i08hABTt6-G6Z3BEkwahQR8hwxSQ08vX2Ixu-apOMar34WG1vyJ2GqOY8xKCzTkGT6OLieze41o9P9y5Ar0y2Nm7CDV7J-JJu0jLO9Rh7fQDO4fJSh_hEZSTCIpG6R4qd-W3iVRQYE_zHxKvDHv3ejo2AQFdBEUgHw-5OukWnFW5O7_GPU)

### Submit rule

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

![](https://www.plantuml.com/plantuml/svg/VL193i8m3Bpx5JwsX_O1750vS4M8vG6c2LNKD8aIHwX2_9sqL6KHgW-MDPuPBrLWyXmxZG2XLSQHfmuTrIqryiYzbkXbpMGQBG6ePkln55EUweteb561FGqOm4p6GzHoAzH0kWEc66LOO7QCbqun-aJ8nyuNWgMmDrEkCTjPLjSUwND4ZYjbQXs5_ACiVjPPyDwJ3t825nnd_ja9ufSWFSJPC1pMlxK83u1A6f5U2Ky0)

(to be continued)
