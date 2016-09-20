# Free project 1

Calendar DSL

## The user and a language
This section describes who the project would serve and why a language might be
a good way to meet their needs.

### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

A calendar DSL would help people schedule events in a more efficient and less
error-prone manner.  There are many times when people must schedule lots of
events on a calendar end up performing many repetitive tasks.  For example, at
the beginning of the school year, students often input all of their classes into
a Google Calendar.  Many of these classes have similar traits, but as far as I
know, using the Google Calendar App on my phone, there is no easy way of adding
many different types of the same event.  Therefore, if you want to, for example,
set a notification 5 minutes before your class started, you would have to
manually change the settings from the default version for each class.  With a
DSL, students and professionals alike would be able to add events in a much more
intuitive and efficient way.


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

Some sort of automation would be helpful to expedite the process of adding
class/meetings to your schedule, as I mentioned above.  A general purpose
language would solve this problem, but would be much less intuitive for users. 
With a DSL, you could create primitives like "daily" or "weekly" that would
help bridge the gap between the code and the semantic model.  In addition, many
people who might use this app might not be familiar with coding.  Therefore, it
would be easier to introduce them to a smaller set of keywords and syntax that
are specific to the use.  Also, you could build some underlying machinery into
the DSL, for example a function that allows you to display the calendar.  This
would be very hard to do in a general-purpose programming language, but
hopefully with a DSL you could extract the details away into a primitive (An
API would achieve the same result here, but would not be as useful for the
reasons previously mentioned).

### Why you?
_What excites you about this idea? How did you come up with it?_

I first heard of this idea during a coding interview, and it seemed like a very
practical idea.  I am mostly interested in it because, as I was adding all of my
classes to my schedule this year, I had to do many similar and tedious tasks. 
For each event, after I specified the title, location, and start and end time,
I had to:

    1. Press "View More Options"
    2. Press Repeat -> Weekly
    3. Change the end date from 2021: 
        a.  Switch from monthly to yearly view
        b.  Change the Month from Sept to December
        c.  Change the year from 2021 to 2016
        d.  Click save 
    4. Press "Reminder"
    5. Change the option from the default to "5 mins before"

Also, some classes (like PLs) met at different times on different days, so I had
to add a separate events with the same name and do the process over again.  At
each step, I often made a mistake and would have to go back and switch the
settings of one class to match the others.  While this experience definitely
wasn't scarring, it was frustrating enough for me to hope that there is a
better way.


### Domain
_Describe the project's domain in five words._

Scheduling events for all ages.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

The user could have an object that corresponds to a calendar.  They could also
create other objects called "events" and assign attributes to these events such
as the start time, duration, location, description, and other features that
Google Calendars offers.  To these features, a user could create object types
that would correspond to abstract classes such as "class".  This could
essentially be a list of characteristics that many events have in common, so
that you don't have to type in the same attributes for each.  In addition, you
could create more complicated ways to repeat an event.  For example, you might
want a reminder "three days before the last business day of each month" to clock
your hours, for example.  With a language, users could create this custom
constraint that would resemble primitives like "daily" or "weekly", and assign
it to different events.  This is the right way to interact with the problem
domain because it allows enough flexibility but is automated enough.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

I don't see this DSL as being especially interactive.  I imagine that each
calendar is contained in a separate program, and when a program runs, the events
are analyzed and a schedule viewer is generated.  Ideally this would not be a
static image, and you would be able to toggle between modes like "daily" and
"monthly", as you can with other calendars.  To change you calendar, you would
edit the text file and rerun the program (though it would be cool to have
real-time editing like in sbt).
Some potential errors could include scheduling events whose durations don't make
sense (e.g. 9:00am - 8:00am).  I would want the scheduler to display as many
events as possible, but also make it clear that there is an error in the code. 
Perhaps a dialog box above the calendar with a descriptive error message would
do the trick.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to create many different types of similar events and add them
to a calendar.  It should also be easy to customize when in event repeats, even
with some unusual requirements (like the example from above).  It should be
difficult to do anything other than scheduling an event.  If the result of
running a program is to display a schedule, then it seems like it would be very
difficult or impossible to do anything other than what the language intends.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I haven't heard of any other DSLs in this domain.  There exist many apps for
scheduling, so there is not a desperate need for this DSL, which could explain
why I haven't heard of one.  A quick Google search didn't turn up any promising
results.  However, [Google Calendar has an API](https://developers.google.com/google-apps/calendar/).
It seems more geared towards creating a collaborative
calendar and controlling the securities.  For example, you can delete or insert
an "access control route," or update the "Freebusy" section. I see nothing about
creating similar types of events or customizing the type of frequency.  Also, a
snippet of some example code might show why a DSL could be useful (the
following code is for retrieving an event from a calendar):

``` import
com.google.api.services.calendar.Calendar; import
com.google.api.services.calendar.model.Event;

// Initialize Calendar service with valid OAuth credentials
Calendar service = new Calendar.Builder(httpTransport, jsonFactory, credentials)
    .setApplicationName("applicationName").build();

// Retrieve an event
Event event = service.events().get('primary', "eventId").execute();

System.out.println(event.getSummary());
```

As you can see, this code is only accessible to people who are comfortable
coding, and is meant for complicated and collaborative schedule manipulation. 
This functionality would not be as useful or accessible for the average person.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

This depends on how complicated of a schedule viewer you make.  For the most
part, this project would be more "language" based.  It involves several design
decisions, such as how to encode an event or an event type.  Also, ideally users
could create new events or date ranges as is they were primitives, so this could
involve interesting design decisions.  The biggest, and I think only significant
"systems" aspect is the schedule viewer.  You could have multiple different
modes (daily, weekly, etc), allow the users to customize the event appearance 
(color,
texture, image, etc), or make it automatically update when you change the
program.

### Scope
_How big an idea is this? How ambitious is this project?_

I think this is a practical project, with several potentially ambitious add-ons.
At a minimum, you could implement the language features that I described above
with a very basic calendar graphic and create what I imagine as the most
important features. In addition to the ideas that I mentioned above, another
potential add-on could include a way to create many different schedules.  For
example, if you are working at a middle school and are assigning students to
different classes, it would be convenient to list the students in an event, as
opposed to the events for a student.  However, this could be outside the domain,
and is not a crucial feature.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This could be a good project because could have an everyday use.  It would be
convenient to have a more functional and automated scheduler than Google
Calendar.  In addition, at a first glance it seems like a reasonably sized
project.  If I have time, then I could continue to add features.  Also, it seems
to include some language aspects and some systems aspects.

On the other hand, it would not be _that_ useful.  I have been complaining a lot
about scheduling, but to be honest it only happens once very six months, and
after learning the API, the language would probably save at most 5 minutes for
my use case.  Also, there does not seem to be as much work to do on the
"language" side.  Furthermore, most of the extensions that I thought of relate
to the "systems" part i.e., making the interactive calendar graphic.
