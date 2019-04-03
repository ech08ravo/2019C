# Forced ranking

![](https://www.plantuml.com/plantuml/img/hLTDZzH643t7lw8L3i1gc1c2aiFcmCS6aZsGe00Y4jf3swwncxMxdUxsp5e8YH-HO_Bd-2LvLMrxPjWbIgGWBPgn-wFgrNklQXw5g7tisoQJ3raMBetjjDUjUfzzjVEwUsFAMAi7wtMcyEzn4StMnE69BYuhxtfRdhd6UNLhlNxs66i-PDdgjXfShtQcQPGbAbLqgW-akaPRlcbPk5PX2t-taQwYF1WNnTe4xDgfCDYehzJjbHmemQb0iU_KhZODoOlqwSvFUajofLQD2L6v3HzZgy27Ucql7wgtR-iOkzFLgdAkQeXlVDyOUyahz9ZI1wLB15kJaZSrURguK7SL0hfZtTqiEtsD0BKwStPBlY8RvwryJE59HtwFA3a4rqNZRE1mYte68WSEtZXleWbKVfzbPCinZO72tPjo6iyhi8UyqUE1CyI2MigJWs__tsH_CDTo3Jskrq7bNXkxuqnijL0RrpHkXoJp0TkURdNJQmRW-hxIHRLrl8i38fGsHzbg2MPEyZ2z6r0wVON5mVM-eB7SONyHFYS80cEWMrpXV8lx68dLWs_NgncE_H7pxfA2gUm7zVd6YujCsrAPcEAA-XBuY08WZdlVhHKMzf720YTqY9VpG_gSbUtRDYVFrq1QqHIcWnImabyUKtMX-993A9PPTdBoI_wE2g71YqOF9oVPcvhidabI0QrOa9rgzJ3JJLUUYCC0ZR2eeONSWfUJKd196vRgcGCEfRoKm56I2dGE4aew5yUrd7HfDXjJz4r4eWNk1ibJrAHHO3wFAp1Uuwa13RP2KJxAuJ-F-rvnnRXeLfcsSpu24AYSEcKiNyD1pCTp0X8deaO01leBiIM1CE-H68KmWq5ZD1l8iVV805RZwVVUU98jdpx-iMEwWzT0fMX8-yMX9XCoua9KKha4-wo3iBsfwfYjLY-Z1p3Le5Pme3CMFSUg8O0Z1BaA-I5O6xQye-f32s3J69iWFII49QXxHG_HXO3S96wbSyTF9ZyO2tVESDb15JgGC2hXYf0JzK1WtQZMbPHCYNoI9OSZTSKcmODZmKRImG0PvavPZgZZ2uCY7qBqIRaLSIaJmren280U-ewBkLG_KXHSEd9TGpDti8LjPP_LGbMzAPDjIDepxnSS3QU0PS17TSvOIVmOwAMO0-TBqYduItITAQH3y9Ez0G5fieNq3ZZ3op74rnqg-UAWChDwQZRXk7EZHa-PhRszIK3NL2luJbnWMrwg9rHeDkjhHBayajcxlgneFBLeNA1cM1mV7MhNDoMpIuSHD7peN0WcXzspbXLTwRPZkKDEqqsp8ZWs3SwxiY_YPuUtJ7C--zF7FvyxLi8ipwFzQ0zU_RRyzF4lfg0S0GOo82MarQ02kF56SVxpTHqAYOA3ixXOi-UnK8NA61NKW6o_PasYWB-cl52zf-my1-AIb1Ee2KXkIe5zdQCoh29uCYmPt3SnjPxsE5dniPnu_QtxAUX0XKEPRre8_6zzatmdECOdrel9yb2WQnlsRE0LKu50UC2G-B5WPAsRY03cUIg8dHGi1ZexOkGOYR4nHX6nnbyBkp6ikj90Oyb1MS_JFQdBZuqqmGWPeva3oNDkfl_seCNe6Jdi-7066OCEn8Da1865CT8Uni8xEpSwgz1SSz0aOLmuyK876c5XEptV68ka9yshSxdto-RA1mX2g9Rd4u2VixI_NcacGKHUoOT72ZkxOSfM_uMEaaWgicun3uWhq8P9yDdgOAuGZurrODqSDnOHaGcY8i5rDudy2DtHa7Uce5Da13C3jSVGE8xfKRf_gHut4MvHrMDLfJF0rppxLujRzXFAEA3CZf_JsCF5G-0ww2FDlUHHORHEgNL9GASXMq58F4ZD3JGrhFlhgLL9pzSy9ePhnJfqlSEPWOkchKmD8bK-COSEMvbIW2vwLoCZcdeoJ8F3GTUGMBP6d37DGPl6TAge-VS4I0FnHCeT05aSnoH3dZG0K6TgYg3BB5RagJ4PUxbYUT248Acd-5sJwlvSerzUGLXdqy-3LfvykNC09s0q7AfXLa_ociB3we_tW4i7Ct8QuDN9oSzkXmnrV8Y9KT2_QSxHyw05keX9IikSPou949blF4_4x6yydBCZeOCKOwlSSppgIjg0uVx3FLxcZQNY435FTzaZ1Ce_EFy6)

```
@startuml
start

skinparam {
	wrapWidth 300
    ActivityBackgroundColor #00FA00
}

/' you will need to use plantuml.com or planntext.com to use this new syntax '/

/' start setup while '/

while (Have you a list of things to rank? [[http://google.com{link to activity} add the link here]] ) is (no)

:Use a Convergent activity to create a set of options which need to be prioritised;

endwhile (yes)

while (Have you a set of criteria which you will use to rank them? [[http://google.com{link to activity} add the link here]] ) is (no)

:Use a Divergent activity such as brainwriting, followed by a Evaluation activity such as dot voting to establish the criteria you will use;

endwhile (yes)

:The source of this activity is [[https://gamestorming.com/350/{link to source of activity design} gamestorming.com]]
and it will take around 30-60 minutes, depending on the nummber of participants, the things to rank, and the criteria.

**Object of Play**
When prioritising, a group may need to agree on a single, ranked list of items. Forced ranking obligates the group to make difficult decisions, and each item is ranked relative to the others. This is an important step in making decisions on items like investments, business priorities, and features or requirements—wherever a clear, prioritised list is needed.;

note right
//Strategy //

Creating a forced ranking may be difficult for participants, as it requires they make clear-cut assessments about a set of items. In many cases, this is not the normal mode of operation for groups, where it is easier to add items to lists to string together agreement and support. Getting people to make these assessments, guided by clear criteria, is the entire point of forced ranking.

end note

/' end topic '/


/' activity sequence '/
://Setting Up//
Participants need to have two things: an unranked list of items and the criteria for ranking them. Because forced ranking makes the group judge items closely, the criteria should be as clear as possible. For example, in ranking features for a product, the criteria might be “Most important features for User X.” In the case of developing business priorities, the criteria might be “Most potential impact over the next year".;

://Ranking//
Each participant ranks the items by assigning it a number, with the most important item being #1, the second most important item as #2, and so forth, to the least important item. Because the ranking is “forced,” no items can receive equal weight.;

while (there are multiple dimensions to a ranking) is (yes)

://Rank again//
If there are multiple dimensions to a ranking, it is best to rank the items separately for each criterion, and then combine the scores to determine the final ranking. It is difficult for participants to weigh more than one criterion at a time, as in the confusing “Most potential impact over the next year and least amount of effort over the next six months.”;

note right
In this case, it would be best to rank items twice: once by impact and once by effort. Although there is no hard limit on the number of items to be ranked, in a small-group setting the ideal length of a list is about 10 items. This allows participants to judge items relative to one another without becoming overwhelming. By making the entire list visible on a flip chart or whiteboard, participants will have an easier time ranking a larger list.
end note

://Enter the Matrix//
Create a matrix of items and the criteria. Tally the scores for each item across the criteria.;


endwhile (no)

: **Now what?**
This prioritised list is a decision. Assign action items and timeframes so you can proceed to the next stage of implementation. ;


stop
@enduml
```
