# Free project 3

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

This idea has to do with asynchronous tasks. It's not super well fleshed out,
but I know it will be something similar to cron, but making it very
easy to automate tasks.

I've never used cron myself (I would definitely try it out before I try to
make a new version or anything), but I've heard that it can be a bit
clunky and not super intuitive to learn.  Hopefully anyone who needs to
fire off tasks to run at intervals would be able to use a more friendly
software to do so.

### Why you?
_What excites you about this idea? How did you come up with it?_

I would be excited for the results of the language, being able to just
write a quick description of what to run, how, and when, and have it
just run when it should.  I would also be excited to learn a bit more
about how cron works and the best way to abstract cron functionality
into abstract language concepts.
### Domain
_Describe the project's domain in five words._

Assign tasks asynchronously with delays.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

I would like to support at least as much functionality as cron,
that is, to run some executable or process periodically, but also
some ability to do conditional operations:
```
if /dev/usb0 exists:
  do once:
    echo 'A usb device was plugged in'
```

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When a program runs, it should create a cron job that fulfills the given
requirements.  It could also run a background process that periodically
queries the state of the computer (if conditional jobs were present in
the input program) to see if a new process needed to be created for
the given job.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to create periodic process and to create a monitoring
process.  It should be more difficult to create jobs that are too interactive
since it could be difficult if multiple were triggered at the same
time, so we might consider restricting to background processes.  It should
be impossible for user error (or creator's error) to create too many processes
which would overwhelm the processor or take up too many resources.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

Yes, it seems that many people already beat me to it:
 * [timely](https://github.com/Factual/timely)
 * [scheduling](https://dzone.com/articles/building-dsl-scheduling-tasks)
They seem to address the need quite effectively, which makes me think that my
DSL project seem as thought it might be superfluous.

I like how the DZone project focuses extensively on fluency and composability
of the DSL designed.  It helped give me ideas for how to represent the
conditions where a task starts when a condition is met, and clarifies whether
or not this repeats or is a single trigger once the condition is satisfied.

## The Project
This section examines whether the idea makes for a good CS 111 project.

### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I think that less than half of the time working on this project would be
involved in language design, since the implementation details of the project
might be a bit gnarly.  I would expect that the query and spin style of the
language might be a particularly difficult part to handle, especially if
it involves interacting with different operating systems.

### Scope
_How big an idea is this? How ambitious is this project?_

This seems like it would be quite a significant DSL and a serious time
commitment, but largeley due to the non-design portions of the implementaiton.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

It seemed like it might be a good idea because it seems to perfom a useful
function.

However, as I have made my way through these questions I've grown closer to the
conclusion that it would not make a great project for cs111 because of its
rather large scope and emphasis on non-design elements.

