# No computer project


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

_The idea is that the wooden blocks you put together to make patterns are a
DSL. (http://www.hand2mind.com/item/wooden-pattern-blocks-1cm-set-of-250/1218?gclid=CJXS3N2Dos8CFYmCfgodAzcAVg&gclsrc=aw.ds)
The need met is learning about patterns and shapes. Additionally, there is
a need of visualizing a pattern before using it. Before wooden blocks, there
was a difficult experience of seeing how the shapes could fit together and
understanding how angles worked in different shapes. These blocks give a
tactile, visual way of learning about patterns and angles._

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

_This language is appropriate because it does not involve drawing, which
can be inprecise, or imagining, which can leave people unsatisfied. It 
addresses the need by giving them wooden blocks, which have all been cut
to be certain shapes. This lets them interact with the blocks and try all
different types of blocks to see which ones fit._

### Why you?
_What excites you about this idea? How did you come up with it?_

_I love this idea because there are only so many ways that the
blocks can interact with each other that does not leave any blank space
in between them. It's such an interesting way to introduce geometry and
learn about the angles of the shapes when the math might still be too
hard. I came up with this idea by thinking about the argument we discussed
in class that the marble run was a DSL. I led me to thinking about how
other childhood toys could be DSLs, which made me think about the wooden
shape blocks._

### Domain
_Describe the project's domain in five words._

_Shapes coming together, making patterns_

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

_People would be able to interact with the language by phyically grabbing
the blocks and trying them out in the program. This is the right way
to interact with the problem domain because instead of asking people to
imagine what happens when a square's edge hits a diamond's edge, they
can physically grab the square and see what happens. This can be far
less confusing for a user, espcially as patterns get larger._


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

_I'm not completely certain how a program would run for this DSL because there's
no point where you stop and test it, but I think that it would run each time that
a user would put a new piece on or move a piece. The errors would be seen visually
by a space in between the blocks. Although these are not terrible errors, when
trying to create patterns or sets of blocks that can be repeated and used for
other domains such as creating art, this blank space cannot be there. So, the 
user would be able to visually see when they have made an error. The program would
interact with the user by showing it the pattern that the user has currently made._


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

_In this language, it would be easy to create patterns. With enough blocks, it would
be easy to create large, repeating patterns. It would be difficult, but possible
to have variable patterns that would change based on some input, specifically
a command to the user. It would be impossible to implement functional programming
in this language._


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

_This is the only DSL in its domain. All the blocks I could find online had very
similar shapes and colors. The only possible difference would be the material,
which I do not think is very critical._

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

_Once someone got an idea to work on this project, they would have to decide which
pieces they want to include in their DSL. So, this would all be engaging with the
language because they would have to think about how the blocks can interact with
each other, how the colors interact with each other, and how many of each block is
enough to make interesting patterns without being overwhelming. The "systems" aspect
of this project would just be making the blocks, which would mostly require some
hours in the machine shop (or an engineering friend)._

### Scope
_How big an idea is this? How ambitious is this project?_
_This project does not have a huge scope because the project as shown is about 5
shapes of blocks, each of which has its own color. If someone wanted to add
to this project, they could make it bigger. However, they would have to carefully
consider which shapes to add._

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

_This might be a good idea for a project because it would focus heavily on the 
design aspect. It would ask someone to defend why they chose to include a trapezoid
over a hexagon, which seems difficult but would be very interesting to think
about. How does a trapezoid work with the other pieces differently than a hexagon
would? It might not be a good idea because of the scope. With a language like this,
there is a very quick point of diminishing returns. Having a set of 5 shapes is fine,
but having even 8 shapes can become overwhelming. It can be difficult to promise that
all pieces will be able to sit next to each other in a satisfying way. So, if
someone were to do this project they would likely be creating a very small set of
blocks, which would probably not take very long._
