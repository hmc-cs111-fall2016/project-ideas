# Free project 2 - Glowsticking Notation


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Glowsticking, or glowstringing, is an arts form that combines dance, 
choreography, and physics into a single performance. Basically, a person has 
two glowsticks on strings and spins them to do cool tricks. Here is a short 
[video](https://www.youtube.com/watch?v=VDdSLuj3CiI#t=15s) of what it looks 
like.

Now that you watched the video, how do you describe the motions? There are so 
many factors that make up a single trick, i.e. speed, the string's length, each 
hand's position, how far your arm extends out, which direction your body is 
turning (if at all). 

I want to create a DSL for describing glowsticking tricks. At the very least, 
it will break down complicated tricks into simple motions (like building 
blocks).


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A language can help express my idea because it can combine small motions (
building blocks) into complex tricks. That way, tricks can be described 
unambiguously. The only challenge would be understanding this language in the 
first place. 

I was inspired by juggling notations (see related work). I believe this is a 
language because users can string small building blocks together to create a 
juggling motion. It isn't readily understandable to me, but for those who do 
understand the notation, they can see how juggling tricks are performed. I 
think a similar approach can be applied to glowsticking, though glowstick 
motions are more complicated than ball trajectories.


### Why you?
_What excites you about this idea? How did you come up with it?_

I love glowsticking because it looks super cool, but the only ways to learn 
tricks are through tutorial videos or in-person. Also, I personally find it 
hard to teach others because it is difficult to describe ("the glowstick moves 
like this while your hand does this... and your other hand does something 
else... uhh..."). 

So a DSL for glowsticking notation would help me (and others) understand how 
tricks are performed. With these building blocks, I can describe new tricks, 
too!


### Domain
_Describe the project's domain in five words._

Creating notation for glowsticking choreography.


### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

Glowsticking routines consist of tricks with transitions in between. My idea is 
that tricks can be broken down into smaller motions (plus transitions). Some 
transitions can be complex depending on what tricks they follow, so transitions 
can be broken down, too. Then, once we have our building blocks, we can string 
them together. One move is followed by a transition into another move (in time) 
to create a performance routine.


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

I'm not trying to make a 3D simulator or anything like that (yet). But when a 
program runs, I want to create a visual representation of the glowsticking 
motions. This visual representation will be constructed from small motions, and 
somehow I will depict this for each hand so people can see how the hands work 
together. If I don't have enough time to make visual representations, I can 
work with text describing these small motions.

Some errors might be the user not providing enough info for a single motion. 
This is a problem because I want the motions to have enough information to be 
unambiguous. In this case, I would have to display error messages that state 
exactly what information is missing.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to describe physical movement of the hands, glowsticks, and 
body/torso. It should also be easy to string these notations together in a 
sequence.

You could make art with this (if I finish a visual representation), but there 
are other programs that can make art more easily than this.

It should be impossible or very difficult to do my Algs homework, compute 
mathematical expressions, create computer programs (in the traditional sense),  
make sounds, and do 3D simulations.


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There aren't any DSLs specifically for glowsticking (mainly because it's not a 
super popular activity), but there are some notations for dance and juggling. 
[Siteswap](https://en.wikipedia.org/wiki/Siteswap) is one example of a juggling 
notation. It has both graphical representations and state diagrams describing 
juggling patterns, or specifically, how the balls move from hand to hand.

[Labanotation](https://en.wikipedia.org/wiki/Labanotation) is a notation used 
for dance, depicting human movements using symbols representing different body 
parts. Shadings and direction symbols show how a particular body part moves. 
These symbols are then sequenced along a time axis to show the duration of a 
particular movement. I think Labanotation is close to what I'm looking for. 
However, I don't need as much attention to leg movements, and more importantly, 
figuring out how glowsticks are notated will be a huge challenge.


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I think the "systems" aspect is relatively simple, since I just have to create 
symbols and organize them to create a sequence. Making a visualization of the 
notations might be the most difficult part.

The most "language-y" part is deciding what the symbols look like. Labanotation 
seems like a good reference, but the symbols look foreign to the average 
onlooker, while my DSL should be understandable to a programmer or average user. 
This will probably take up a lot of time, especially since the quality and 
intuitiveness of visualizations can vary per person.


### Scope
_How big an idea is this? How ambitious is this project?_

As long as I avoid 3D simulations, this project should be within the scope of a 
half-semester. It is a much bigger idea than juggling notations or 
Labanotation, mainly because glowsticking has so many variables to keep track 
of. 


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This is a good idea because I can create a grammar for something that cannot be 
explained well currently. Also, I have references such as Labanotation to look 
at, so I feel better knowing that dance notations are possible to create and 
use.

This might be a bad idea because I don't know anyone else who would use this. 
Glowsticking isn't widely popular to begin with. Thus, I run the risk of making 
things convenient for only me.

