# Design and collaboration processes

##Workflow Model 

![Submit Rule](https://www.plantuml.com/plantuml/img/ZLHBQzmm4BxxLyoj44XxRqF8qX889PTkeUUnDBQ7rMChZTRDl-z8ZfDDkxJsmI1fvfllOVak2oOftdMTi3W2k8QT4JwnFC4NnZ6XXwvBT2IKhllu68F5fqzTY4BWQ90EuAQ_lKV3ZWKbffiF_ItexbKYpy5cyEHxIXdYyAQIOu1lCGkrZgNXn3HdUCYvKAux9kbKoe31GZcwY0eNw9Se9Wc7yPqUZQICQd4s4zcY4fuFWGFiREm9FiSGo4Y3uQ3IQ2MbVU_rMKHy3N5sP4U2HmoAkqXPEQoeAghKjOscU0goGYWDgAweIT-L_XQN9fM_Y1lMazT16wWbCZ6f9PbohdPM9C63OjJ1P-AkdajVHCG_h6arjNNfR4YeeAE2cXeLzcgi6kTRBXg6nUeYrloWJnZCTEx03xBXiWSxvrRpcuOvfaEbiqoZAY0VDkKoaJa0js-byJqMXKxqKzUItyGnbNIHonuzDIpCyCBulFC-yV_wLl3pjZrAILl43npGSQQ_rVzRTjwaUr-stDMQvn2TYxEcMfDeAOCjr6vWzBu4DZNjEcpIrtKyQUWpoxHSnWkOhooMFySyiTF5dUxhl-Ot)

@startuml

title  - Activity Diagram 

repeat

:Monday;
note left
  <b>Facilitator</b> 
  *reminds members of <b>Facilitation Roster</b>
  *reviews Issues
  *creates and uploads next meeting's agenda
  *schedule meeting in Adobe Connect and invite members
  ....
  <b>Knowledge Manager</b> creates meeting minutes document
  ....
end note

:Tuesday;
note left
  <b>Facilitator</b> hosts and facilitates meeting
  ....
  <b>Knowledge Manager</b> records session and takes notes
  ....
  * record meeting on Adobe Connect
  * take notes and assign actionable items
  * update master branch
end note

:Wednesday;
note left
  <b>All members</b> work on assigned tasks
  ....
  <b>Knowledge Manager</b> check issues and pull requests
end note

:Thursday;
note left
  <b>Same</b> as Wednesday
end note

:Friday;
note left
  <b>Same</b> as Thursday
end note

:Saturday;
note left
  <b>All members</b> finalise assigned tasks
  <b>Knowledge Manager</b> checks issues and pull requests
end note

:Sunday;
note left
  <b>Facilitator</b>
  *follow up on items due
  *communicate and hand-over with next <b>Facilitator</b>
end note

repeatwhile

@enduml

> Provide details here of your team workflows. Use [activity diagrams](https://github.sydney.edu.au/crli/EDPC5022-2019/wiki/Sequence-Activity-Interaction-diagrams) or such as you see fit. Mainly maintained by the *Knowledge Manager*. 
