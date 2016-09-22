# No computer project


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

A group of people on campus regularly play a large game of Diplomacy.
The board games involve the players sending in instructions for their units
on the board.
These instructions are collected then played out simultaneously.
This causes a lot of conflicts between their instructions which are then 
resolved based on the game's rules.
Further complications arise when players send invalid instructions.

A program that can take in these instructions and then validate moves and
resolve conflicts would speed up this process.
As of now, it takes 5 to 10 minutes for people to manage this process.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

This program would need to take in inputs from the players.
A DSL would be an appropriate method to take in these instructions.

### Why you?
_What excites you about this idea? How did you come up with it?_

I like boardgames and I'm somewhat interested in boardgame design. 
This project builds on a homebrewed version of Diplomacy, so I'm excited to
contribute to a project that already exist and needs help.

### Domain
_Describe the project's domain in five words._

Multiplayer turn-based homebrewed boardgames.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

Diplomacy has its own syntax for user instructions
```
<Nation>
<Boardgame piece> <Location> to <Destination>

<Nation>
<Boardgame piece> <Location> holds

<Nation>
<Boardgame piece> <Location> supports <Boardgame piece> <Location>
```
Since this is the syntax that players use, a DSL for the game would also use
the same syntax to cater to its users.

But the DSL would need to know what the map looks like to validate moves.
We could use an adjacency matrix to store this data.
The players could enter the data for this matrix using a spreadsheet.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

The program would store the representation of the graph.
This map will be used later for validating players' instructions and resolving
conflicts.

As players send in orders, it would read the moves to ensure that they are
valid.
When the order collecting phase is over, it would then collect the instructions 
from each player.
It would go through the instructions according to the game's rules and resolves
conflicts.
Finally, it would output the final positions and states of each boardgame piece.
The output format could be a list of every piece and its respective location.

If the program finds an error in a player's set of instructions it could send
an email to the player based on a database of players' information.
An email might be the best way of notifying the player since each player's
instructions should be kept secret from other players.

Errors that occur when processing all instructions to resolve conflicts
could be displayed in an error file.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to communicate what you want to do with your boardgame pieces.
It should be possible to do everything the physical boardgame allows, such as
specifying an instruction that relies on another instruction in the same rule.
It should be impossible to cheat in the game and turn in invalid orders.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

The boardgame's system for turning in orders is already a DSL.
There are also online versions of the game.
So players would send in their instructions and a program would resolve them.
However, these games are restricted to the standard map in Diplomacy.
The group that I interviewed generates their own maps to accomodate more players
than the original game allows.
So they would need a more flexible system for their game.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Since Diplomacy already has a syntax for submitting instructions, it would be
best to use the same syntax.
However, we would need to create an intuitive interface to store the map.
A map can be easily translated into a graph and 
there are a lot of ways of representing graphs.
So I think it would not be too difficult to choose a representation and build
an interface for entering the map's data.

There would not be a lot of work in sorting out semantics since the game
has clear rules on which moves are valid and on resolving conflicts.

### Scope
_How big an idea is this? How ambitious is this project?_

The project is not very ambitious.
The bulk of the work would be in designing an interface for entering the map
into the program.
Since the DSL has a very clear use, the scope is clear.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

The project would be a good idea because I have a set group of people that
I would be designing this for.
On the other hand, this group may be too small and specific. 
I would not experience making tough decisions on ambiguous naming since I have a
group I could poll for every design decision.

The project seems to be two DSLs. 
The first one the game already specified and the second one would be for 
representing a map.
So the project may be too simple.

