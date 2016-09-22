# Free project 2


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.

A DSL for keeping track of appointments across many different devices easily.
This DSL would need to be easy for the user to read and lightweight enough to
share across anything in the user's system.

### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

When interviewing people for the practice with the Hive the most common thing
the people we talked to used technology for was for their Calendar.  This idea
would be a more lightweight idea than a Calendar.  Somewhat like a cross between
using a big heavyweight Calendar application and going super lightweight and
keeping a todo list on your phone's notepad.


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL is appropriate because it could provide a nice syntactic structure so that
actions could be performed upon your appointments, such as looking up ones that
are coming up or ones that you have on some day in the future with ease.

### Why you?
_What excites you about this idea? How did you come up with it?_

It's an exciting idea because the vast majority of people now-a-days use technology
to keep track of appointments and todo's.  It could be nice to add another way
for people to do this so that they have more options.

### Domain
_Describe the project's domain in five words._

Lightweight appointment, calendar, todo, language

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

I think they would right into a structured field the various aspects of the
appointment.  Perhaps they could write it as text and we could parse it if they
write it with an appropriate structure.  Then if they wanted to query or set
some rule for an appointment or appointments they could do so via various
commands specific to the language.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

The simplest program run would just store the appointment.  A more complex run
of the program could search for appointments for some particular day or with
some particular person.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

The key feature of this langauge that could potentially make it more appealing
than the solutions currently out there must be the simplicity of writing things
down.  It should feel like you are just writing a quick note to self in a textpad.
It should be possible without too much work to perform some operations on these
appointments.  Anything not scheduling or todo related should be impossible
with this langauge.  It is not going to be designed to be a general purpose
database, but is going to be a DSL for scheduling and todos.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There are tons of things in this domain that I imagine Prof. Ben would call a DSL.
I'm not really sure if I would call apps like google Calendar and iCal DSLS, but
they are solutions for a specific domain that have meet most if not all the requirements
to be a DSL.  The improvement that this langauge would provide is that it would
be a more lightweight/easy way to write down appointments.  I always feel like
the simple create appointment view doesn't quite let me put in enough info
and clicking through to the detailed view is "a lot of work" (well feels like
it sometimes...).

## The Project
This section examines whether the idea makes for a good CS 111 project.

I think this could make for an interesting CS111 project. There is a nice design
element to it and there would also be some but not a huge amount of implementation
to work out.

### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I think maybe 60/40 design to implementation.  

### Scope
_How big an idea is this? How ambitious is this project?_

I think this is a fairly small project.  There could be a fair amount of design
work to think and ask people about what the best way(s) they want to be able
to input appointments are, but once that is done I don't think it would be too
hard to allow some operations to be performed on that since the user will be
entering in text and text is typically easy to process.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This might be a good idea for a project because everyone could have an interest
in using it.  Conversely it could be a bad idea for a project because everyone
may already have a soluiton that they are quite used to and works well enough for
them.