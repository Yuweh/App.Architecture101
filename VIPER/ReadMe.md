## VIPER
-----

## What VIPER means?
VIPER is a backronym for View, Interactor, Presenter, Entity and Router. It’s basically an approach that implements the Single Responsibility Principle to create a cleaner and more modular structure for your iOS project. 

-----

### PARTS

View - The VIPER View in an iOS application is a UIViewController that contains a sub view, which can be either implemented programmatically or using the interfacer builder (IB).

 Its sole responsibility is to display what the Presenter tells it to, and handle the user interactions with the screen. When the user triggers any event that requires processing, the View simply delegates it to the Presenter and awaits for a response telling it what should be displayed next.


Interactor — contains business logic related to the data (Entities) or networking, like creating new instances of entities or fetching them from the server. For those purposes you’ll use some Services and Managers which are not considered as a part of VIPER module but rather an external dependency.

//The Interactor contains all the business logic related to the entities and should be completely independent of the user interface (UI).
In our Article Visualization app, one use case example is to fetch the list of articles from the server. It’s the Interactor‘s responsibility to make the requests, handle the responses and convert them to an Entity which, in this case, is an Article object.

Once the Interactor finishes running some task, it notifies the Presenterabout the result obtained. One important thing to have in mind is that the data sent to the Presenter should not implement any business logic, so the data provided by the Interactor should be clean and ready to use.


Presenter — contains the UI related (but UIKit independent) business logic, invokes methods on the Interactor. // The Presenter works like a bridge between the main parts of a VIPER module. On one way, it receives input events coming from the View and reacts to them by requesting data to the Interactor. On the other way, it receives the data structures coming from the Interactor, applies view logic over this data to prepare the content, and finally tells the View what to display.


Entities — your plain data objects, not the data access layer, because that is a responsibility of the Interactor. //The Entity is probably the simplest element inside a VIPER structure. It encapsulates different types of data, and usually is treated as a payload among the other VIPER components. One important thing to notice is that the Entityis different from the Data Access Layer, which should be handled by the Interactor.


Router — responsible for the segues between the VIPER modules. // the Router, which is responsible for the navigation logic between modules, and how they should happen (e.g. defining an animation for presenting a screen, or how the transition between two screens should be done). It receives input commands from the Presenters to say what screen it should route to. Also, the Router should be responsible for passing data from one screen to the other.
The Router should implement a protocol that defines all the navigation possibilities for a specific module. That’s a good because it enables a quick overview of all the paths an app can take by only looking at a Router‘s protocol.


Because of a limitation from the iOS framework, only ViewControllers can perform a transition between screens, so a Router must contain a reference to the module’s controller, or any of its children.


Referrences:

Bohdan Orlov - https://medium.com/ios-os-x-development/ios-architecture-patterns-ecba4c38de52

Pedro Henrique Peralta -  https://cheesecakelabs.com/blog/ios-project-architecture-using-viper/

----

What are the benefits of VIPER Architecture?

What are the downside of VIPER Architecture?
