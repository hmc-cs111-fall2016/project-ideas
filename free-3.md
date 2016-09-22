# Free project 3

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_
My idea is to create a repository visualizer DSL. It is very difficult to jump
into a large repository of code and understand how the code works. Especially for
people new to open source, going into GitHub and making sense of a large project
can be very intimidating. I imagine this stops a lot of people from even beginning
to scratch the surface in understanding how an interesting project works. If I
could help, the experience of jumping into a new code base would be much less
intimidating. While READMEs do a good job of explaining the project as a whole,
there is often a lack of description of how the codebase is structured and what
each directory contains. Therefore, I would want to be able to visualize the 
code in relation to the application. There would be a "starting point" directory
that is clearly defined for each part of the application (front-end, database, 
back-end, etc.). Ideally there would also be a visualization to trace through 
which part of the code a specific action runs through. 

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_
It is appropriate because the target users are developers who write code.
It makes sense to give them additional code to write because the code will be
written in the existing code base. Furthermore, it requires language to
communicate what exactly you want users to understand.

### Why you?
_What excites you about this idea? How did you come up with it?_
The motivation is from my summer internship.  I worked at (Sourcegraph)[https://sourcegraph.com], a semantic code search and global cross reference engine. One
of the ideas thrown around was to help users understand code bases. The idea of
a "starting point", was explicitly brought up by one of the developers, and I
want to take this to the next level. This excites me because if done well, it
could truly be used in every single code base and helpful to every developer
out there.

### Domain
_Describe the project's domain in five words._
Visualizing code repositories

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 
The user would have to explicitly code where the "starting point" and trace
points are in the repository. So, we could imagine the code in the dsl to look
like this: 

```
import Visualizer

var tracingSomeAction = new Visualizer();
function foo() {
	tracingSomeAction.startingPoint()
	...
}

function bar() {
	tracingSomeAction.tracePoint()
}

function baz() {
	tracingSomeAction.endPoint()	
}
```

The output would be a series of charts or trees for each Visualizer object so
we could see where to start and the trace through the code for the action.
 
### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_
When the program runs, an image with links to specific parts of code would be
generated.  There would be some CLI to run the code specifically to search for
these user generated code snippets using the Visualization library. Errors would
be if no starting point or end point were found, and this would be communicated
when the CLI was run. 

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_
It should be easy to generate graph images. It should be difficult but possible
to generate random art with this by creating weird visualizations. It should be
impossible to do anything else.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_
There are some applicatons/DSLs in this domain. One example is (this)[http://ghv.artzub.com/].
It creates really _nice_, artsy visualizations, but it does not do it in a practical
manner. We want to create something that is actually readable and useful to 
people new to a project.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_
I think most of it would be language design, probably 70% or so. The 30% would 
be figuring out how to create images from the code and maybe figuring out how to
compile the code such that we only look for the stuff specific to our library. 


### Scope
_How big an idea is this? How ambitious is this project?_
I think this is a pretty ambitious project. It seems decently difficult, but
also very useful.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

I think it would be great to create a DSL related to programming itself. It also
serves an interesting and useful purpose. It may not be a good idea because I am
not entirely sure how to create a good user experience of generating visualizations
separately such that it doesn't occur every single time the code is run.

