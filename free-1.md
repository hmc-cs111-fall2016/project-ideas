# Free project 1 (Theaterical Lighting Control Language)

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

For live theaterical productions, there exists a diconnect between the language
with which one describes actor and scenic movements through space and the
lighting that illuminates that space. Currently, lighting designers will watch
a run through of the show to note where different scenic elements and actors are
over the duration of the production. They will then envision lighting cues&mdash;
shifts in the lighting&mdash;and generally describe what is happening along with
a verbal line or action that prompts the change. The lighting designer then
looks at the their light plot&mdash;a technical drawing where each lighting
instrument will be hung (and aimed) in the venue&mdash;and spits off a string
of channel numbers (or group names) to a light board operator along with a fade
time and intensity level; they are essentially translating their more
descriptive cues to a less descriptive computer form. Optionally, when
programming in the light cue which list channel numbers and intensities, the
designer *might* instruct the board operator to include a note next to the cue
specifying (in some abstract sense) what the cue is meant to achieve. When the
designer plays back the cues with the action on stage they look along on their
decriptive cue sheet and the computer version and call out more channel numbers
and intensities to edit the cues. During a show where the stage manager is
telling a board operator when to hit `GO` for the next cue does not necessarily
have a clear picture of what the cue is going to do besides taking notes and
memorizing it. This can be problematic if a cue is skipped or someone is not
in a place they are supposed to be&mdash;it makes it very difficult for the
stage manager to decide when to skip cues in these cases unless they are intimitely
familiar with each and every cue.

I imagine a different way of formally noting the cues where they both have
electric/computer significance and are human readable in order to avoid the
manual translation from abstract cues to numeric channel intensity lists. This
would not only cut down on the time a programmer and designer have to spend
programming&mdash;they'd only have to write the cues once and would have both
forms&mdash;but it would also make it clearer to the board op and stage manager
what is going on (or about to happen) in each moment of the production&mdash;especially
when "emergency" adjustments/skips need to be made.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

Currently, there exists a fairly technical vocabulary to describe lighting
scenes and another language that gets entered into the computer&mdash;lighting
designers have to currently know both, so I think it would make senese to create
a DSL that combines these two in an abstract way offering more semantic meaning
to what a designer is programming (apart from the method of manually associating
meaning).

### Why you?
_What excites you about this idea? How did you come up with it?_

I've been involved with technical theater since middle school, and I have always
been intrigued by its fusion of technology and the arts. I have sat through
a number of light programming sessions thinking to myself that it is redundent
and very time consuming. Why does a designer verbally translate what they have
written on a cue sheet into computer commands? If there was a better langugae
to do both the description and control, it would be more efficient and easier
to reflect on without constantly referring to charts and spreadsheets. Furthermore,
I have stage managed productions where the lighting designed does not make it
clear to me what each cue is set to do making it more difficult to time correctly.

First semester I was talking with someone about how it would be interesting
to create more student-led fully lit performances but dreaded the task of making
worksheets and then spending time with someone especially focused on programming
lights. I wasn't really sure of another solution, but after thinking about it in
the context of DSLs I think it would be a really engaging and useful tool.

### Domain
_Describe the project's domain in five words._

Easy, expressive theatrical light cueing.

### Interface (syntax)
_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

Instead of using an Excel spread sheet and then a lighting console with a
number pad and keywords, a lighting designer would use a full QWERTY keyboard
to formally describe the lighting scenes:

```
production: "DSLs"
designer: "Ross Wollman <ross.wollman@pomona.edu>"
zones:
  center_stage: channel(1)
  upstage:
    left: channel(12) channel(81) channel(89)
    center: channel(18) channel(2) channel(90)
    right: channel(32) channel(52) channel(18)
  downstage:
    left: channel(127)
    center: channel(123) channel(19)
    right: channel(34)
groups:
  all: zone(upstage) + zone(downstage)

cues:
  1.0.0: in 1::second downstage::zone goto 100%::intensity
    to: light the entir stage
  2.0.0: then goto blackout::intensity
    to: allow actors to leave
  3.0.0: after in 2::second downstage:left::goto 20%::intensity
    to: illuminate the two new actors
```

The above pseudo code is one way this langugae might look&mdash;the exact
organization will need to be considered futher, but the overall idea is one
can create groups and zones (perhaps even paths of lights) that are then
meaningfully refered to in the `cues` section.

I think this is expressive in that it reads somewhat naturally (although going
along Fowler's principles, it won't be a natural langugae) and is farily easy
to communicate. Lighting designers and programmers would likely feel comfortable
learning this limited langugae.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When the program runs, the groups and zones are determined and then the cues
are composed sequentially which will eventually get turned into code that
can communicate with a dimmer rack (which itself physically controls the flow
electricity to lights).

As designers write, they may make syntactic errors or try to refer to a zone
that has not been defined. In these cases it would be ideal to have simple
and clear error messages helping to debug the code. I could imagine a process
that requires a program to compile after each new cue to make
sure things are all working before it gets to be too late.

Another error could be that a designer simply types the wrong channel that is
still a valid reference but is physically in the wrong place. For this
reason, when declaring a light cue that uses a specific channel the designer
must use the `special` keyword which is used colloquially to denote a light for a
unique intentional purpose. This way, users could be warned if there seems to be
an errant light included in their cue.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to create a fully lit, cued show with all the basic commands
provided by modern day lighting consoles. This system should not be able to
provide cues for sound or other technical elements&mdash;but should be allowed
in the future.

It should be easy to individually control lights and manipulate groups.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

From my research and experience in theaters, the only DSL is the channel intensity
level method of cueing lights. Theater, although pushing the technical limits
at times, also likes tradition&mdash;if it's not broken don't fix it is the moto
in many venues.

The current "langugae" is easy to learn and very fast to type&mdash;something
that is important since other people are waiting on the programmer to code up
the cue live, but it lacks semantic and physical meaning.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

For CS111, I think this project would require the most time spent on creating
an expressive syntax that is liked by lighting designers. The actual translation
to a protocol that could interact with a dimmer rack is outside the scope of the
project at this time. However, a "transpiler" that converts the DSL to the
traditional cue programming langugae is certainly feasible and would be a good
excersize.

### Scope
_How big an idea is this? How ambitious is this project?_

As mentioned above, this project could have a huge scope if it involved compiling
to a protocol that is processable by a dimmer rack. In the ultimate project it
would also involve creating a new lighting console that had a keyboard similar
to modern day keyboards with shortcuts for common keywords.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea
project?_

Getting professional lighting designers and programmers to use it would be
very difficult since they rely on expensive lighting consoles with custom
buttons that they are extrmeley familiar with. However, I do think it has
potential if proven through practice to be easier, more efficient, and descriptive.

Because the potential scope is so large, there will likely only be part of the
project done by the end of the semester; in an ideal world I would contruct
the langugae and all the architecture needed to communicate with digital
dimmer rack, but I do not think this is a realistic goal for the semester.
