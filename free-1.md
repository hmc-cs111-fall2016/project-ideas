# Free project 1

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.

### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

This project is designed to serve individuals who need to schedule meetings
among a large group.

Currently the de-facto standards for scheduling are one
of the following two methods:
 * Everyone send out their availability for a certain time and a leader
picks the times that seem to work best for a plurality.
 * Everyone uses some software, such as a WhenIsGood&#8482; or When2Meet&#8482;
and choses a binary yes/no for each time slot.

If I was able to help them, users would be able to specify, in a way that feels
natural, their availability and preferences.  Hopefully this can reduce either
the work of an individual (who must compile the results of an email) or the
repetition inherent in painting over the same boxes for pairs of weeks when
using a WhenIsGood&#8482;.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

Since a large part of scheduling involves individuals
expressing their constraints (and hopefully preferences as well), a language
might be a good fit, since it can be tailored to allow this expressiveness
in a way that a simple calendar might not.

### Why you?
_What excites you about this idea? How did you come up with it?_

I had the idea when (during the beginning of this school year) the many
organizations of which I am a member began sending out scheduling notices,
all trying to claim spots in my schedule simultaneously.  It irked me that
there was not a better way to handle the scheduling problems, so I started
thinking about how it might be improved.

I am excited about trying to make the language integrate with existing calendar
formats, since this would involve finding a clever abstraction for all the
information which could serve as a medium between the natural / intuitive
language with which users would describe their schedule, and the highly
structured data of an exported Google Calendar or iCal instance.

### Domain
_Describe the project's domain in five words._

Scheduling with precision and integration.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

The user might provide text of the form:
```
Thursday:
  free one_hour_of(2pm - 5pm)
  free 9pm - 11pm
Friday:
  busy 12pm - 12:30pm
  busy after(7pm)
```
or combine this with a calendar document.

The user might also provide input of the form of conditionals, where the users
notes how their freedom might be impacted by other group members, etc.

This is a good method to interact with the problem domain, since it mimics
how we might naturally think about our schedule.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

The data supplied by the user (either through an intuitive language or an
exported document, or some amalgamation of the two) would be transformed to
the abstract representation of a schedule.

If there are multiple abstract representations, different operations
may be performed upon them (decided by the organizer), such as intersection,
greedy algorithms for free individuals, multiple meeting times that cover
all individuals etc.  (The language should provide a way for users to provide
a custom combination functions from modular pieces.)

It should also provide a color-coded graphical picture of the schedule
information the user input, so they can verify that the information they
provided was parsed correctly (and entered correctly).

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to describe when are the great, good, bad, and terrible
times to meet (likely default values).  It should also be possible to
express more complicated dependencies, such as a preference for a meeting
time that coincides or avoids another group member, or a freedom in a 3
hour block where only 1 block can be scheduled at a time.

It should be very difficult to do perform functions unrelated to scheduling,
such as arithmetic, nested control flow, or see implementation details.

I don't think there should be anything in between (of medium difficulty).

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

We might consider the aforementioned websites 
[WhenIsGood](http://whenisgood.net/) and
[When2Meet](http://www.when2meet.com), since they are computerized schedulers
with a specific syntax (painting over certain blocks), and associated
semantics (painted blocks are free blocks).

These DSLs are quite minimalistic (i.e. when they run, they only support the
intersection operation for the sets of times from each individual -- as far
as I can tell).  My solution to the scheduling problem might be a bit more
ambitious in the functionality it hopes to provide, but I will need to take
care during design to avoid feature creep and the complexity for users that
may entail.  Perhaps I will find that the existing websites' simplicity is
more desirable than the benefits of the features I would hope to add.

## The Project
This section examines whether the idea makes for a good CS 111 project.

### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

The underlying system should not take much implementation, it could be pretty
easily represented as a 
[protocol buffer](https://en.wikipedia.org/wiki/Protocol_Buffers)
for each individual.  The most interesting part of the project, and I would
guess that it would take at least 50% of the time, is the design of how
users should be able to input their data.

The algorithms for finding an optimal schedule could take significant work
if that were the purpose of the project, but we could provide rather modest
combining facilities and focus on making the data entry as interesting as
intuitive as possible.

We might also consider the difficulties arising from reading in information
from a potentially complicated calendar document (overlapping events, multiple
calendars, etc.) which could take a bit of time if we hoped to provide full
support for reading in arbitrary calendars.  Again, we could focus more on the
design aspects and provide less support for reading in complicated calendars.

### Scope
_How big an idea is this? How ambitious is this project?_

This is difficult to tell.  There are many possible extensions to the project that
could make it a multi-year project, but the very basic DSL should be able
to fit into a semester, as it just needs to parse dates and times and construct
an abstract and visual representation from this data.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

It might be a good idea since it does fit into a use case that many
individuals encounter on a semi-regular basis, so if it could improve that
process, it would be a great win for DSLs!

The idea might be more of an "app" than a "language" problem, witnessed by the
two "DSL" references I provided.

