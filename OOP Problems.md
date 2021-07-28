#Design 

Common problems in [[OOP]] as code paradigm


## The banana gorilla jungle problem
Imagine that you are creating a new project. And you need a `Banana` class. Ok no problem you realized this class in previous project, lets reuse it. But then you got another problem `Banana` class depends from `Gorilla` class then `Gorilla` class depends from `Jungle` class. Now instead of copying `Banana` class you got almost full previous project in your new code.


The creator of Erlang, Joe Armstrong proclaimed:
The problem with object-oriented languages is they've got all this implicit environment that they carry around with them. You wanted a banana but what you got was a gorilla holding the banana and the entire jungle.


## The fragile base class problem
Imagine you've reused class from previous project for your new code. What happens if the base class changes? 
It can corrupt your entire code. You might not even touched it. But one day your project works like a charm, the next day it doesn't because somebody changed a minor detail in the base class that ends up being crucial for your project.

Code reusing can seems very efficient in short term, it can get costly in the long term.


## The diamond problem

Inheritance is this cute little thing where we can take properties of one class and transfer it to others. But what if you want. to mix the properties of two different classes.

Well, you can't do it. At least not in elegant way. Consider for example the class Copier. A copier scans the content of a document and prints it on an empty sheet. So should it be the subclass of Scanner or Writer? 
Example from: https://cscalfani.medium.com/goodbye-object-oriented-programming-a59cda4c0e53

There is no good answer. And even through this problem doesn't break yours code, it comes up often enough to be frustrating.


## The hierarchy problem
Let follow up with diamond problem. Lets `Copier` be the parent class, and `Scanner` and `Printer` be sub classes  that only inherits a subset of the properties. Problem fixed! 

What if `Copier` is only black-and-white, and `Printer` support colors? 
What if `Printer` is connected to WIFI but `Copuer` no?

The more properties you have in classes, the more difficult it becomes to establish proper hierarchies. You trying to solve this problems and in result you got a big complex project that solves a simple task. 


## The reference problem

## 5. The reference problem

You might say, alright, then we’ll just do object-oriented programming without hierarchies. Instead, we could use clusters of properties, and inherit, extend, or override properties as needed. Sure, that would be a bit messy, but it would be an accurate representation of the problem at hand.

There’s just one problem. The whole point of encapsulation is to keep pieces of data safe from one another and thus make computing more efficient. This doesn’t work without strict hierarchies.

Consider what happens if an object `A` overrides the hierarchy by interacting with another object `B`. It doesn’t matter what relationship `A` has with `B`, except that `B` is not the direct parent class. Then `A` must contain a private reference to `B`, because otherwise, it couldn’t interact.

But if `A` contains the information that the children of `B` also have, then that information can be modified in multiple places. Therefore, the information about `B` isn’t safe anymore, and encapsulation is broken.

Although many object-oriented programmers build programs with this kind of architecture, this isn’t object-oriented programming. It’s just a mess.


## **The danger of the single paradigm**

What these five problems have in common is that they implement inheritance where it’s not the best solution. Since inheritance wasn’t even included in the original form of object-oriented programming, I wouldn’t call these problems inherent to object orientation. They’re just examples of a dogma taken too far.

Not only object-oriented programming can be overdone, though. In pure [functional programming](https://towardsdatascience.com/want-to-get-started-in-functional-programming-enter-scala-ea71e5cfe5f8), it’s extremely difficult to process user input or print messages on a screen. Object-oriented or procedural programming is much better for these purposes.

Still, there are developers who try to implement these things as pure functions and blow their code up to dozens of lines that nobody can understand. Using another paradigm, they could have easily reduced their code to a couple of readable lines.

Paradigms are a bit like religions. They’re good in moderation — arguably, Jesus, Mohamed and Buddha said some pretty cool stuff. But if you follow them to the last little detail, you might end up making the lives of yourself and of people around you quite miserable.

The same goes for programming paradigms. There’s no doubt that functional programming is [gaining traction](https://towardsdatascience.com/why-developers-are-falling-in-love-with-functional-programming-13514df4048e), whereas object-oriented programming has attracted some [harsh criticism](https://medium.com/better-programming/object-oriented-programming-the-trillion-dollar-disaster-92a4b666c7c7) in the last few years.

It makes sense to get informed about new programming paradigms and use them when appropriate. If object-oriented programming is the hammer that makes developers see nails wherever they go, is that a reason to throw the hammer out the window? No. You add a screwdriver to your toolbox, and maybe a knife or a pair of scissors, and you choose your tool based on the problem at hand.

Functional and object-oriented programmers alike, stop treating your paradigms like a religion. They’re tools, and they all have their use somewhere. What you use should only depend on what problems you are solving.


## What about solution?
In my mind better solution to use best of different paradigms.


Origin: https://thenextweb.com/news/object-oriented-programming-is-dead-syndication