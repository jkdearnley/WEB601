# Week 13
We looked at Flux, created by facebook,and how Redux 
uses Flux to manage the state of an application.

Flux was created to help with the problem that the classic 
Model View Controller (MVC) architecture pattern has managing 
application state in complex applications.

* Flux runs in this flow:
* View calls an action
* Action calls a Dispatch
* Action is dispatched to store
* Store notifies the view