# Free project 2


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Currently, the competetive Pokémon meta has grown very stale, with the same
pokémon on each team. I think that this is partially due to the complexity of
differnt builds and values leading to such a huge variety of thigns that might
work, that players find it hard to find new viable builds. In addition, testing
new theories is a very time consuming process. Hopefully, this could speed up
testing.


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A language to specify the moves and values of a pokémon could be very useful as
it would allow the user to see what the effect would be by replacing a move or
redistributing Effort Values.


### Why you?
_What excites you about this idea? How did you come up with it?_

I came up with this idea mostly because I had been thinking about Pokémon a
lot due to [proposal 1](free-1.md).


### Domain
_Describe the project's domain in five words._

Simulating battles by various pokémon.


### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

The user would want to fully specify each of the 6 Pokémon (e.g. moves, EVs,
IVs, Abilities) in their team as well as the structure of the simulation (e.g.
10 different opponents, each fought 10 times).

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

The interpreter would read the team, then simulate various battles against
random opponents. Maybe the user could also specify a team to play against.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

Testing different pokémon's effectiveness against different opponents or on
different teams should be easy. Controlling the simulation should also be easy.
Everything else hard or impossible.


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I wasn't able to find any.
[Smogon University](https://github.com/Zarel/Pokemon-Showdown) has some nice
human-readable syntax for specifying a Pokémon
```
Ampharos @ Ampharosite
Ability: Static
EVs: 252 HP / 252 Def / 4 SpA
Bold Nature
- Rest
- Sleep Talk
- Volt Switch
- Dragon Pulse
```
[Pokémon Showdown](http://pokemonshowdown.com/) is the leader in simulating
battles, and they have their own internal representation, but not a DSL.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Hopefully, the system wouldn't take too much time as the simulation can just be
relegated to Pokémon Showdown. However, from experience I can guess working with
that API will not be as simple as one would hope. It might be interesting to focus
on the language. Since this is intended for comparisons, we might only specify what
is different rather than everything like Smogon.


### Scope
_How big an idea is this? How ambitious is this project?_

I think this project might be small in intention, but end up being quite
large for the wrong reasons.


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

I don't think this would be a good project as it would probably end up being very
much about the implementation and not the design.
