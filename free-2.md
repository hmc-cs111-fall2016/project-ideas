# Free project 2


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

There is a need to compile and link C/C++ files by the software development community.
Currently, the common way of compiling and linking C/C++ code is through a DSL called
make. However, make is very very confusing to use and doesnt seem to have much fluency
so I think it really needs a revamp. If i could help them, their experience would be
much less confusing. I imagine they could easily just define the dependencies in a more
natural way than the Syntactic-Aspartame filled make. 

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL is required for this I feel. Currently lots of C/C++ rely on Make as a DSL
and I would want my DSL to not be to big a change or too uncomfortable to use meaning
a DSL is required to do this. I am sure a program could be created instead but it would
take away from the current measures in place and could even make it more complicated.
I think a DSL addresses the need since users will need to customize their files on the go
and maybe even create these make files with scripts which is only possible if it is a DSL
or has an API like a DSL.

### Why you?
_What excites you about this idea? How did you come up with it?_

I think my main relation to this is that in CS70 make files were a horrible aspect
and our groups could never figure them out. They just arent natural and I think my anger
with the current system makes me very excited to fix it. 
I came up with this when reading how a previous student recreated LaTex, another complicated
DSL, and I thought about Make and wanted to maybe fix that too!

### Domain
_Describe the project's domain in five words._

Software development program compilation/linking

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

The user might interact with the language by specifying facts about the different
C/C++ files they want to compile/link and then which compiler/tags they want to use.
I am imagining a sort of text file where these facts are entered and then the language
understands it and makes the correct calls. I think this is the right way to interact
with the language since it is similar to how make files currently work but removes
some of the more complicated aspects like having to understand exactly how to crate
the CLI calls in the make file. 

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When a program runs, the different facts written down will be accumulated to determine 
the structure of the code and then the proper compiler commands and tags will be used to
compile/link everything. I think many errors could occur with not linking proper statements
or not having all the edependiencies labeled and they would probably be communicated to 
the user during the compilation process since it may be difficult to know if a file is missing
or not. 

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

Compiling/linking programs should be extremely easy. One should be able to 
control which compiler they use and with what Command line arguments it is 
run with. Also it should be easy to tell if a mistake has been made with the
file linking process but that may be tricky to implement. Honestly it should be
impossible/difficult to do anything else. Maybe it should just be difficult
to add a looping functionality so as to allow for many files with similar names
to be looped through?

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I Google'd quite a bit to try and find any other DSL in this domain (other than Make)
and I couldn't find anything. This kind of suprises me but I guess enough people have
dealt with Make so far that it has not been worth creating another DSL for it.
Now I personally do not believe that there is nothing like Make but I could not
find it on google and that is the main way I know of discovering DSLs. There at least
doesnt seem to be any popular DSL in this domain (other than make) so I assume this is
because everyone has already implemented Make into their programs and have not wanted
to bother porting the data with another DSL. 

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

With this project I feel that 90% of the project would be trying to engineer the
***language*** aspects for it. This is because there already is a DSL called Make
which I am just tyring to improve the language aspects of. The parts of the project
that arent about language will mainly just be trying to parse the new fluency into the
current Make file fluency. 

### Scope
_How big an idea is this? How ambitious is this project?_

This is probably a very ambitious project. Make is a very large, very well developed,
and very old DSL so trying to properly port over all its features into a new lanugage/fluency
would be extremely difficult and large. The project would probably have to focus on a certain
subset of the Make domain instead of remaking the entire domain. 

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This would be a good idea because it could be very useful to the programming community
and because it would require a lot of deep thought about how to remake the language of make.
I think it might not be a good idea because it could be too large of a scope and it could be
hard to properly test if it is functioning for large projects: it would require making huge
projects to test with which involve other possible errors on my part. 
