# App.Architecture101
Intro To App Architecture
---------

STATUS:
Already using MVC on my projects
Will try to rebuild an App with VIPER and MVVM


---------
## iOS APP Architectures:

Models — responsible for the domain data or a data access layer which manipulates the data, think of ‘Person’ or ‘PersonDataProvider’ classes.
Views — responsible for the presentation layer (GUI), for iOS environment think of everything starting with ‘UI’ prefix.
Controller/Presenter/ViewModel — the glue or the mediator between the Model and the View, in general responsible for altering the Model by reacting to the user’s actions performed on the View and updating the View with changes from the Model.

---------
## MVC
---------
- most used framework in iOS
- bigger apps could populate VC and may cause Massive VC, making it problematic to test

Model 
View 
Controller

---------
## MVP
---------

Model 
View 
Presenter


---------
## MVVM
---------

Model
View
View Model
(View Controller still Present)


---------
## VIPER 
---------
- based from Clean Architecture
- used Singular Responsiblity makes it more equally distributed and testable

View
Inspector
Presentor


---------
Referrences:
Bohdan Orlov -
https://medium.com/ios-os-x-development/ios-architecture-patterns-ecba4c38de52

Entity
Router
