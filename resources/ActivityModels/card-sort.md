# Card sort

![](https://www.plantuml.com/plantuml/img/RLR1ZXj543qpNr62GvBLhXq9k2I7JGWAv0295A88XJsqPyep7Szq3zqzTaoqKZw22nByNBw4zxh7tlL2f8tiSK_LgrUlNlMJc4n8qz1N-KDLnOrrembca8_L5xjWnhUsIPry_V1X9VZtj4vsQzF-ErDlsk0drppplG_orSzcQzxxjvrDMbrNrVAUxFqaEzltubGRILwcg3BsnZ7TelR3uLdgRCIXdSIzI-Q3t5lczpCWYPgcKNQTxJN_K9MFztyqMyqfng30YmmcIQyc9c2LseGc2d1vrrkd4hjynFcaKNvpjKSYwwnhfR6n3fg0p6gD7_rQh5lxC9XalGCsX3qKi4AW5AOwJGXsYJZltdKfZO-MozRxjbSMzH7vDZniPgQknJHukrF9ltGQzEfA7WXglk_yWwfwz0OS62Vdjb4ZhJeD9JVW3mgWlGo-qLvCRrl79-V7u4m4-2QHHMMSTT8rVesFgqfTCvErryX4lm14z5EebMLcse-1yBbK4rcE6JGca026MDIIV5v47zBoMDzDe6ECHYCGNilTrw-kAkCQiQde8PaDW6Rne5SNttmhE3YXC-U8C08r-vAvLt7JCAmqC0swd6njHmWeBghgxEpbwhtMYJ-zwit-xAnw1fH2b0p0uY0EWWDCwAoHTT3V9_3NxsMrFscp2JML2zw4I4iX6Y8BRGs0XFpys7syF4uuZ0Z8iZN1Akedo2cCFcfSo0j45HG_83nLZX_hM_ZEJ_ANE3jTHQ0WT4G71SXE4hAQppE2b5jOAkoq7-EX_JN-Qprm553ER6qxrpQ_vhSG5kW_reew5a9D39ewtyZEXqsKznD6o4I0mLc6oWcOB_PGQ0cFeOkK9XC06T7Z9RUNqLk7DbFb9mLoXE9XXe2VymfSFhJ6sJ_mpP8kn8ns1SNkp1uj9ZOpZhsjIwAx7AAKh125bcP-R26RKilLH3lOteG-Jyeh7zF5cp4VDEir301D6v21EfKJzTGOoCQkrsZyEj2gydGLef2gypi5dGjvRaF4F1wxb26L6UwHz6XEBA_P6bShSFQ8ChNTYQ9XKNxg6_A3Dn6-EPrjYndOkTa8PvGBUQsmikPkVX8vs8jHmRv3cuHvw0gvSfQscYV2n2nIbuBliq3mPfQ9w0SDjOMICRFm_y85Ovs01aJGsE1XIXhG8GEvjuGpBE10z5i9jkrIjLo-Je4QtSiIDlxqm06HP-PVewRi7EYS-_pfhoI92gJ54z8UTeN8_7gmuutpEp4hZr5XnUcETvyV3OU38W5HK1VpbTGe9NXOVloFkN1sipjIZyeum1FXmkGsvnlLZpq3WSjRAHVoqg7hD67ECwGvUzT1LdTOlNs4stIC1J0Ks-Bf3QlZg2OiigNd9PON9ByaFzgwB4OyEJfnp4PNvvK9FyygbLScHd3_WzrcHPMCeZRRMpQMRbglUwN_rHiETO1U_82Ai2LJiAk9SpklL11MDaqPF5DdAaqVVHvpxFcDe6-HWxkGxnLhrgxqn8dcwIyEKNTufAxLELxSP1cLLGDft4ZSqXTdkl9-RfcoLTO1ZbvmjUcU7GI4w3cqyqAON8qhGiYRrSQORJYV7SoUOvcxbXtcu7iS9bvDl5CsjzPolkFjenneRhWa5RTWEuevVvbtof610J2VEgZ139GHT-ZSZO73Wl6iliIj8B1KpIkC8_4FH-fagEYGr2J-k8DkN7BMs-TFVrgKFEMDQdYrQszr7X03kyGdM0X3B5Otm2NvMxbCSHK6Gqy69NXwSEox_KWxVti7nQdkw2wVF_qzSA6GC5IGcS0pnvsCj_XumUU_OgvB4w2VcSGRc5a0jv9niMkZi1xGFq_-JV9pleBhH9fzSukBKuEfE9cVwf6SdVqC0zb1GPUuFE3g2iWboOwiql9iFVMP38mERWHo5DwblANoRCn0uPxpbOfRulzlajW0CAzm53zlmfUFgpic-NBaOVZKOPHfbfcSB0nOTSGI3d1lzl9u_nnDqslALxMFvVErt3p3VPDB--J2TqB6exEpvvvRfvoPHl3nKxvpbdUu9GQRzxNuR1S0KkkObWSBnHQbEd7h6wid28mh_hy0)

```
@startuml
start

skinparam {
	wrapWidth 300
    ActivityBackgroundColor #NavajoWhite
}

/' you will need to use plantuml.com to use this new syntax '/

/' start setup while '/


while (Have you prepared at least 30 cards or online shared notes \ncontaining discrete pieces of information that need to be structured? \n[[http://google.com{link to activity} add the link here]] ) is (no)

:Use an ,idea generation or mental model alignment, activity to create these aftefacts;

endwhile (yes)

:The source of this activity is [[https://gamestorming.com/card-sort/{link to source of activity design} gamestorming.com]]
and it will take around 30-45 minutes, depending on the nummber of participants.

**Object of Play**
Card sorting is a practice used frequently by information architects and designers to gather and structure inputs for a variety of purposes. In a common use of card sorting, information for a website is put onto the cards, and the sorting helps create categories for navigation and the overall architecture. The method works just as well for creating slides for presentations, or at any point where information needs to be sorted and organized in a sensible way.

The applications of card sorting are numerous, and in use it works similarly to Post-Up and affinity mapping. Card sorting can differ from these methods, however. First, the cards are generally prepared in advance, although participants should be allowed to create their own while sorting. Second, the cards are a semi-permanent artifact and can be used as a control over several exercises with different participants to find patterns among them.;

note right
//Strategy //

Although the Card Sort game won’t tell you everything you need to know about a set of information, it will help reveal the thought process of participants. In this sense, it’s more about people than information. Only after a number of sorting exercises with a number of groups will larger patterns appear.

end note

/' end topic '/


/' activity sequence '/
://First Pass//
Give the group either the shuffled deck or randomly distributed online artefacts, and access also to blank versions. Describe the overall organization challenge, and ask them to sort the cards into groups that go together.

If they think something is unclear or missing, they may alter a card or create a new one. Once they have created the groups, ask them to name them and describe them.

An example of a group might be
"User interaction”.;



note right

There are variations of sorting—including asking the group to rank the items from most to least desirable or to organize the cards into two categories such as “must have” and “nice to have.” You may also ask the group to sort cards into a predefined set of categories, to test their validity.

end note


: **Now what?**
Which cards were difficult to assign to groups? What is the role of these pieces of information in your overall plan?;


note right
//Optional activity//

You might consider using [[http://padlet.com/{padlet} padlet.com]] for this activity.

end note

:**Follow this up**
Model this as a mind or other concept/process map.;

stop
@enduml
```
