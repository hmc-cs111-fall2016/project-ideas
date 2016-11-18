# Free project 2


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

When I am scheduling things, I often need to figure out when I am free. It is
hard to get that information at a glance when looking at my calendar. To do that
right now, I have to meticulously go through each item on the calendar, noting
down each open slot: two hours on Monday, then two different three hour slots on
Tuesday, etc. It is slow and excruciating.
My DSL will solve this problem. After inputing all calendar times, this DSL
should be able to output "free times", which will instantly let the user know
which times they can use to plan activities, meetings, nap, etc.


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

This depends on how you define a "language". I imagine two different ways to
show the free times. They can either be in the form of words, and can be in JSON
or some other format so other applications can consume that data. Or, like most
calendars, they can appear in a visual time block. This can either be done as a
plugin on top of Google Calendar or its own calendar (though that would be more
complex).

### Why you?
_What excites you about this idea? How did you come up with it?_

I have been doing a lot of interview planning, and it is tiring to repeatedly
look at my calendar and give my free times to recruiters. This would have saved
a lot of my time during recruiting season.

### Domain
_Describe the project's domain in five words._

Shows my free time easily


### Interface (syntax)
_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

The user would interact with the language by typing and giving it constraints.
Programming would look like giving constraints like "1hour 1pm 5pm 10/15 10/31",
which means any hour-long time between 1pm and 5pm between 10/15 and 10/31 that
the user is free. It makes sense to give constraints like this as they are easy,
succint, and logical. This is better than having to click a GUI and select
constraints - though that option should not be ruled out.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

The program will take the constraints given and query the users calendar and
return a list of times that fit the constraints that are also free (no planned
activities in that time). The program takes in the constraints from the user and
returns the list of free times. The errors that might occur are when there are
no times to return (if that can be considered an error), if the constraints are
ill-formed (if you want times between 1pm and 5pm but put in `5pm 1pm` instead),
or if the querying of the user calendar (i.e. through Google Calendar API)
fails. The first one should be an expected condition, so an empty list or "no
free time available" can be printed. The second one should be easy to
communicate as well, as when parsing this error should be obvious. For the last
one it will depend how the parsing fails - is the internet not plugged in? Is
the API broken? Did the API return with an error? I assume those can be passed
down to the user as well or at somepoint the DSL should interpret it as a query
error of some sort.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to query for free times that fit the user-inputted
constraints. It should be possible but difficult to do other kind of calendar-
related work (not sure what that might be, but maybe adding events or checking
for busy times instead of free times). It should be impossible to do non-
calendar-related work.


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

The obvious DSL is the traditional calendar itself. Google Calendar and iCal all
provide great DSLs for planning in general. For this specific use-case, however,
I think they do not do as well. As I describe before, it is painful to look at
the calendar and events each day, tally up the free times and see which ones
work. It isn't impossible to do, but it is not easy, fast, or pleasant to do.
Calendars are greate when you need to see what you're doing for the day, plan
where you'll be, etc. as they give you a great reference. It would be great,
for example, if Google Calendar could highlight all the user's free time, then
it would do better in this use case.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

A lot of the decisions would be coming from the language aspects of the project.
Since this will be about what constraints the users can put in, that will affect
this project a lot. The systems aspect of the project will not be as important,
except for what the DSL does with the list of queried times from the user's
calendar. That should be fairly simple - iterating through a list and tallying
times should be quick, even if implemented badly! However, choosing the right
language for the user, and giving the users the appropriate syntax and language
to do what they want to do will be key to how this DSL works!

### Scope
_How big an idea is this? How ambitious is this project?_

This could have a large scope depending on what kind of constraints are allowed.
If it's just a simple, this date to this date during this time, then it is not
a very large scope. However if you start allowing language like "10/15 10/31 on
weekdays" or something, then this starts becoming a little more challenging.
Recurrence could also make it interesting, i.e. "first Monday of every month" or
something. Simply adding these cases would make the program have larger scope,
language-wise and implementation-wise.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea
project?_

This might be a good idea because I know I want it and I want to use it. This
might not be a good idea because potentially the scope might be too small.


