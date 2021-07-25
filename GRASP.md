#Design 

[[OOP]] [[Software design]]


## General Responsibility Assignment Software Patterns

Nine fundamental principles in object oriented design and responsibility assignment.


### Information expert
Problem: What is a basic principle by which to assign responsibilities to objects?
Solution: Assign responsibility to the class that has the information needed to fulfill it.

This pattern used in situations when needed to decide where to delegate such responsibilities as method, compute fields and so on


### Creator 
The creation of objects is the most common activities in an object-oriented system. Which class is responsible for creating objects is a fundamental property of the relationship between objects of particular classes.
Problem: Who creates object A?
Solution: In general, Assign class B the responsibility to create object A if one, or preferably more, of the following apply:
- Instances of B contain or compositely aggregate instances of A
- Instances of B record instances of A
- Instances of B closely use instances of A
-  Instances of B have the initializing information for instances of A and pass it on creation


### Controller
The controller pattern assigns the responsibility of dealing with system events to a non-UI class that represents the overall system or a use case scenario.

Problem: Who should be responsible for handling an input system event?
Solution: A use case controller should be used to deal with all system events of a use case, and may be used for more than one use case. For instance, for the use cases Create User and Delete User, one can have a single class called UserController, instead of two separate use case controllers.


### Indirection
The indirection pattern supports low coupling and reuses potential between two elements by assigning the responsibility of mediation between them to an intermediate object. An example of this is the introduction of a controller component for mediation between data (model) and its representation (view) in the model-view control pattern. This ensures that coupling between them remains low.

Problem: Where to assign responsibility, to avoid direct coupling between two (or more) things? How to de-couple objects so that low coupling is supported and reuse potential remains higher?
Solution: Assign the responsibility to an intermediate object to mediate between other components or services so that they are not directly coupled.
The intermediary creates an indirection between the other components.


### Low coupling
Coupling is a measure of strongly one element is connected to, has knowledge of, or relies on other element. Low coupling is an evaluative pattern that  dictates how to assign responsibilities for the following benefits:
- lower dependency between the classes
- change in one class having a lower impact on other classes
- higher reuse potential


### High cohesion
High cohesion is an evaluative pattern that attempts to keep objects appropriately focused, manageable and understandable. High cohesion is generally used in support of low coupling. High cohesion means that the responsibilities of a given element are strongly related and highly focused. Breaking programs into classes and subsystems is an example of activities that increase the cohesive properties of a system. Alternatively, low cohesion is a situation in which a given element has too many unrelated responsibilities. Elements with low cohesion often suffer from being hard to comprehend, reuse, maintain and change.


### Polymorphism 
According to the polymorphism principle, responsibility for defining the variation of behaviors based on type is assigned to the type for which this variation happens. This is achieved using polymorphic operations. The user of the type should use polymorphic operations instead of explicit branching based on type.

Problem: How to handle alternatives based on type? How to create pluggable software components?
Solution: When related alternatives or behaviors vary by type (class), assign responsibility for the behavior—using polymorphic operations—to the types for which the behavior varies. (Polymorphism has several related meanings. In this context, it means "giving the same name to services in different objects".)


### Protected variations 
The protected variations pattern protects elements from the variations on other elements (objects, systems, subsystems) by wrapping the focus of instability with an interface and using polymorphism to create various implementations of this interface.

Problem: How to design objects, subsystems, and systems so that the variations or instability in these elements does not have an undesirable impact on other elements?
Solution: Identify points of predicted variation or instability; assign responsibilities to create a stable interface around them.



### Pure fabrication
A pure fabrication is a class that does not represent a concept in the problem domain, specially made up to achieve low coupling, high cohesion, and the reuse potential thereof derived (when a solution presented by the information expert pattern does not). This kind of class is called a "service" in domain-driven design.
