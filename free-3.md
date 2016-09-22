# Free project 3

Groups DSL

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

A group is defined as a set of elements along with an operation such that the
elements "play nicely" with the operation (the group is closed, there is an
identity element, each element has an inverse, and the group is associative).
Often times, it is useful to find correspondences between groups, known as
homomorphisms, so that if a problem is complicated in one space, you can map it to
another domain where the solution might be clearer.  Sometimes it is hard to come
up with a map, and then to prove that the function is in fact a homomorphism, and
to do so involves tediously checking the pairwise product of each element.  In
abstract algebra, humans often tend to avoid doing brute force work in search of
cleverer solutions. However, it would be helpful to have a computer check your
progress on several examples to make sure you are on the right track.  This could
be encoded in a DSL.  One could create a DSL where the user can specify groups and
group operations and then leave the work to the DSL to find a bijection.
Sometimes a computer wouldn't be able to determine a bijection this way, say if
the group were infinite.  It would still be useful for a program to check hundreds
of examples, and if all of them work then that is a good indication to the user
that the groups are homomorphic.  In addition to showing two groups are
homomorphic, there are many other useful facts that you can show with this DSL
(_a_ is a subgroup of _b_, every group of size 5 or less is abelian) just by
encoding the elements and having a computer try several possibilities.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL would be appropriate because it would abstract away much of the work
required in creating functions to solve similar problems.  Moreover, a DSL would
be more appropriate than an API because this DSL would be more streamlined for
abstract and linear algebra.  In the same way that you would want a calculator to
have a small set of functions, it would be easier to learn the language if it were
limited to group theory.  Also, the syntax would hopefully represent the semantic
model more closely.

### Why you?
_What excites you about this idea? How did you come up with it?_

Much like the previous DSL that I mentioned, I am excited by this one because it
links two of my classes together.  Moreover, in all three of my problems sets we
had problems asking if one group was a subgroup of another, or if two groups were
homeomorphic/isomorphic.  In both cases, the easiest way was to find an example
and then verify that properties held for all combinations of elements.  This work
could have been expedited by a DSL.  I am also interested in many different facets
of this project--I have so far very much enjoyed abstract algebra; I am intrigued
by theorem proving (that was the topic of my summer research freshman year); I am
interested by Prolog, which seems like a potential way to store many facts and
check different combinations; and we dealt with encoding group theory axioms
logically in Jape during CS81.  This idea surfaced when I was talking to Prof Ben
during office hours.  He mentioned that groups had the potential of being encoded
in a DSL, and suggested that even if it might be hard to _mathematically_ prove a
homomorphism, a computer assistant could at least check hundreds of examples.

### Domain
_Describe the project's domain in five words._

An abstract algebra proof assistant

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

For starters, a user would have to define a group.  A group would consist of
elements and a group operation.  However, these elements could be variables,
coordinate pairs, or other possiblities.  It would be neat to use something like
Haskell pattern matching to define these elements as abstractly as one wanted.
For example, maybe you want to define an element as `Pair Double Double`. Then the
user would need to define a group operation within this same group object.  This
operation would need to take two elements as inputs and return one as an output.
I would imagine that this operation would look much like a function definition.
Once they have a group, they could define homomorphisms similarly.  This could be
a good way to interact with the problem domain because it gives the user as much
freedom as possible in expressing the group elements.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

The user could store all of these groups and functions in a "database", and then
have a main function which uses the database to do whatever the user asks.
Hopefully, the functionality built into the language would include determining if
two things are homomorphic, if _a_ is a subgroup of _b_, and operations like "for
all" and "there exists" that can be investigated through multiple attempts.  Using
this language, one could imagine asking, for example, if all groups of five
elements are abelian, since you could loop through all the possible group
operations and ensure that for each _a, b_ in _G_, _a_ and _b_ commute.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be very easy to check or prove useful abstract algebra properties about
groups.  As I mentioned above, ideally this would not be limited to homomorphisms
and subgroups.  It should be difficult to do any other sort of math, or coding for
that matter.  I think this language might have to be Turing Complete if it allows
loops and variables, so it would be hypothetically possible to do any computable
task.  However, most of them would be very difficult.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I would be surprised if there are any DSLs in this domain so far.  The main reason
for this is that it is a very specific domain, it people might think it isn't
worth the time to automate the process of finding homomorphisms instead of just
solving the problems case-by-case. Also, I hadn't thought of this type of DSL on
my own since I was approaching abstract algebra with a different mindset, and it
was only after talking with Prof Ben that I realized its potential.  When doing
abstract homework, I look for clever and short solutions, and try to avoid the
brute force that a computer could help with. I imagined that in order for a
computer to be helpful, it would have to be a theorem _prover_ that thought of
novel ideas like a human could.  This is a heavily researched area and a massive
project.  However, a computer could be useful not in doing the actual _proofs_,
but as more of an assistant to show that you are on the right track.  This bridge
between math and CS mindsets might explain why such a language does not exist.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I think much of the project would involve the most flexible way of writing a
language to define groups and operations.  Some groups that we have discussed in
class include the Cartesian product between of two sets, or the set of bijections
between two sets.  The could also be finite or infinite, or numbers with intuitive
operations (like + and *) or variables where you define the operations case by
case.  In addition, sometimes you would want the function to do something generic
for each x and y, and sometimes you would want to define a product for each pair
of elements.

For the systems part, the most commonly used component would be creating a way to
try all possible products.  If we incorporate other methods like `for all` and
`there exists` or other logical operations, the systems part of the project
could get trickier.

### Scope
_How big an idea is this? How ambitious is this project?_

The domain itself seems reasonably small, but the scope could grow to be very
large.  At its minimum, defining finite groups and operations and having a
function check all possible pairs seems very feasible.  However, allowing more
freedom in the definitions and extending the functionality could be more
difficult.  As I continue to learn more about groups (I have only been taking
abstract algebra for three weeks), I may learn about more ideas that could be
assisted with a DSL, which might extend the possible scope.


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This would make a good project for me because it combines two classes, which will
enhance my understanding of both of them.  As I mentioned in an earlier response,
I am also very interested in many components of this project.  Also, at its
minimum the scope does not seem to large.

On the other hand, the domain seems quite small, and it might not be very useful.
There are not _that_ many problems which involve finding homomorphisms, and most
of them seem to be for beginners.  Therefore, it might not be worth it for most
people to learn an entire new language.  Moreover, as someone new to abstract
algebra, I feel like it would be more helpful to think of the bijection on my own
than to use a computer sidekick.  Also, there are some groups that would be
quite difficult to encode, like the set of rotations in 3-space or the group
generating by composing paths on a torus.
