# Free project 2


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Mudders get a lot of email. 
Many people subscribe to dorm chats and occasionally receive
email with interesting content but a lot of times they get useless
emails (these range from counting threads, to emails asking for rides from
airports, and to ASHMC senate summary emails).

As an example, these are a series of emails sent to a certain dorm's chat
list

![EDC emails](/images/emails.png)

people would want emails at the top of the list and the bottom of the list.
However, all of the emails in between sent over a few hours, would be 
undesirable.

A language for filtering emails with enough flexibility in configuration could
cut down on these unwanted emails reaching their inboxes. The emails could
instead be redirected towards a folder for them to check occasionally.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL would allow for more customization in order to effectively
filter out emails. 
This customization is key since different users would want to receive and 
filter out different types of emails.
The customization could also be used to specifically target types of emails.
For example, a user could specify that they do not want emails that only contain
numbers and a sign-off. 
This would then filter out counting threads.

### Why you?
_What excites you about this idea? How did you come up with it?_

I don't mind nonsensical emails from dorm chats but a lot of people do.
I would be happy to help people eliminate annoyances in their lives.

I came up with the idea when someone mentioned that another person has a really
complex email filtration system.

### Domain
_Describe the project's domain in five words._

Filter out unwanted email types.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

The user would write a configuration file. This file would contain something
like

```
name: "ISO war"
keywords: ["ISO"]
start-frequency: 60
start-count: 3
step-frequency: 3600
to: "ISO"
```

This means, filter out emails that are considered to be "ISO war" emails. These
emails contain the word "ISO". 
Filter them out if more than 3 such emails are 
sent over the course of 60 seconds and continue filtering them out until the 
frequency drops below 1 email per 3600 seconds. 
These filtered emails should go to a folder labeled "ISO".

A configuration file using JSON or XML-like syntax would give the system a good
level of customization, provided that the language has enough keys.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

The user would run a command, maybe in the command line, to start the program.
The program reads the configuration file and continuously reads incoming emails.
It would filter emails that should be filtered at all times and it would
filter emails once certain criteria (such as emails per second) are 
triggered.

Syntax errors could occur if users try to use a key that the program does not
recognize. This error should be displayed after the user enters the command. 

There could be a lot of silent errors where the program misinterprets the user's
input and simply fails to filter out the specified emails or filters out emails
the user wants to receive. It would be on the user to identify these errors.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to identify types of emails based on keywords and regular
expressions.

It should be possible to identify emails that require a frequency threshold.

It should be impossible to do anything outside of filtering out emails,
such as using loops.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

The [Gmail API](https://developers.google.com/gmail/api/guides/filter_settings)
has XML files that do a similar thing. 
The API has good fluency and descriptive variable names.
But since the syntax is based on Gmail's search syntax, it cannot take into 
account factors such as email frequency.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Since these criteria are most easily described in natural language, it would
be a significant challenge translating it into code.
So a lot of time would need to be dedicated to syntax and naming.

However, semantics would also be difficult as the program would need to
interact with an email client in a secure way.
Another challenge in semantics would be natural language processing problems 
that may be required in order to filter things such as counting threads.

### Scope
_How big an idea is this? How ambitious is this project?_

Due to the challenges in communicating with an email client and my unfamiliarity
with NLP, this would be an ambitious project for me. The problem is quite open-
ended so it would also be a challenge to determine how much the DSL should be
able to handle.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This would be a good idea because there would need to be a lot of language
decisions in terms of syntax, since I would prefer to not use an XML
configuration file interface.
There would also be a lot of design decisions with naming.

However, this project definitely tends towards the API side of the DSL spectrum.
It is also a really ambitious project, in addition to all the work for 
designing the language, there would have to be a lot of work to get the
semantics to work.

