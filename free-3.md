# Free project 3

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

This language will help students see the connections between art and science,
an hopefully stimulate people's interest in interdisciplinary boundaries.

More specifically, the language will allow users to create digital graphical
art by defining and manipulating mathematical expressions. What ContextFree is
for grammars, this language will be for mathematics.

Currently, there is a clear divide between "sciencey" disciplines and "artsy"
disciplines, when in fact their is a great deal of creativity involved in the
sciences (including math), and knowledge of computer science and mathematics
can be a great help to those trying to create art. This language would attempt
to close that divide and show users the benefits of interdisciplinary study.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

I want the user's experience to be one of discovery. There is an unimaginably large space to be explored here, and the user should be in charge of how they
choose to explore that space. The best way to accomplish this seems to be to give the user a small set of building blocks that hopefully form a basis for the space, and to provide an easy way to combine the building blocks to form connections and set off in new directions. In other words, to give the user a language and let them decide what to say with it.

### Why you?
_What excites you about this idea? How did you come up with it?_

One of my best friends is an engineering major interested in art, or an artist who is studying engineering. One of the things she is most passionate about is closing the gap between science and art, as I mentioned above. That, and the specific method of exploring math through art or vice versa, are ideas she has often expressed an interest in. As I've learned more about DSLs in this class, it occurred to me that a DSL could be a good way to implement these ideas.

### Domain
_Describe the project's domain in five words._

Interactive art described by math.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

Given that this is meant to be an interactive exploratory process, the
interface should facilitate fast, easy changes to parameters. I imagine it
would look similar to Bret Victor's
[system](https://www.youtube.com/watch?v=PUv66718DII&feature=youtu.be&t=571),
which we saw on the first day of class. The user would be able to define a
mathematical model for their art -- perhaps using MATLAB-like syntax -- and
then they could use sliders and other interactive tools to tweak the
parameters, thereby exploring the space around their model.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

At a very high level, when a program runs, the user's mathematical expressions
are evaluated and the result is displayed in a visual form. The exact method of
translating formulas to an image, I have yet to determine. I can think of
several possibilities. The user could give formulas the determine the color as
a function of space.

Or, the formulas could be interpreted as describing a set of objects or
surfaces in 3-space, which are then rendered to the 2D screen.

Or, interesting properties of the functions specified the user could map to
interesting features in the resulting image. For example, the zeros of a
function could correspond to bright points or lines in the image.

Or, these methods could be combined in a way specified by the user.

In terms of errors, there are roughly two kinds. The first occurs when the user
enters an ill-formed formula. This could be as simple as mismatched
parentheses, or it could be more complex. The second type of error could occur
when the formulas do not easily map to a visual result. For example,
singularities may pose a problem.

As this language is intended to be somewhat education, it would hopefully
provide for all of these errors a helpful error message, which contains
information about what went wrong, _why_ it went wrong, and how to fix it. It
would be really awesome, although probably difficult, to link to a knowledge
base like Wolfram Alpha where the user could get more information on the theory
behind the error.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to create a visually interesting picture which gives some insight about the formulas that created it. It should be difficult, but possible, to learn to predict the form of the image based on the formulas. But it should not be possible (or it should be prohibitively difficult) to choose formulas to create a specific image. Just as one would not use ContextFree to create a particular picture, so one should use this language instead for exploration.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I've mentioned that this language is like ContextFree in that it uses a formal
theoretical concept to explore art, or vice versa. There are also many existing
tools which can help the user visualize a mathematical function, but these are
typically geared more towards academics. Examples include [MATLAB](http://www.m
athworks.com/products/matlab/?requestedDomain=www.mathworks.com) and
[Mathematica](https://www.wolfram.com/mathematica/). I do not know of any
existing DSLs geared specifically towards the math-art boundary.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Implementing the visualization aspect might be difficult. I'm not familiar with
what solutions are already out there for generating images, so I until I am
able to look into it further it will be difficult to say exactly how much of a
challenge this will be.

The bigger difficulty would be implementing the interactive features a la
Victor's system. However, those are features that could be added after
achieving a working prototype.

Much of the rest of the time spent designing the language would be in designing
the conversion from formulas to images. Getting this right will be both
difficult and critical, because I suspect that not any implementation will
yield interesting visual results. However, I would argue that making these
decisions is equivalent to designing the language itself, and not the
implementation, because the decisions will be heavily driven by the need to
provide an intuitive and rewarding interface to the user.

### Scope
_How big an idea is this? How ambitious is this project?_

I think it's borderline. It seems like a difficult project, but as I described
above, it could be implement in stages. A minimum viable product might not
include the interactive parameter adjustment I talked about; it might function
just as a way to visualize mathematical expressions, with the more interactive
features being added later as time permits.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

I think this project could inspire a creative approach to language design. I
like the way that the language focuses on process (ie the user interacting with
the program, rather than just writing a program and then calling it finished).
This mirrors the goal of CS111 to focus on the process of language design.

The biggest drawback is that there are likely to be planned but unimplemented
features left over at the end of the semester.
