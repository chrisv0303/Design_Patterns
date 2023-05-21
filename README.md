# Design Patterns in Java Notes

## Understanding Design Patterns
- Design patterns are solutions to a problem in a context where it is the situation in which the pattern applies. The problem is what you are trying to achieve and any constraints of the context. The solution is what solves the problem in that context.
- Pattern classifications allow thinking at a higher level of abstraction. The Gangs of Four (GoF) patterns can be classified in many ways, but there are two that stand out:
	- Purpose with:
		- Creational - there are 5 creational patterns related to object instantiation providing a way to decouple the code that creates the object from the object itself.
		- Behavioral - there are 11 behavioral patterns concerned with how objects interact and distribute responsibility.
		- Structural - there are 7 structural patterns which describe how classes and objects are composed to create new structures or functionality. 
	- Scope into:
		- Class - class patterns describe how relationships between classes are primarily defined via inheritance. These relationships are established at compile time
		- Object - object patterns describe relationships between objects that are primarily defined by composition. These relationships are created at runtime and are more dynamic and flexible than the ones defined by inheritance.

## Why Are Design Patterns Important?
- Patterns capture expert knowledge to create well-designed software. To understand well-designed software, software that is flexible, easy to maintain, and reuseable, so it can change without too much rework. The benefits of using design patterns are:
	- Patterns are about reusability
	- Find the appropriate design
		- Find classes and interfaces
		- Determining object granularity
	- Communication and documentation 
		- Shared vocabulary
		- Precise and complete
- Strategy Pattern - defines a family of algorithms, encapsulates each one, and makes them interchangeable. Strategy lets the algorithm vary independently from clients that use it. It allows us to:
	- Change a part of a system independently of all other parts
	- Swap out behavior at run-time
- The strategy pattern is a mix of:
	- Encapsulating what changes
	- Favoring composition over inheritance
	- Open-close principle
	- Programming to interfaces

## Getting to Know the Behavioral Design Patterns
- Behavioral patterns describe how objects or classes should communicate, as well as their responsibilities. The behavioral patterns we should know are:
	- Strategy and State - a strategy is a synonym for a plan or an approach for doing something. It can be compared to an algorithm with something that produces an output from an input. Multiple strategies have the same inputs and outputs but have different implementations of performing an operation to produce the same output. Although state patterns are similar to strategy patterns, its intention is different. An object's state is the combination of the values of its attributes. 
	- Command - the command pattern encapsulates method invocations. To encapsulate commands or method invocations, you define a super type, which can be an interface or abstract class exposing one method usually called execute, and for each particular command you want to support, you define a subclass that overrides the execute method in a particular way. 
	- Observer - the observer pattern is about notifying one or more objects when the state of another object changes. Just as other patterns do, the observer pattern creates a hierarchy for the objects that need to be notified. The observer pattern can also create a hierarchy for subjects so we can reuse and change subjects and observers independently of each other. To add new observers at any time, the only thing the subject needs to know about an observer is that it implements the observer interface. A concrete observer can have a reference to its subject in case it needs to pull out some state from it. 
	- Template method - the template method is one of the two behavioral patterns that don't use object composition. It defines the steps of an algorithm allowing subclasses to provide the implementation for one or more steps. It is intended to implement an algorithm leaving the definition of some operations or steps to a concrete subclass. Each concrete subclass must provide an implementation of the undefined steps of the template method's algorithm.

## Getting to Know the Creational Design Patterns
- Creational patterns describe how to abstract the process of creating an object, hiding how objects are created and put together when exposing only their interface. This gives a lot of flexibility in what gets created, when it's created, who created it, and how it gets created. The creational patterns we should know are:
	- Singleton - the singleton pattern is one of the most simple patterns, and at the same time, the hardest to get it right. The intention of this pattern is to ensure a class only has one instance, providing a global point of access to it. The key to the singleton pattern is restricting the access of who can call the constructor of a class. 
	- Factory and Abstract Factory - the factory and abstract factory patterns are about delegating the creation of one or more objects to a special class called factory. There are three types of factories:
		- Simple factory - too simple to be considered a pattern, but leads us to the factory method. We pass the argument of a method, an identifier of the class we want to create so the method can create more than one object.
		- Factory method - a hierarchy of factory classes by defining a supertype. They don't only have a method to create objects, they also have methods to configure objects. If we place a method in the parent class, so the subclasses only have to implement the create method, factory method becomes a specialization of the template method pattern.
		- Abstract factory - the abstract factory pattern can be an extended version of the factory method. Instead of creating a single hierarchy of objects, abstract factory is used to create a family of related objects. If the factory method has one abstract create method that is implemented by each concrete factory, the abstract factory has one method for each abstract product.
	- Builder - the builder pattern offers a solution to the problem of constructing classes with many attributes. The objective of this pattern is to seperate the construction of an object from each representation so that the same construction process can create different representations. A popular way to implement this pattern is by using method chaining, where the build methods in the concrete builder return an instance of the concrete builder itself represented by the 'this' keyword.

## Getting to know the Structural Design Patterns
