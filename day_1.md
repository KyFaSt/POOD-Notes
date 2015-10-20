## Day 1
###thoughts:
- Flow is good for when you’re doing something you already know. Flow is not good for when you are learning—remember for code retreat!
- how much of the code you work on is greenfield and how much is editing existing code? You cannot refactor without tests, you cannot do OO without refactoring. Code is often written once and read many many times
- Martin Fowler- refactoring is altering existing code without altering its behavior. Oftentimes we say refactor but we mean rewriting
- programmers sometime equate terseness with cleverness and we want so badly to be clever. quit picking on everyone for being extremely clear
- distraction is what kills you
- you can make it easier to tell how things are different by making them more alike
- if there is a non-recursive solution, you should use it
- abstractions increase re-usability but decrease readability
- when the future cost is similar to the present cost, you should wait to make the change
- the worst code in your app is the code that's most important. It is usually a large conditional. It's usually replicated in a lot of places in your app. It probably means you are missing an object.
- don't skip the easy problems to work on the hard ones
- code smell is a general term but a code smell is actually very specific (from M. Fowler's refactoring)	

###methods:
- the inebriation test- you’re on call, they call you about a bug in some code you did not write. You need to be able to look at code immediately and understand what it does
- If you solve the easy problems first, you will find that the hard problems become easier.
- Practicing by making each test pass one by one, we practice as if we’re writing the test ourselves
- practicing not changing the sending and receiver at once replicates working in large code bases where you cannot do this.
- when you have an abstraction that claims to have single responsibility but actually has conditionals, it is the wrong abstraction. It is very difficult to move forward from this, it is the code that makes everyone sad. "Moving on from the wrong abstraction is hard. Not doing it is like staying in a bad movie because you paid for it"
  1. take that method and put it back in each of the places it is called
  2. delete all the code that is not used in each caller. Then you'll see what the abstraction _should_ be
  	-- this is called inline refactoring (from Martin Fowler: Refactoring, Improving the Design of Existing Code) 

###terms:
- shameless green- maximize for readability, do not care about changeability
- cumulative song
- Open/Close (from SOLID)
- no-op land
- L from SOLID (Barbara) Liskov Substitution - subtypes should be subsitutable for their supertypes

###questions:
- when you dry methods out right away, you can get this inside-out pattern***ask about this
- don’t chase red, ask for explanation

###google:
 - cumulative songs and java
 - horizontal refactoring


###ruby:
- can pass ranges to ‘when’ method in case statements
- object.succ -> get the next number

###tools:
- git-pair

###homework
- pick most egregious smell from our abstraction, find the one we can fix the easiest
