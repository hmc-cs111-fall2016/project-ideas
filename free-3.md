# Free project 3

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.

A DSL to describe video game tactics. This would help newer plays learn from more
experienced players by providing experienced players a way to share tactical or
strategic advice.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

The need met by this idea is the need to learn how to play games better. I'd be
helping people who want share their strategies with others and those who want
to learn.


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL could be appropriate because it would provide a way for users to compare
between different tactics and strategies.  In some games it could also help users
understand losses by looking up the strategies that were used against them.

### Why you?
_What excites you about this idea? How did you come up with it?_

This excites me because gaming is very fun and exciting and it's an activity that
I love to do.  I think a number of Mudders also like games so it could be an idea
that people here might think is fun.  Moreover there are many games that I am so
clueless to the tactics, such as the game Diplomacy, that I can't really play well
enought to enjoy.  If there was an easy way to learn or read about tactics it would
increase the number of games people would be interested in playing.

### Domain
_Describe the project's domain in five words._

Gaming strategy and tactic descriptions

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

A user would either write a strategy or read a strategy or search for a strategy.
The reason this could be the right way to interact with the problem domain is that
it could provide a simplified manner to undestand strategies. Currently in many
games people will share their thoughts on streams like [Twith](http://www.twitch.tv)
but there is not an organized collected place to view these strategies.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

The program running would be people reading or searching for strategies.  An error
that could occur is that someone could write a very ineffective strategy and then
the user could be learning total garbage that would not help there game.  Sadly,
the only way I can think to communicate this to the user is that they would lose
a lot of games.  Perhaps if the strategies are posted somewhere there could be a
field describing the effectiveness of the strategy and then the user could filter out
ineffective strategies.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to find, write, and read strategies.  It should be impossible
to automate strategies. The intent of the langauge is to help humans understand
the strategy not to help create bots that can play the strategy (although this
DSL would provide a great format for someone who wants to create a bot to get
ideas about how to program their bot).

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There are various forums and such that people post strategies on. There are also
books written about many more classic games.  I don't believe any of these classify
as DSL because they have no real syntactic structure (well books have English but
that's not a DSL).  I think this could be an improvement by providing some universal
standards across gamees for sharing infomration.

## The Project
This section examines whether the idea makes for a good CS 111 project.

This could be a good CS 111 project since it would require a lot of design to
make possible.  I think it is substantial enough that it would take a non trivial
amount of time to develop, but also not so difficult to implemenet that it would
take too much time.  I think we could finish it by the end of the semester.

### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

This project is mostly design I believe.  I think it would be something like 90/10
spent on engaging with the language as opposed doing the system aspects.

### Scope
_How big an idea is this? How ambitious is this project?_

I think it is pretty ambitious because I think it would require a lot of thought
into design to find a way that works for describing all games.  Perhaps all games
is too broad and we would need to focus in on some sector of games or maybe even
one specific very interesting game.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

A benefit of this project is that games are fun and played by many people so it
could be fun and applicable to work on.  A drawback is that this project is a bit
difficult for me to see a clear way to design it.  There are many parameters that
might go into a strategy and it could be difficult to design.  On the plus side,
it could be a good exersize for designing a langauge built to grow, since that
would probably be necessary as new games are designed.