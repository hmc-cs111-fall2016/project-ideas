# Free project 1

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_
This language serves the need to take notes in economics classes on the computer.
My personal experience, and those of a couple other economics students, finds
that taking notes on the computer allows for a more complete transcript of the
lessons given by economics professors. Economics professors tend to provide
powerpoint slides that outline major points -- or worse, major questions -- of
the lecture and then provide the context or answers to these points verbally.
Often, the homework questions and exam questions relate to the things _said_ in
class. Thus, it's extremely helpful to transcribe lectures, in my opinion. 
Typing on the computer is much faster than writing by hand, so transcribing is
more possible on the computer.  However, the biggest issue is that economics 
involves many graphs. Copying down these graphs by hand is currently the main 
option for note-taking, unless one searches for the exact graph on Google
and then copies it into ones notes -- highly inconvenient and not fast enough
for a classroom setting.  Thus, I found that I had my notes in two places: on
my computer, and loose sheets of paper with graphs. Eventually, I switched note
taking style to only take notes by hand, but it still feels inefficient to this
day, and frustrates me immensely when exams come around and questions regard 
content _said_ in class but I failed to take note of.

Thus, I propose a DSL that is a markup language specifically for economics to
allow transcribing notes efficiently, but most importantly, allow for graphs to
be embedded in the notes very quickly and easily.  This allows a economics
student to have their notes all in one place, and the opportunity to transcribe
the verbal lecture from the professor while having relevant graphs available for
reference.  


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_
A DSL is appropriate because lecture notes consists of content written in some
language. Thus, the solution to the problem above should also be some sort of
language. Furthermore, since notes can be taken on the computer, a computer
programming language makes sense; however, it serves a very specific focus, so
it should be a domain-specific language so it does not confuse economics students
who likely have little interest in learning a massive language for this small
purpose. 

### Why you?
_What excites you about this idea? How did you come up with it?_
This excites me because it stems out of a personal problem. My high school was
okay with allowing me to take notes on the computer in any class. I found
that social sciences classes which require memorization, teachers
who did not necessarily write every important definition or point out but rather
preferred to talk about it, could be extremely frustrating if good notes weren't
taken. I became a great note taker with my computer and, though studies show
otherwise, felt like I absorbed more through taking robust, detailed notes on 
the computer rather than listening and hand-writing notes sparingly. The biggest
issue came in college economics, my major, when many graphs came into play and
therefore made computer notes very difficult.  Using Evernote, clipping pictures
of the relevant graphs from Google images was the only solution, but was too
inefficient to continue doing.  So, I thought having a domain specific language
for this would be a great solution. 

### Domain
_Describe the project's domain in five words._
Creating graphs for economics notes

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 
The user would likely be using some sort of text editor or word processor for
taking notes. This is an early problem for me: can I create the language to be
usable in popular word processors? Regardless, I would imagine some note snippets
to look similar to the following in this language:

``` 
This is a standard supply and demand graph

Graph{
	Y-Axis: Price
	X-Axis: Quantity
	SupplyCurve()	
	DemandCurve()
}

generate Graph
```

```
Today, we're learning about the *Engel Curve*, the graph looks like this: 

Graph{
	Y-axis: Income/month
	X-axis: Units
	EngelCurve()
}

generate Graph
```	

By instantiating some Graph object, you can generate a graph in place in the 
notes. Then the user could label axes and specify the curves that are needed 
in the graph. So you could specify SupplyCurve(), which would give a default
upward sloping supply curve. Each curve could take certain parameters for
transformations, for example `SupplyCurve(Slope: .5, Y: -10, X: 50  )`, would
give you a supply curve with slope of .5 starting at a Y-value of -10 and X-value
of 50. Also, we'd want to support markdown in the language to give users
easy formatting options when writing notes.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_
The program would ideally run on save.  When it runs, the language would generate
a graph image and then copy it to the clipboard for the user to paste or
ideally make it appear in place, but this might be difficult. An early issue I 
could forsee happening is if a user specifies a curve that is not supported in
the program.  For example, if they specified `ProductionFunction()` and we didn't
support that curve, there would be an error.  The way for this error to appear
would likely be through some sort of linter, much like other programming
languages have. We would then notify users at compile time, or in this case on
save that there is an issue and communicate it clearly.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_
It should be easy to both take notes in natural language and generate graphs in
the same editor or workspace. It should be possible to create extremely custom
graphs, but I imagine that it would be difficult and may require more time
than available during a class session.  It should be impossible to do anything
other than take notes in natural language or create economics graphs. No web
development, solving algorithms homework, etc.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_
There aren't any DSLs that do this in the editor. However, there are tools
online such as [this one by a UConn  Professr](http://harmon.uconn.edu/GraphTool/GraphTool.html) that are online. Though not really a DSL but more of a user interface for
creating graphs, this is similar to what I would want to do. This doesn't really
address the need of students in the classroom taking notes. That being said, I
admire the ease at which you can access popular and common curves, such as cost
curves and production possibilities curves, to create graphs.   

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_
I am not entirely sure how to implement languages quite yet, so I don't think I
have an accurate judgment of this at the moment. I do, however, think that this
may require a lot of systems code to work in the context of an editor. At this
point I would still think language design would be a major part of the project,
so my guess would be 50-70% of time would be spent on language design. 


### Scope
_How big an idea is this? How ambitious is this project?_
I think this is a pretty ambitious project. While I think the impact is relatively
small, and adds some convenience to a very specific group of people, it may be
difficult to implement. Furthermore, if I am able to somehow mix pure text or 
markup and efficiently create graphs in place (unlikely, this will more likely
be just an easy way to create graphs in an outside environment and copying it
into a note taking app), it could be a new way to think about creating notes
or documents since visualizations are present in many documents and are usually
created separately. 

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_
This would be a good idea for a project because I think it touches on many
different things: creating visualizations are needed, design to make the language
intuitive is important, and working in the context of an editor or word processor
is also a major aspect.  However, this may not be a good idea because it may be
too ambitious to solve the actual problem of creating graphs in place. I'm not
sure whether it's actually possible to compile the graphing code from a text 
editor without creating my own compiler, which I'm not sure we'll be doing or
have time for. 

