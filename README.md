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

## Getting to know the Structural Design Patterns
