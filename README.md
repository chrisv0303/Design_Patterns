## Design Patterns in Java Notes

# Understanding Design Patterns
- Design patterns are solutions to a problem in a context where it is the situation in which the pattern applies. The problem is what you are trying to achieve and any constraints of the context. The solution is what solves the problem in that context.
- Pattern classifications allow thinking at a higher level of abstraction. The Gangs of Four (GoF) patterns can be classified in many ways, but there are two that stand out:
	- Purpose with:
		- Creational - there are 5 creational patterns related to object instantiation providing a way to decouple the code that creates the object from the object itself.
		- Behavioral - there are 11 behavioral patterns concerned with how objects interact and distribute responsibility.
		- Structural - there are 7 structural patterns which describe how classes and objects are composed to create new structures or functionality. 
	- Scope into:
		- Class - class patterns describe how relationships between classes are primarily defined via inheritance. These relationships are established at compile time
		- Object - object patterns describe relationships between objects that are primarily defined by composition. These relationships are created at runtime and are more dynamic and flexible than the ones defined by inheritance.
