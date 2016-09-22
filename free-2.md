# Free project 2


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

_Right now, Mudd freshman must use a Python interface to learn the made up,
similar to assembly, programming language HMMM. This interface requires
students to carefully construct their program because they cannot easily
go back and change line numbers (that they must hand type for each line).
Hopefully, my language would be able to make using HMMM a lot more 
accessible and user-friendly._


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

_Right now HMMM is a language and students will hopefully still work with
it as a language because that is what users are comfortable with. Hopefully,
this will just be an improvement on the original language._

### Why you?
_What excites you about this idea? How did you come up with it?_
_Addressing one of my biggest pet peeves of CS5/42 makes me really excited
and knowing that it could help students feel more comfortable with a topic
of the into CS class that can be confusing._  
_I came up with it by talking to some friends. I asked for their help with
something that is impossible in my language for free-1. One of them jokingly
mentioned HMMM (which would have, indeed, been impossible). However, we 
started talking about how terrible it was to program in HMMM because of the
line numbers, the difficult debugging, and other problems. So, I figured
that one option would be to rewrite HMMM, fixing these problems._

### Domain
_Describe the project's domain in five words._

_Simplified assembly for learning CS_

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

_The user will interact with this language by writing a pseudo-assembly
code. The programs will look like lines of assembly code. However,
HMMM only knows about a handful of commands. So, each line should be
one of these commands. This is the right way to interact with the domain
because it will let students learn the ideas of assembly without being
overwhlemed by actual assembly and all the "gotchas" that come with that._

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

_When a program runs, it will take the users input and run it based on the
rules that we have written. It will interact with the user because the user
will tell the language the program that they want to run and the language
will give the user the output. It could get errors that it cannot run the
program because it does not know a command or the command does not have the
right inputs. Hopefully, it would be able to comminicate to the user the
lines that that occured and which of these problems it is._

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

_It should be easy to write simple programs in assembly. It would be difficult
yet possible to write recursion in assembly. It would be impossible to create
data structures in this language._

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

_Right now, there is the current implementation of HMMM. It can be found here:
https://www.cs.hmc.edu/~cs5grad/cs5/hmmm/documentation/documentation.html. I
really admire that it keeps it simple. Right now, there are only 23 instructions,
which makes it easy for students to have a reference guide of what each
instruction is. I think the languages' debugging could be better. Right now,
students must either dump memory or print registers. I would be interested in
seeing if there are better ways to debug (not print out the full memory or 
have an easier way to make automatic breakpoints). I would also be interested
in how possible it is to remove the line numbers._

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

_Most of the work would be on design decision because most of the language has
already been implemented. So, the basics are there. In recreating the language,
I would be focused on trying to find different ways to make the language more user
friendly, hopefully with lots of input from freshman, CS5 students, and Prof
Dodds._

### Scope
_How big an idea is this? How ambitious is this project?_

_This project does not have a huge scope. Most of the documentation discusses
how they have implemented HMMM and they include all the files necessary to
learn how they implemented HMMM. So, adding the possible new features and 
would be the largest part of the project. However, I think that the scope of
this project can grow as I talk to more people about features that they would
want to see and see how difficult these implementations are._

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

_This would be a good idea for a project because it's already implemented in
Python, a language I am very comfortable with. Additionally, almost all Mudd
students have seen this language and the freshmen will have just used this
language right as I am working on this project, so I will have a large pool
of people to gain feedback from as I am working._  
_This may not be such a good idea because I'm not certain how possible it is.
It is quite possible that someone has already tried to do some of the updates
that I have thought of to HMMM and they were simply not possible. Additionally,
the scope may be a little small. I worry that there will not be enough to do._
