##Day 2
###thoughts:
- as soon as something starts changing, you can expect it will change more
- want to do subtle refactors that bring you to safe place to refactor
- don't give up on immutability because you're afraid of something
- what should the default value of an arg be?
	- You could start with nil to see if something better arises. You may soon realize that nil is the default value of everything in ruby. You could then try a symbol with a really obvious meaning. Nil can mean a million things which means it can mean anything. this helps when there are 6 other places in your app where you need to make changes too. If it is the default (the caller doesn't pass an argument) and someone uses it unexpectedly it will be obvious.
- Kent Beck- "make the change easy then make the easy change" (this may be hard to do)
- privacy can be a code smell
- if you recognize the code smells you can refactor
- only have private methods that are tested public methods that have been factored to private methods, maybe private methods are something that could be better as their own class?
- some things are very high in complexity but not very high in churn
- you can make people more fond of you if you ask them a favor.


###methods:
- Replace conditionals with polymorphism. We started with a case statement that switched on number and returned a big string. Now we have case statement that switches on number and selects the correct object. This might be the most interesting problem in OO, selecting the correct Object.
- sending an argument to a method and then inspecting it is not OO, it's procedural. The name of the refactoring for primitive obsession is to extract a new class.
- recipe to extract class from M. Fowler's book:
	1. initialize with attr_reader of the variable that gets passed around
	2. copy all of the methods that use the variable (should be under private) into the new class


###terms:
- SOLID
	- S: single responsibility principle. Sometimes "small" and "one thing"
		- "everything in a class should be cohesive around its responsibilities" - Rebecca Wirfs-Bock
		- How do you know a class has a lot of responsibilities?
			- it has high churn rate (it is getting checked into version control every day)
			- if a class has a lot of public methods and those classes don't have a lot of shared public and private methods, that could be a sign
		- writing smaller objects means you don't have to understand the entire app to make a change
		- how small to go? One size larger than you are comfortable with. Leave a bit of smell around

	- O: Open/Close
	- L: Liskov Principle- Trust, Don't lie to me
		- all instances of subtypes should behave like their supertypes
	- I: Interface segregation principle
		- shouldn't matter if the class I depend on changes its requirement
	- D: Dependency Inversion- should depend on abstractions, not concrete objects

 
###google:
- Rebecca Wirfs-Bock
 
###ruby:
- flog gem

###tools:
- 

###homework
- brown bags-bring code smells and explain them
- read



###what are these random thoughts?!!?

greater than and less than are not the same as checking for equality!

data clump
- don't want receiver to make changes around data, want to separate this into its own class

###ideas for work
- code and tell, devs bring code and talk about existing code and when and how they are making new patterns









