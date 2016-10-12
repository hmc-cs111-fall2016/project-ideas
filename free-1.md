# Loop Animate

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

My first idea is for a DSL that allows the user to create simple looping 
animations. This DSL meets the need of inspiring creativity through code! It
allows users to create animated art work through simple programming. Animation 
can be a very tedious and intimidating process for those who don't have strong 
drawing skills or experience with the Adobe Creative Suite. In other words, 
animation seems out of reach for those who don't really have an art background 
and are just casually interested in animation. This DSL allows for users to 
create cool animations with very little to no background in drawing or coding! 
I imagine it would be a great learning tool for kids, inspiring interest in 
the fields of both Computer Science and Art.


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL would allow the user to more easily create looping animations. For 
example, it's likely easier to define and add animations to large number of 
shapes through code than through manually drawing them or adding new shapes
through some sort of GUI. It addresses the desire to create interesting 
looping patterns and movements with a relatively little investment in time.


### Why you?
_What excites you about this idea? How did you come up with it?_

I'm excited by this idea because I'm personally interested in learning 
about animation but have very little experience with it! I created very 
minor animations using Unity this summer, but found it to be a rather 
painstaking process and required a great deal of time and patience to 
learn. I reflected on this experience and thought about how a DSL could
be used to facilitate this process. I thought back to our first assignment 
with ContextFree, and I thought it would be cool to apply principles of this
DSL in creating a new DSL that allows for animations.


### Domain
_Describe the project's domain in five words._

Digital art with looping animations


### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_

I want to keep to commands as simple as possible, so there would be a small
set of defined shapes, which the user would instantiate as objects. The 
properties of the object could be modified (i.e. color and size), and the
objects could be easily modified. There would also be a set of animation
methods, which could allow shapes to float across the screen, rotate in place,
and gradually change size/color. The user would call methods on the objects 
and they could specifiy the intervals at which the methods would be called.
I imagine the interface looking similar to ContextFree, where the user writes 
code in one part of the window, and the result of compiled code appears next 
to it. This would be a good way for the user to immediately see the results
of their animations, and modify them as necessary.


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

The user could incrementally see the progress of their animations, by compiling
the code and the result being displayed right next to it. This gives the user
the immediate satisfaction of being able to see their coded creations. It is 
likely that the user will make syntax errors, perhaps having invalid parameters 
for the shapes and methods. Errors will be identified at compile time; the 
animations won't be generated if there are syntax errors, which would hopefully 
be highlighted in the code. 

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to create simply shapes and animate them! There should be
room to also generate more complex combinations of shapes and animations so
that more experienced users won't be bored. I imagine it would be possible
to create less loop-like animations and longer story-like animations, but it
would take a lot of work and at that point it would be better for the user to
use established animation software. It would be difficult to do anything other
than animated art, like solving mathematical functions. It would be impossible
to do something like parsing text or composing a song.


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

[Processing](https://processing.org/) is a DSL that is very similar to the type 
of language I want to create. It is a language for "learning how to code within
the context of the visual arts", and it allows the user to create still digital
art as well as animated digital art. There are many libraries that extend the
language, showing its extensibility and success as a readable and writable
language. I actually think this DSL addresses the desire to create art and
animation very effectively, and I wish I had known more about this before! I 
suppose a drawback of the language is that it has such a wide range of features
that it might require some investment of time to become proficient with the
language, and it is not necessarily the most intuitive for those who have
never programmed before.

Another interesting program I found, which is much simpler than Processing and
has a very intuitive GUI is Kaleidoscope, featured on Google's [Made with Code](https://www.madewithcode.com/projects/art).
It allows the user to drag and drop shapes and select the animation they want from 
a drop down menu. Unlike Processing, the range of features is very limited and there 
isn't too much customization the user can do. 

For the purposes of my DSL and to not replicate the awesome work that's already 
been done, it might be cool to combine the simplicity of the GUI of Kaleidoscope
and the customizable nature of Processing to have a sort of intermediate DSL that
is both intuitive and expandable.


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I think around 50 percent of the time would be spent on desigining the language.
I feel like it will be fairly simple to define terms of the lanugage, especially
because coding languages for visual art already exist and I would be able to model
aspects of my language after those. However, I think I'll need to make important 
design decisions on how the the code can be organized from the user end (i.e. 
creating classes or separate files). I also think I'll need to decide how simple
the language will be, either by limiting the vocabulary or by limiting the
parameters for different objects.

The other half of the time will be spent figuring out how to parse and execute 
the code, figuring out how the shapes and animations will be represented on the 
screen. I'll need to do some research on which language would be the best one 
to implement my DSL and determine what can feasibly be animated. I'll also 
need to decide what kind of user interface to create to allow the user to see
the result of their code.


### Scope
_How big an idea is this? How ambitious is this project?_

I would say this project is quite ambitious, particularly for me because I've
never done my own coding project before and I don't feel exceptionally proficient
in any programming language. Also, I don't particularly have much knowledge in this
domain, so it would require a lot of initial research on my part to figure out what
would be feasible to implement. So it feels like a big idea because it requires a 
lot of work both in desigining the language and designing the interface for the user 
to execute the language, but I think there will be a lot of resources that would 
help me carry out this project.


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

In the process of fleshing out this idea, I realized that Processing
language already has a lot of the characteristics that I wanted to have for my
language. So I question whether this DSL would be a productive thing to make,
since people who are interested in this domain can just learn Processing. However,
as a learning experience, I think it would be fun and very feasible to implement,
since I can use existing DSL's like Processing and try to replicate the feautures and
possibly add new ones. A potential possibiliy is that I can create an internal DSL for
Processing so that it can help people who are already interested and invested in the 
domain. So all in all, I'm not sure I'll stick with this original idea because I feel 
like I should create something more novel, but the idea of creating a DSL for
Processing is now very intriguing to me. 
