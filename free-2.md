# Free project 2


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

The process of writing a program to solve a recursive solution efficiently
(using a Dynamic Programming (DP) solution) requires a lot of boilerplate code
and opportunity for simple errors to be introduced.  The individuals using 
this language would be anyone who hopes to implement a solution to a recursive
algorithm more efficiently.

Hopefully their experience would be transformed from thinking about how
to best implement their dynamic programming solution without a stack overflow,
to one of simply thinking about the nature of the recurrence, expressing that,
and letting the language transform it into an effective implementation.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

The key to solving an algorithm with dynamica programming is understanding
the recurrence relation, and thus being able to build up a solution of a
given size out of solutions of smaller sizes.

### Why you?
_What excites you about this idea? How did you come up with it?_

I am excited for this project to be able to generate code for computing
solutions to generalized dynamic programming problems, especially
getting it to work for some of the more difficult dynamic programming
solutions to write by hand, such as the Nussinov Algorithm for RNA folding.

### Domain
_Describe the project's domain in five words._

Transform recurrences to dynamic programs.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_

The user would likely use this language as an internal DSL of another language
so that we can rely on the complexity and expressiveness of mathematical
functions in the host language.  This will allow us to specify the general
form of a recurrence and there will also be some manner of describing the
order in which we will fill in our dynamic programming table (i.e. row-by-row
versus along the diagonals).  This could also be described as a mathematical
sequence or a function and an initial condition, as a method to get the
order of tha table's cells to be filled in.

This is a good way to approach the problem domain, since the problem is
fundamentally one of computation, the idea being that we draw from the
host language to make the recursive solution easier to describe.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

I have a design decision to make, and I have not made it yet.  When the
code is run, we will either:
 * Generate the code which runs the DP and outputs it in a file.
 * Generates and executes the DP immediately, returning an answer.
I am currently leaning more toward the first option, as it would allow the
dynamic programming algorithm to be reused rather than regenerated each time
and also included in other code rather than run by hand.  Of course we could
always offer both options, but implementing the first one has interesting
design decisions related to pretty printing and comments in the generated code.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to represent a simple recursive algorithm and generate
the code which efficiently solves the algorithm.  It should also be fairly
straightforward to implement a standard recursive algorithm but to use
memoization rather than dynamic programming, since this would involve many
of the same components, but might be prefered in some cases (when not
_all_ of the subproblems must necessarily be solved).

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I don't think so.  I did find a github repo which had a heading called
[Clojure Dynamic Programming DSL](https://gist.github.com/foobar27/2777922),
but I don't think it's what I was looking for!  I think that perhaps a reason
for the lack of DSLs in this area is that a DSL to solve dynamic programming
algorithms is not much of a need to be filled.  Programmers working on a
solution to a dynamic program can certainly implement the dynamic program if
needed to, and my proposal would just make it a bit less work to do so.

It may also be the case that this problem is not particularly well suited
to being solved with a DSL, but rather with a library, which I would guess
_do_ exist for solving this problem.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

This project would probably have less than half of the time spent working on
it dedicated to the language design, since we would rest heavily upon the
host language for the parsing of expressions and the design decisions
I would be responsible for would mainly be how a user would represent information
about their table and the method by which they will fill it in.

A good bit of time would likely be spent implementing the process by which a
recursive expression is transformed into a rule for filling out one cell based
on others.

### Scope
_How big an idea is this? How ambitious is this project?_

This project seems to be pretty modest in scope.  It would involve parsing,
abstracting the generalized notion of a dynamic programming solution, and then
perhaps some research into pretty printing the outputs.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This might be a good idea since I find myself excited about the prospect of
quickly generating a solution to some of the more annoying DP problems.  It
would also involve learning a bit about how to subvert the parser of the host
language, since we want to keep its ability to extract meaningful relations
from mathematical expressions, but also to keep track of the struture of
recursive calls, since this is key information which informs how to construct
our table, and it would be ideal if the user didn't have to provide it twice
(once in the recursive expression, once for the DSL).

It might not be a good idea if there isn't enough language design in the
project.  The scope might be too narrow, addressed only toward solving a
very specific class of problems.

