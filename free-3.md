# Free project 3: Recursion visualizer

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.

This project would serve intro CS students trying to wrap their heads around recursion, or more advanced students dealing with more complicated recursive algorithms. 

### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

In Intro classes, recursion can be tough to grasp at first, so this would be geared towards those students. This would also benefit students in more advanced courses like Algorithms, where multiple recursive calls can be easily visualized instead of having to manually draw it out. In this way, it would be easy for students to actually see all the recursive calls saved by a lookup to a DP table, for example. 

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

CS students, the target audience for this project, are familiar with programming so using this DSL would not be hard. The idea is to allow any recursive function and its arguments to be displayed on a visualizer. It would show the starting call and subsequent calls, also displaying the arguments that change with each call.

### Why you?
_What excites you about this idea? How did you come up with it?_

From my experience as a CS major and having tutored Intro CS classes, it would be a very helpful DSL. It's exciting to me because it's a very real problem that can be tackled. I came up with it while brainstorming with a friend. At first we thought of a DSL that would turn a recursive function into an iterative one, then came up with this. 

### Domain
_Describe the project's domain in five words._
Visualizing recursion for CS students

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

Ideally, the user would interact with it by writing/pasting code into some sort of GUI, maybe on a webpage. Then certain parameters could be set like the starting arguments passed into the function or the speed of the animations to display the recursive calls. 

The MVP would be the same thing but on terminal - users would pass in a file with the recursive function. CS students should be comfortable enough with using terminal to use the DSL. 


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

The recursion function to be visualized may have an error in it. If I do this with Java, Ant should be able to catch these errors on compile time. If a non-recursive function is passed, then it will need to show an error displayed to the user through the GUI or a terminal message. 

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to visualize the steps of a recursive algorithm in this language, impossible to do anything else. 

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There is this one already, though not sure if it technically qualifies as a DSL: http://visualgo.net/recursion. It's very well done already, I like how you can rewind and play the recursion step by step. There are also standard recursion problems that you can see via a drop-down menu, instead of having to strictly write your own code. That project was built by quite an extensive team (and several groups of students' final projects) so it would be unlikely that mine would be better to use. Although, in my opinion, it would be better if the recursive calls (i.e fibonacci(4), fibonacci(3)) could be displayed as well with the operations performed showed on the arrows between nodes. 

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

There doesn't seem to be that many language design decisions necessarily, more UI choices to be made to display the information in the best possible way. One difficult choice would be choosing which features to prioritize. 

### Scope
_How big an idea is this? How ambitious is this project?_
If a full GUI needs to be built, it would be quite an ambitious project - evident by how many people worked on the visualgo.net project. If we're ok with less of a UI, it could work on the terminal which would save time. I would need to figure out how to store recursive function calls on a stack, complete with its arguments. Then I would have to figure out how to generate a tree to visualize these recursive calls.  

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

It'd be a good idea for a project because the problem domain is so relevant to us as students. There are techincal challenges involved, but the overall amount of work seems to be within the scope of this class. It may not be a good idea because there aren't strictly speaking that many language design decisions to be made (unless you count the input and the output of how to display these recursive calls). 
