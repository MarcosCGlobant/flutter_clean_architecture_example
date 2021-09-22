# clean_structure_example

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

## Folders Tree Explanation

### Core

#### Parameter

What’s the use of this? don’t forget that we’re trying to write a clean code so later on when we need to pass parameters to a function/method to get the articles from the REST API we pass this class, because a clean function/method should have 3 or less parameters, otherwise we create a class like this and pass it as a parameter to that function/method.

### Domain

#### Entity

Entities are the internal representation of the app we’re building.

#### Repository

Interfaces for the repositories of the services.

#### UseCase

##### Callable class

Callable classes are those classes that contains implementations of a method called “call” and this “call” method itself responsible for making the instance a callable instead of calling method belongs to that instance. Here’s an example.

##### What's an UseCase?

This is the representation of our Use Cases, and this abstracted class takes a type T and params P.. The type is what the “call” method will return, and the params is the parameters that the “call” may require (can be set to void if no params are required).

##### UseCase

Interfaces for the useCases of the repositories.

##### Implementation

Implementations of the useCases interfaces.

### Data

#### Model

This knows about the object structure defined in domain, and maps the information from the repository.

#### DataSource/Remote

This is where we define the service implementation of the app.

#### DataSource/Local

This where we define the database implementation of the app.

#### Repositories 

Implementations of the repositories interfaces from domain.

### Presentation

#### Bloc 

This is where the business logic of the app handles the information received.

#### View

This are the screens of the app, that show the data recovered.

#### Widget

Abstraction of elements used on the View/Screens.
