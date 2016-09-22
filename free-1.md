# Free project 1

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Tableau trees is widely used in logic. 
There is a LaTeX 
[package that's specifically for drawing tableau trees](http://ctan.org/pkg/prooftrees)
but its syntax is quite challenging.
So this project would be for logicians who are not familiar enough with LaTeX
to feel comfortable using the packages for drawing trees.
Ideally, this project would eliminate the need to drawing out lines and moving
text boxes using formatting tools like Google Slides, which is the recommended
formatting tool in CS 81.

_Why is a DSL appropriate for your user(s)? How does it address the need?_

People already use a package in a DSL (LaTeX) to draw tableau trees and trees
in general.
But a tableau tree has enough distinguishing characteristics from any tree 
diagram that a DSL for tableau trees should have a simplified interface.
In CS 81, the construction of a tableau tree is reduced to two operations:
stack and split. So I think a DSL can use that technique to build a simpler
syntax for a DSL for tableau trees.
A DSL for this would make the task much less cumbersome as hopefully users
would find the DSL simpler to use than drawing out a tree using lines and text
boxes.

### Why you?
_What excites you about this idea? How did you come up with it?_

I have to draw tableau trees for my CS 81 homework and they cannot be hand
drawn.
I generally TeX my homework, but I've found the syntax of packages for drawing
trees to be difficult to understand.
I imagine that the syntax would be even more daunting for people who do not
use LaTeX for most of their homework.
I TeX-ed tableau trees in the latest homework but it required a lot of trial
and error as well as reading a _lot_ of samples of various tree structures.
I would be really happy if there was an easier way for me to draw trees for 
my homework.

### Domain
_Describe the project's domain in five words._

Writing logic proofs in math.


### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

Like LaTeX, the programmer would write text to a file which would then be
compiled to the image of a tree.
One possible way a program could look is
```
(A \or B) \and C \check
C
A \or B
  A
    branch1
    branch2
  B
```
which would produce the following tree

![tree](/images/tree.png)

This uses LaTeX syntax, such as backslashes to invoke certain symbols, which
is familiar to many people who work with math.
The structure is more easily readable for statements that stack (such as
C and A \or B) compared to the equivalent tree in many tree packages in LaTeX
which expects a statement on the next line to be the child of the previous
statement (so A \or B would be the child of C) which would then draw a line
between them. 
This would go against tableau convention.
The package prooftrees solves this issue but still requires A \or B to be
indented relative to C, which is harder to read.

For logicians, there should not be a need to specify math mode marked by \$
since everything should be mathematical symbols.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

The program would read the entire file to calculate how much branching is
requested. 
It would also calculate how long each statement in the tree is based on how
many symbols are used.
This is then used to calculate the angle and length of lines in the tree for
branching to give each statement enough space.

If the program runs with no issues, it would then produces a new file, an image 
or pdf, of the resulting tree.
Else, it would produce a file containing error messages.

Possible errors could include unrecognized commands for symbols.
With the syntax described before, blank lines could be an error or a warning.
An error could arise if the user tries to branch in more than two directions,
this would throw off the distance calculation.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to draw binary trees with logic symbols.

It should be possible, but maybe not necessarily easy, to customize these
symbols. 

It should be impossible to draw trees that are not binary.
Drawing shapes other than trees is also possible after a lot of difficulty.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There are many packages in LaTeX for drawing trees.
This is the code I actually used to generate the tree image used as an example
earlier
```
\Tree
[.{
$(A\vee B) \wedge C\checkmark{}$    \\
$C$ \\
$A\vee B\checkmark{}$   \\
}
    [.{$A$}
        [.{branch1$\quad$}
        ]
        [.{branch2}
        ]
    ]
    [.{$B$}
    ]
]
```
I used the package qtree, which is actually for linguists so it uses
linguistics conventions. The code shows that it requires a lot of work-around
to get the tree I wanted. I used qtree with the help of 
[this page](https://github.com/cpence/latex-tableaux)
which documents ways to make qtree work for logic proofs.

As mentioned earlier, tree packages generally expect each node to be a single
line.
So stacking in tableau trees do not translate neatly into most tree packages.

There is a package for tableau trees, 
[prooftrees](http://ctan.org/pkg/prooftrees).
But the syntax is quite complicated since it offers a lot of customization,
which is great for experienced users. But this makes it difficult for someone
who wants to draw a basic tableau tree.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I suspect that a lot of time would be dedicated into semantics, specifically
into calculating the spacing between branches.

The proposed syntax seems very intuitive to me, so maybe there won't be a lot
to do in terms of language design decisions. 
But my guess could totally be wrong and maybe there's a lot more research
required into the language aspects.
If the language borrows a lot from LaTeX, which seems to make sense for the 
domain, there would not be much to do in terms of language design.

### Scope
_How big an idea is this? How ambitious is this project?_

The project has a very specific set goal, so I think it's not too ambitious.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This would be a good idea because I would be excited to work on this project
and because I think there's a real need for it.

This would not be a good idea because there may not be a lot of time needed
in terms of language design.
Moreover, I could fall on the trap of designing a language that only makes
sense for me.

