# Free project 4

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

My final idea is to create a DSL which is designed specifically for plotting
high dimensional data.  I would be helping scientists, data analysts, and
anyone who needs to create three dimensional plots.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

The problem of plotting high dimensional data is essentially a problem of
describing the shape of a surface in some dimension and rendering this
information in a useful manner.  Having an effective way to express the data
can allow the computer to worry about the rendering rather than leaving
it up to the user.

### Why you?
_What excites you about this idea? How did you come up with it?_

I was often annoyed by the use of boilerplate code in matplotlib and
difficulties in verifying that 3D plots were correct.  I was thinking
that having a better way to express the data might be the bottleneck.
For example, in matplotlib, one must create a "meshgrid" and set values
of a function to corresponding values, rather than simply provide a
set of (x,y,z) values to plot, or a function and a range of `x`s and `y`s.

### Domain
_Describe the project's domain in five words._

Ploting high dimensional data easily.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

A user would probably use an internal DSL written in some language that already
has high quality plotting and rendering DSL written in the language.
The DSL might just provide additional APIs which can allow greater freedom to
adapt to one's data rather than forcing the data to undergo transformations to
fit a rigid API.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When the program runs, the DSL will manipulate the data provided by the user
to put it into the format expected by the plotting software used as a backend.

Errors could include data that of the wrong format for the API, in which case
we would need to check that the data conforms to our expectations before
calling the backend code, which might fail and give very unhelpful error
messages to our user.  We should catch these mistakes in input, provide a
useful description of how it differs from our expectation, and then return.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to plot three and four dimensional data without much thought.
We can use perspective, color, and perhaps even texture to represent additional
dimensions.

There should be a way of producing level set plots as a manner of dimensionality
reduciton.

It should be a little more difficult to plot very high dimensional data, since
rendering will likely be difficult and provide little insight.  However, we
might want to investigate dimensionality reduction to see if there are still
lower dimensional plots we can generate to help get an idea of trends in
certain dimensions.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

Absolutely, R, matplotlib, and MATLAB all occupy a similar domain to this one.
However, ours would be more narowly tailored to apply only to plotting in multiple
dimensions.  These other languages provide facilities for high dimensional
plotting, but in my experience they are a litle less polished than the two
dimensional versions which see the most use.  Many of the visual issues can be
addressed with code, but again, this is troublesome and boilerplate which could
be avoided.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Most of their time would probably be spent dealing with the various backends,
verifying input data matched those expectations, and visually inspecting
various generated plots for aesthetics.  Very little time would actually
be spent designing the language.  (This is a very good question, it has helped
me rule out a good number of projects now!)

### Scope
_How big an idea is this? How ambitious is this project?_

The project is of medium to large scope, since interfacing with the backend
could take significant research and debuging.  The optimization of the various
elements of the final rendering could also be significant in determining the
intensity.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This might be a cool project because it fulfills a useful need, but it is
probably not a good project for cs111 because there are not enough interesting
questions about how to represent the data in languages.

