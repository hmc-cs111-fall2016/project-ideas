# Free project 3

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Some people use white noise to help them concentrate or fall asleep.
Some people also have preferences based on the frequency spectrum used
to generate a noise.
For example, some prefer pink noise to white noise.
The DSL would let people customize random noise similar to white noise.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL could make it easy for someone to generate random noise and customize it
to their liking.
It is easy to find white, pink, brown, blue, violet, and grey noise but it is
harder to make noise from a different frequency spectrum.

### Why you?
_What excites you about this idea? How did you come up with it?_

I used to enjoy listening to random noise in order to fall asleep.
Now that I know more math and cs, I thought about writing a program to generate
random noise.
I've also been having trouble sleeping because I've been sick, so I thought
about random noise again.

### Domain
_Describe the project's domain in five words._

Generate random noise for relaxation.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

The interface should be graphical. Users can draw the top of a frequency 
spectrum like those displayed 
[here](https://en.wikipedia.org/wiki/Colors_of_noise).

Users can also utilize a slider to change left-right balance for stereo volume.

The graphical interface is simple to use and hopefully intuitive.
People who are interested in random noise also use colors to name noise,
so a graphical interface may be helpful for generating more complex noise.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

The program would use the currently displayed frequency spectrum to generate
noise.
The noise should stay updated as the user modifies the spectrum.
So the noise should change with the drawing without interruptions.

If an error occurs, the noise should stop as really terrible sounds could
result from the error. Then an error message should appear on the graphical
interface.

A possible error could be a strange spectrum that is discontinuous.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to generate white, pink, brown, blue, and violet noise 
since the spectra are just straight lines.
But it should be easy to make a make a preferred noise since the user gets
continuous feedback.

It should be possible to create noise of discrete frequencies, although it
should be difficult.

It would be almost impossible to make music.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There are applications that play preset colors of noise.
There are also websites like [this one](https://www.random.org/audio-noise/)
that generates random noise with some customization.
Along a similar domain, there are many websites that overlay ambient noises
like [this one](http://soundrown.com/).
I have not found an app or website that lets you customize noise based on
frequency spectrum, which may be too niche.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Due to the graphic interface, I think there is a lot of work in language
design decisions.
For example, adding color, since it's often used to describe these noises, 
could be a consideration which requires a lot of research into language.

With the right implementation language and perhaps the right library, it should
not be too difficult to implement the semantics.

### Scope
_How big an idea is this? How ambitious is this project?_

The project has a definite goal, which I don't think is too large.
Designing the user interface may be challenging, but definitely do-able.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This would be a good idea because it uses a non-conventional interface for a
DSL which could lead to interesting design decisions.
It's also a project that I would have a lot of fun using.

This may not be a good project because it may be too niche.
I might be catering too much to my own needs and preferences.

