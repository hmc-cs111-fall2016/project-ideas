# No computer project

Tap code to communicate with my neighbor

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

I often want to communicate with my next-door neighbor, Ricky Pan, to coordinate
things like when he is going to dinner or ready to head to class.  However, often
he is not online, or we are both too lazy to reach our computers.  To verbally
communicate, I have to get off of my chair, leave the room, and knock on his door.
Originally, we were only about three feet away, so there should be a more
efficient way of communicating.  We have found that when we knock on the wall
adjoining our rooms, we can communicate.  So far, we have only used this to
indicate that we are present, but hypothetically we could extend this mode of
communication in to a DSL.  This would help us both communicate more efficiently. 
If we employed this DSL, we could learn important information about each others'
appetites or tiredness at an instant.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL would be more useful than our existing way of communicating because it
involves less effort.  In addition, a DSL would be better than learning, say,
Morse Code or the Vietnamese Tap Code (which encode each letter as a unique tap)
because
    
    1. It would take longer to communicate with these verbose languages
    2. It would take time to learn the all the characters
    3. We do not need as extensive of a language

### Why you?
_What excites you about this idea? How did you come up with it?_

I am interested by this idea because it will directly effect my quality of life. 
Some might think that this DSL is just a way to make people more lazy, but in my
opinion, that is the purpose of all DSLs.  Programming languages so that humans
don't have to go through the effort to think of their effort in binary or machine
code, and similarly, this DSL would mean that we have to expend less energy doing
routine tasks.  I came up with this idea as I was sitting at my desk and wanted to
communicate with Ricky.  It seemed like their ought to be a way to get his tell
and receive messages both immediately and in the comfort of my room.  However, the
best I could muster was a sharp knock, alerting him that I had something relevant
to say before I went next door.  If we had a DSL, we could have carried out the
entire conversation through the wall.

### Domain
_Describe the project's domain in five words._

Communication between neighboring college students.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

In this language, a program would look like a set of vocabulary (consisting of
taps) strung together by a grammar that would convey the semantic model.  We would
already have a set of primitives that would correspond to the most important words
(perhaps hungry, tired, ready, etc).  There would also be intensifiers (very). 
This is the best way to interact for our domain because it conserves energy and
elicits an instance response.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When a program runs, the participant taps on the wall, and the user listens for
the message.  There are many possible sources of error, as hitting a wall is not
an optimal medium for communication.  The listener could indicate an error by
slamming the wall, interrupting the tapper and suggesting that he repeat the
message.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be very easy to indicate the emotions that we choose as primitives of
the language.  It should also be easy to indicate times like "in 10 minutes", or
"at 1 pm", since these seem necessary for planning outings.  Ideally, it should
also be possible to define new words for the language, but this would most easily
be done through conversations outside of our language.  Therefore, I would not
include creating new words as part of the DSL.  It should be very hard to engage
in complicated, philosophical discussions.  If we wanted to, we could include the
Vietnamese Tap Code to allow us to communicate in a different language, just as
how you can include in-line assembly code in C.  This would make it possible to
have more verbose conversations, but certainly quite difficult.  For basic
purposes, this feature seems unnecessary.


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There are related modes of communication that involve tapping, like Morse Code or
the Vietnamese Tap Code that American prisoners of war used to communicate between
cell blocks.  However, I would argue that they are not really domain-specific. 
Both these examples are merely translations from the alphabet into a sound, and it
is possible to express any idea.  It is not easier to describe any particular
domain per se using just Morse Code, so it is not domain specific (unless you
argue that the domain is "short messages", which seems somewhat broad).  It also
doesn't fit into our model of unambiguity, much like how we don't consider natural
language to be a DSL.  Our dorm tap code would be an improvement because it would
allow us to express our ideas more concisely than spelling out each letter
individually.  I doubt that there are other DSLs analogous to this because the
entire purpose of the language is to conserve energy; therefore, this domain is
the least likely to go through the effort of defining the language.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

All of the work would go into directly engaging in the language aspects of the
project.  There is no systems aspect that I can think of (what would the "systems"
aspect even represent in this domain?).  Creating the language would definitely
be tricky, as we would struggle to balance the size of the language with
concision.  It would be tempting to constantly add new words and grammar to make
it closer to what we could express in natural language, but this would cause our
messages to be longer and harder to understand.

### Scope
_How big an idea is this? How ambitious is this project?_

This project has a pretty small scope.  There is a relatively small set of
"crucial" information, and we could convert it to taps using an arbitrary map. 
The grammar would also be relatively simple.  Both of these aspects seem like
decisions we could make within an hour.  We could then test out the code an make
changes to the language as we see fit.  Since the scope is so small, and we have
the aid of natural communication, I don't see this as a very ambitious project.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This could be an interesting project because it involves applying our DSL
knowledge to a non-computer-related example.  Also, if it proved successful then
our tap system would have uses between neighbors all around the Claremont
Colleges.

However, I do not think this would make a very good CS111 project.  As the
previous question addressed, the scope of the project is relatively small, and it
seems like something that could be determined over the course of a night instead
of for several weeks.  In addition, I would not get to apply CS knowledge to this
project, which is a major focus of the course.
