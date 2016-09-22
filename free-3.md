# Free project 3

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

The need met by my idea is a need for a simple beat creation for many music genres.
I am trying to help those who casually make music and want an easy way to translate their
production ideas into an actual beat/background music. Currently, these user would either
have to learn more complicated sound design software or use things similar to the "App" 
shown in class where you draw around on a grid. Idealy, if I could help them, I would
make the beat generation simpler by allowing for the mouse clicks to be the main beat creator.


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

Most programs for sound/beat design are very complicated. I think a main reason
for this is because with a program it is easy to add a ton of features and then
dilute the program, confusing the user. A DSL would probably be appropriate because
they can be abstracted to allow for a non-technical user to easily make music.
I think a language adresses the need for easier interactions with the music. 

### Why you?
_What excites you about this idea? How did you come up with it?_

I may not be big on making music but I am a huge music fan - especially
for music that has cool beats. I also would be really enjoy plugging something
like this into speakers and freestyle with it. Additionally this idea excites
me simply because making a language like this would be really interesting.

I was thinking about a possible music DSL from the start but hadnt created
a good idea. Then at some point I was playing music really loud and kept
tapping my finger to the beat. I kinda thought it would be cool if I could
actually make music by doing that and it kinda sprung up that it could be a
DSL.

### Domain
_Describe the project's domain in five words._

Simple beat creation.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

A user would interact with the language by asking the language to record a sound
and then clicking on the page to create the sound. Idealy you could alter the pitch
of the beat by changing where you click. Also I may or may not want the user to be
able to alter the sound after recording it. Lastly, the program would record where the
button presses were made to display to the user. Programming in this language would look
a lot like clicking on a blank screen that displays where you clicked and then makes music
from it. I think this is the right way to interact with the domain because it is super simple.
A mouseclick is very intuitive/fluent for everyone who can easily use one and is a fairly
natural way of interacting with beats since many people already dance or tap to the beat.


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

I think when a program runs the user will click on some screen somewhere and the
program will record the clicks and translate it into sound. It would also display
where they clicked so they could see the pitch created. I am imagining to make
things consistent it would be good to record the user input and keep looping over it
allowing the user to make slight changes to the beat or create a new beat. The
programs only interaction with the user would probably be to play the music and
display general HOWTO information. Also the program would allow the user to move
the "beats" around. In terms of errors though, I cannot imagine any errors occuring.
Maybe if they are clicking too rapidly it could require an error which would probably
just be a popup window asking them to slow down.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to make beats and hear the beats on loop to decide if you like it.
It should also be easy to make small changes with the music without having to restart
the entire process (even though the "point" of the DSL could be that you cant alter
old beats. Im not sure yet). Other than that, most other things should be difficult/
impossible. It definitely shouldnt be possible to do calculations or interact with the
computer in non-music ways. Also, one should not be allowed to make real programs.
Just music creations. Probably just mouse. Simple background beats that can be altered
for other sounds. 

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There are some similar DSLs in this domain. The main ones would be like the one Prof. Ben
showed us in class. A great example of this is (BeatLab)[http://www.beatlab.com/create] where
you can click on a box and the program will play the sound once it gets to that part.
It addresses the need well since it is easier but I feel it is less intuitive to place
a beat on a grid instead of tapping what you feel the beat should be. It definitely has
some very admirable qualities. For example, it is easy to add many different sounds and
make it longer. Also you can easily change the sound after creating an initial beat since you
just have to click somewhere else. However, I think it could definitely be improved.
For one, it is not exactly like my idea in that it uses the grid style instead of a more
intuitive click. Also I think it can be fairly confusing using all the sounds/features it gives
the user access to: I think a simpler approach addresses the need for easy sound design. 


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

The language itself is fairly defined, just click. However what to do with the language
is not very defined. Should you be able to click and drag? How about Altering a click after
the fact. What should a scroll do and how can these all be intuitive/fluent. Basically,
there are still many language aspects of the project even if they arent as noticeable on
first glance. 

### Scope
_How big an idea is this? How ambitious is this project?_

I think this is a somewhat ambitious project. It requires many different aspects of
computer science like I/O, UI, Language Design, and sound prouduction. I also think
of it as not too large a scope though since it focuses on a fairly specific domain
and has easier fluency than some project ideas. Therefore, the project is definitely
ambitious but that doesnt mean it isnt doable. 

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This would be a good idea for a project since it makes an interesting product
and requires an interesting aspect of language design, how do you design a language
with no words? It also involves many aspects of computer science so it is definitely
a learning activity. This might be a bad idea because the language design doesnt
involve words (it can be a pro/con) and because it might not be as useful as I would hope.
