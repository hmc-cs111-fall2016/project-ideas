# Free project 2


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.

The language I had in mind builds Gantt charts. Gantt charts are used by people that need to build project schedules. Gantt charts not only encapsulate a schedule but also the dependencies within the schedule. These projects can vary widely from personal team projects to industry sponsored projects.

A language would be useful because it would make writing the dependencies easier.

### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

There are programs that make Gantt charts. However, there are a couple reasons why we would want a DSL for Gantt charts. Most software is not dedicated to Gantt charts. As a result, software is not built to make Gantt chart creation intuitive. Gantt chart software also costs money. Smarthsheets and Microsoft Project are two common Gantt chart creation softwares that cost money. The software also usually requires monthly subscription payments to continue using the software. This forces people to constantly pay to use the software indefinitely.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

All software for Gantt charts use Excel-like cells. But with a language, we can express complexities like what kind of dependencies there are within a schedule. There are several kinds of dependencies, so having a language can easily enumerate the kinds of dependecies. It also makes it clear what kind of dependencies there are when reading code. Overall, this would increase the intuitiveness of Gantt chart creation.

### Why you?
_What excites you about this idea? How did you come up with it?_

People at Harvey Mudd College in engineering clinics and other project-based engineering classes use Gantt charts to help schedule their tasks. I've talked to someone that personally expressed their frustration in how cumbersom it is to make Gantt charts with commercial software. It would be great to give students something easy that makes nice Gantt charts, saving them time to work on harder problems.

### Domain
_Describe the project's domain in five words._

Gantt Chart Creation

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

A user might type tasks with times with some natural language. For example, a user might specify something like `Inspecting hadron collider from 12:00 - 2:00 pm ...`, where the trailing dots represent further input. A user would also be able to build blocks like a sequence of linked tasks. This would be similar to making objects or classes in Scala as sometimes we might want to have blocks be standalone or a template for patterns within the project schedule.

There are a couple of good ways to interact with the problem domain. One is an imperative style of interaction. Scheduling problems for us tend to be naturally imperative as we simply just input times and dates into schedules. We often are able to figure out the logic, so an imperative style would be a natural choice.

A declarative choice/addition might also be useful. If one wants the program to make a schedule based on a few constraints, then a declarative approach can automatically generate a chart. One can then slightly tweak the chart to make it perfect and potentially save a lot of time this way. I believe an imperative or declaritive approach can both be useful and depend on a user's situation.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When the program runs the code, the output should be a (potentially interactive) Gantt chart. The program takes in lines of code (like tasks and dependencies). Errors such as conflicts may arise, although tasks may optionally be set to overlap intentionally. When a dependency is broken or an unintentional arises, the program should output messages to the user specifying where the problems occur in both the visualization and the code. 

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to implement basic dependencies like the ones defined by Gantt charts. It should also be easy to create tasks with times and dates and group them in objects or classes. I might decide to make it hard to have the users describe tasks in large amounts of detail. The point of Gantt charts is to get the big picture, and I think removing the ability for users to write a lot about individual tasks will make them focus on the big picture. 

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_


### Scope
_How big an idea is this? How ambitious is this project?_


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

