# Free project 1

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Currently, most users of LED strip lights use the default remote to control the colors
because they don't know how to code anything better. This remote alows for a classic fade
effect or just picking a color and leaving it there. The only way to upgrade this is by
using somewhat tricky arduino/raspberry pi code which the average person with LED strip
lights doesn't know. Therefore, my idea would ideally abstract the complex electrical code
required and allow for easy customization of very fun and useful LED strip lights.  


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

To create whatever design/controls a user likes, I think a language is necessary
because there are many features to take advantage of that a simple user interface
could not handle. For example the user would need a way to integrate time and other
looping interfaces into the code if they want the lights to follow a certain pattern.
This would best be solved by a language &mdash specifically a domain specific one as
they give full responsibility to the users to create complex interactions.

### Why you?
_What excites you about this idea? How did you come up with it?_

I really like LED strip lights (I have them in my room and am working on putting
them on my longboard and car) but dont like how the only features are "fades" (going
from one color to another etc..). I want to grow this technology to allow for more
complex light creations. For example, I would love for them to know when they should
turn on and off or to put on a gentle color for sleeping. I came up with this idea at
4 am talking with a friend about how fun LED lights are. I had just ordered more and my
friend complained about how they were too repetitive. I realized maybe that could be fixed
and then double realized that maybe a DSL is the right idea.

### Domain
_Describe the project's domain in five words._

Light creations for LED strips

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

A user would interact with the language by linking together commands relevant to their goal.
I started to imagine an upgraded CS5 sound lab but related to lights and far more fluent.
I also have wanted to tinker with a language more natural and I think it might be the right
way to interact with the problem domain since it allows ease of use. On the other hand,
Loops and aspects of time could be very important to the language so maybe a more technical
approach is better. I am actually very back and forth on this. 


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When a program runs, an example of their creation can be displayed on the screen for them.
Additionally, the program would try and interact with the user to learn about which file
the code should go to and learn about when they want the light design to begin. Some obvious
errors I can think of are syntax errors and sending values to the LEDs that are invalid/too large.
I think these would be checked for during compilation to notify the user quickly.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be really easy to change the colors of LEDs, create different types of fades,
and link these fades/designs together to create a "light show" of sorts.
I also think it should be easy to use loops and conditionals in combination with the above
to create interesting effects. It should be difficult to make anything too extreme like
light effects that relate to music being played. Finally it should be impossible to
represent strings or other encodings. Also features like multi-threading or creating
designs with other objects should be impossible. I dont want any project to be possible
in this language. 


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

The only information I could find is that to control these lights you must use Arduino or
Raspberry Pi code to control the wire outputs for the LEDs. I would not consider this
a DSL in my domain but rather a DSL in the domain of all electrical engineering projects.
I think the reason why there hasnt been a DSL is either because those interested in the domain
are okay using the regular Arduino code or because it is quite a specific domain so it doesnt
seem likely to have languages created for it. 


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I think that most of this project will be working on the **language** aspects.
Once the back end methods of creating a fade function/color change function/etc..
are completed, the rest will be trying to design the language in a way that promotes
chaining commands and easily integrates aspects of looping and time to allow for complex
light effects. 


### Scope
_How big an idea is this? How ambitious is this project?_

This project could be quite ambitious. There are lots of features that could be made for the user
and it is easy to get lost in "feature creating land" instead of language design land.
However, I also think the scope is not too large since it focuses on a reletively specific
domain. 

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This could be a great idea for a project since it is very fun, allows for a lot of language design
choices, and is mainly designed around allowing the user to create complex creations with it. 
This might not be a good idea because it technically requires working with Arduino/Raspberry pi (even
though this part could realistically be ignored) and because it might be too specific of a domain
that it really is just useful for me and not a whole lot of others. 
