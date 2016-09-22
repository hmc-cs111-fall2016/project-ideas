# No computer project - Gymnastics scoring system


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Gymnastics, diving, and figure skating are Olympic sports with seemingly 
ambiguous scoring systems. Part of the ambiguity comes from the subjective 
nature of artistic sports, but the part comes from spectators who don't know 
how scoring works and therefore make a hissy fit when their favorite people 
lose.

While I can't stop hissy fits, I will show how a DSL can help rank moves and 
how that translates into points. For now, I will focus on gymnastics since it 
is the most popular "subjective" Olympic sport.


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

This isn't just a rulebook. A language can help describe the moves (and its 
corresponding point values). Moreover, shaky transitions can lower the score 
and spiral into poorly executed moves. Essentially, I want to clarify how 
scores are calculated and how each move contributes to he overall score. This 
idea is very domain-specific, as it only pertains to gymnastics or other 
artistic sports.


### Why you?
_What excites you about this idea? How did you come up with it?_

I am a mere spectator of Olympic gymnastics, and I actually have no clue how 
gymnastics scoring works. But non-experts complain about gymnastics all the 
time, so I don't see why I can't make a gymnastics DSL.


### Domain
_Describe the project's domain in five words._

Sectioning gymnastics scores into pieces.


### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

According to the 
[Code of Points](https://en.wikipedia.org/wiki/Code_of_Points_(artistic_gymnastics)), 
the total score consists of the D-score and E-score (difficulty and execution). 
The D-score is calculated at the start because it represents the difficulty of 
the planned routine. On the other hand, the E-score starts at 10 and decreases 
as gymnasts make errors.

I would plan to make my language so that given a difficulty score (and sequence 
of moves), judges can mark off execution points while gymnasts perform. Then, 
spectators might understand where exactly points were taken off.


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

I've been thinking about having a program run in realtime. For example, once 
the timer starts for the gymnast, judges can be prepared to take off points for 
poor execution. That way, we know exactly why the points were given at a 
specific moment.

Some errors would be the calibration between routine moves and the clock timer. 
The timing probably won't ever be perfect, but gymnasts have been practicing 
against the clock for many days, so timing won't be much an issue.

The biggest (but uncommon) error would be for a completely failed move that 
affected the rest of the performance (i.e. quit early). However, at that point, 
the judges and spectators know that the score is low and it wouldn't matter 
much at that point.



### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to keep track of where the execution score decreases 
throughout a routine.

It would be impossible to do my Algs homework, make art, make sounds, and 
anything beyond simple math and computations.


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I referred to the 
[Code of Points](https://en.wikipedia.org/wiki/Code_of_Points_(artistic_gymnastics))
Wikipedia article, which explains how gymnastics scoring works. This is a good 
guide to understanding general scoring, but it isn't enough to satiate angry 
spectators when their favorite people lose, nor is it really a language (it's 
more like a dictionary that defines the words).

I feel like there aren't any real DSLs because judging isn't meant to be public.


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

There isn't any hard systems aspects, except maybe tracking which execution 
markoff goes to which move according to time. I personally feel like there is 
little language and systems aspects, despite that neither dominate the other.

### Scope
_How big an idea is this? How ambitious is this project?_

This isn't very ambitious, and I doubt how viable this is. I'm just trying to 
find a way to more specifically encode gymnastics scoring.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This might be a good project because it can more clearly describe gymnastics 
scoring, which is confusing to some onlookers. There isn't anything overly 
complicated about this idea, so it is appropriate for a project.

One personal drawback is that I have little knowledge of gymnastics and I don't 
have much vision for this project.
