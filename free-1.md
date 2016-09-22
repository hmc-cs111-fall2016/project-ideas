# Free project 1

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Since Twitch Plays Pokemon began in 2014, there has been lots of interest
in creating similar "crowdplay" games. However, it is an area primarily
done by people willing to overcome the steep curve of learning how to interface
with emulators and Twitch's API. A DSL could help people who would have previously
been excluded from making a "Twitch Plays"


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL is appropriate for multiple reasons. We are focusing on a specific domain,
listening and executing Twitch chat commands. In addition, we are attempting to
make that one domain extremely easy while allowing for everything else to be
hard or impossible.


### Why you?
_What excites you about this idea? How did you come up with it?_

I was a big fan of the original Twitch Plays Pokemon and I was excited to see
other people continue the tradition, but no one did. I attribute this
significantly to the difficulty in creating such a project.


### Domain
_Describe the project's domain in five words._

Crowdsourcing video gameplay via Twitch.


### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

I was imagining the language as a declarative one. There is a lot of repetitive
things in running something like this (connecting to chat, running a scraper,
sending input to the game) that only differ in parameter, not implementation.


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

The interpreter would read the program to figure out its parameters. It would
then launch the game and start a Twitch stream of it. It would then start
continuously reading chat looking for commands and sending the input to the
game.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

Specifying what game and what commands can be said in chat to interact with
the game should be very easy. Pretty much anything else should be hard. Unless
the "game" you specify is Eclipse.


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There are plenty of Twitch bots that allow chat to interact with the stream, 
such as by suggesting what music should be played. A popular one is
[Moobot](http://twitch.moobot.tv/). There is also a lot of work by the
Tool Assisted Speedrun (TAS) community on scripting (
[usually in Lua](http://tasvideos.org/LuaScripting.html)) to interact
with games. However, as far as I know, there hasn't been work to bridge the
two.


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I think time would be split more towards systems at the beginning, when making an
MVP. But once we progress past single command=single input, I have been extremely
conflicted about how to deal with any kind of global state or conditionals, which
can be very important in some games.


### Scope
_How big an idea is this? How ambitious is this project?_

This is a project that should be relatively easy to get something working, but new
features could be added and the language grow to whatever size I want.


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This is a good idea as I am excited about it, there are a couple of interesting
language decisions I would enjoy grappling with, and I think it could be very
beneficial to people who are interested in crowdsourcing a game.

