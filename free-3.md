# Free project 3

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

This idea would fill the need for actors that want to practice their lines. The
main audience would be actors, but anyone who wants to speak publicly without
relying on a prompter or reading off a paper could use this. Currently, if
people want to memorize lines for a play or a speech for some event, they need
to drill themselves. Actors and public speakers who do this often will create
tricks to do this themselves and/or have other people help them memorize lines.
However, a lot of people can use help in this department. For example, I am in
many plays, and memorizing lines is my least favorite part of acting. I often
just stare at the words over and over again, and maybe say them aloud. However,
especially if there are many rapid fire dialogues among two or more characters,
the memorizing lines becomes harder. It is no longer about just the words, but
where you come in. You start off the first sentence, but then another character
says somethings, and its back to you again. Maybe your character has to cut that
person off, or maybe your character is just responding to the other character,
or maybe your character says something totally out of the blue and changes the
entire trajectory of the scene (very important if so). Or maybe you have a
half page worth of a monologue or soliloque, which are in themselves very hard
to memorize.

The idea for this DSL is to be able to prompt you for your next line, either by
giving the next line or phrase your character is saying, or by giving you
prompts from other characters. Basically, this DSL would act as your
memorization buddy, helping you memorize quicker and faster! If this comes to
fruition, then people can practice their lines by themselves, and can improve
their memorization game easily. A computer program will never complain about
practicing too much or practicing at 4am.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL is appropriate because it will be more intuitive to use than, for example,
just using the "say" command on your terminal. Ideally, it will take in the
script and be able to listen along as you talk, giving the next word or other
characters' lines when it determines it is appropriate or if the user presses
some kind of input. For acting scripts, it would be able to identify which
characters are saying what as usually lines are preceded by a character name and
colon, i.e. "James: What are you saying? Emma: You know what I mean!". The actor
would then be able to select which character they are practicing for, and the
DSL will automatically say the lines of other characters.

This is a pretty specific need, as most speech software are about ability
assistance rather than a specific memorization use. A DSL here also makes sense
because it is single purpose.

### Why you?
_What excites you about this idea? How did you come up with it?_

This excites me because I need it! I came up with it because I was practicing
lines and wish I had something like this to help me. I have no trouble
memorizing lines, but find that especially if my lines intersperse other
people's lines, then I have more trouble practicing. I want to remind myself of
the cues for me to speak with me looking at the script.

### Domain
_Describe the project's domain in five words._

Helps you memorize your lines

### Interface (syntax)
_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

The user would interact with this language by importing a document into it. This
document would be the script you want to memorize, or parts of a script. Then
the user will navigate to the lines where they want to start practicing. They
can select the line at which they want to start, and a line at which they want
to end. This allows the user to memorize specific parts or scenes. The DSL
will then let the user select the character the user wants to memorize, and
the DSL will scan and block out all those lines. The DSL will give the user the
option to block out the entire script on screen, so the user can only see greyed
out paper, or the DSL can grey out only the user's character's lines. Then, when
the user clicks "run", the program will either start off saying another
character's lines, or wait for the user to speak if the first line is the user's
character's line. Ideally, the DSL will listen to the user speak and
automatically figure out when to say the next line. However, that technology
seems hard to implement. The simpler version is to give the user two keys that
they can use. One to prompt the DSL to say the next character's line, and one
to start speaking the user's character's current lines. The second option can be
further broken down to either speak sentence by sentence if the user has
forgotten large swaths of information, or word by word. The word by word option
is because sometimes the user has actually memorized everything but just need a
tiny clue to get going on the next part of their dialogue.

This is the right way to interact with the problem domain because it simulates
memorizing off paper. At least personally, it helps a lot if I can visually
think about "where" my lines are (printed) in relation to other lines. My idea
is the script will initially appear like it's a Microsoft Word document, and the
greying will take effect and change what the user can see.


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

As discussed above, this DSL will probably be a program in and of itself. We can
consider each instance with a different script to be a different program. The
program will scan the imported script, display it, and allow the user to choose
which parts to practice and grey out those parts. The kinds of errors that might
occur are scanning errors, since this DSL will scan the script to differentiate
the lines of different characters, etc. There might be errors with setting up,
i.e. reads the start and end markers wrong, or greys out the wrong parts, etc.
Maybe it can say stuff about scanning if the DSL thinks it has parsed the script
wrong or does not know how to parse it (if it is not a script). The greying
could be manually modified by the user, as if the DSL knew the greying out was
wrong then it would not have greyed that part out in the first place.

Known errors (i.e. parsing errors) should be communicated via a text pop up or
red underlines (like in Microsoft Word) to indicate which parts are probably
wrong.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to read lines and skip lines that the user wants to practice
on. It should be possible but difficult to edit the script, or make the script
speak to you and convince people it is actually an AI. It should impossible to
do non-text related things like draw pictures.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

It would probably be a lot more "systems" work than "language" work. Most of the
language work would be centered around a good UI to present to the user to
maximize usability and intuitiveness. The bulk of a the work would be in the
"systems" work - implementing the scanning to determine which characters,
greying out some lines, etc.


### Scope
_How big an idea is this? How ambitious is this project?_
Moderate, a lot of places to do add-ons.


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea
project?_

It is useful and people would use it. It might not be a good idea as it does not
exercise the "language" work as much. It is debateable whether the UI is the
language part of the DSL. Even if it is, it is not immediately obvious that
there is a lot of work to be done there (though obvious I could be wrong and
there are probably many things to do with the space and how the DSL is presented
to the user).

