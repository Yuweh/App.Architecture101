# App.Architecture101
[![IDE](https://img.shields.io/badge/Xcode-9-blue.svg)](https://developer.apple.com/xcode/)
[![Language](https://img.shields.io/badge/swift-4-orange.svg)](https://swift.org)
[![Platform](https://img.shields.io/badge/platform-iOS%2011-green.svg)](https://developer.apple.com/ios/)

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
- most used framework in iOS
- bigger apps could populate VC and may cause Massive VC, making it problematic to test

Model 

View 

Controller

---------
## MVP

Model 

View 

Presenter


---------
## MVVM

Model

View

View Model

(View Controller still Present)


---------
## VIPER 

## What VIPER means?
VIPER is a backronym for View, Interactor, Presenter, Entity and Router. It’s basically an approach that implements the Single Responsibility Principle to create a cleaner and more modular structure for your iOS project. 

The main parts of VIPER are:


View: displays what it is told to by the Presenter and relays user input back to the Presenter.


Interactor: contains the business logic as specified by a use case.


Presenter: contains view logic for preparing content for display (as received from the Interactor) and for reacting to user 
inputs (by requesting new data from the Interactor).


Entity: contains basic model objects used by the Interactor.


Routing: contains navigation logic for describing which screens are shown in which order.

---------
Referrences:

Bohdan Orlov -
https://medium.com/ios-os-x-development/ios-architecture-patterns-ecba4c38de52

Pedro Henrique Peralta -  https://cheesecakelabs.com/blog/ios-project-architecture-using-viper/

Entity
Router
