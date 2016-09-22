# No computer project


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

The idea is to have a story made out of modular pieces that could all
fit together to form something of a syntactically correct, but potentially
nonsensical narrative.  The purpose of the idea would be for entertainment.
Hopefully the experience of someone engaging with this DSL would be
enjoyment and experience comedy.  The user would construct some part
of a story, and based upon the decisions they made, the pieces would
interact in such a way that their story can be constructed from one
of exponentially many combinations of modular story blocks.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

The "need" is simply a desire for entertainment, so if the project
manages to entertain the user, it has served its purpose.  Language is
a natural choice for any kind of storytelling, and we need a language
that is specific to our domain of precise language to be able to construct
stories logically guaranteed to reach some conclusion.

### Why you?
_What excites you about this idea? How did you come up with it?_

I was looking at a book and thinking about how it was linear, but there
do exist books with "create your own ending" type stories. This was when
I imagined if we were able to pick not just between two endings, which
arrive through our choices, but rather construct our own endings using
myriad modular building blocks?

### Domain
_Describe the project's domain in five words._

Creating chaotic stories without planning.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

The user might have a deck of cards from which they can construct the initial
state of their character(s), setting(s), and plots.  From this point on, the
user might use a booklet or story guide which uses information about the
items or number of characters found in a story to determine the next step,
these choices build on one another, leading to a chaotic sequence of next
steps highly dependent upon initial conditions.

For example, one rule might read:
"If at least one character has been injured, and has not yet healed, add
the next tile from set #42."

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

The running of the program is the repeated lookup (by the user) of the next
step in the story.  Each next step should have some relation to all of the
the rules that can produce it so that the story, while chaotic, does not just
read as a pseudorandom hodgepodge of events, but rather a silly and loosely
connected thread of continuity.

Errors would result on the behalf of the user following with an incorrect
card, which they would either discover on their own, or not.  Either way
is acceptable.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to generate a silly story based on simple inputs.

It should be difficult to predict the next step in the story.

It should be impossible to predict the ending of the story given the
starting configuration.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

The only one I can think of is the story books that I mentioned inspired me,
which have one story along the top half of the pages, and a corresponding
story along the bottom half, where at each step you decide if you want
to flip the top page or the bottom page, and the different choices lead to
either a final ending at the top or at the bottom.

I think the language will be a bit clunky, especially as it will force users
to perform manual lookup of the next step themselves.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Most of the time would be spent coming up with unique story modules that can
easily be led into and out of by other modules.  A significant amount of time
would also be spent figuring out how to connect the modules together via
the different conditional chains, in a way that gives a roughly uniform
distribution of story elements from a particular combination of elements.

### Scope
_How big an idea is this? How ambitious is this project?_

This would be quite a substatial undertaking, as it would involve creating
an exponential number of storylines from whatever collection of starting
story blocks we would provide.  It would also take a bit of ingenuity to
ensure that the completed stories were worth the effort, not just a
boring laundry list of events.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This would be a terrible idea for an actual project, but I found it very
interesting to think about in principle.

