# Free project 3

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.

I'd like to see if it is possible to extend the work of Milo Han from last semester. He (or she?) wrote a program for sight reading. The language would serve music teachers and their students in improving their sight reading. A language might be good as it would be able to specify what kind of music one wants to sight read in order to sharpen one's weaknesses.

### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Sight reading is the process of reading music without having seen the music before. Once someone reads through the music once, the music cannot be reused for sight reading. As a result, the need for a constant source of new music would be satisfied with a DSL for sight reading. We are helping music students and teachers. The current experience is to find music from the books and play through them. However, the books may contain music that is too easy or too hard. Therefore, music teachers and students tend to filter through resources to get good sight-reading material. By then, there might be little to none to help them. With our DSL, it would solve this problem and let students quickly gain skill in sight reading.


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL is appropriate because we want the users to give input on what kind of sheet music is generated for sight reading. A language can express a lot, and this kind of detail can create sheet music tailored to individual students and their needs. It addresses the problem of finding the right kind of music to sight read.

### Why you?
_What excites you about this idea? How did you come up with it?_

From my first project description, I explained how I am involved in music. However, I cannot sight read as well as some others. In the world of classical music, many professionals are able to sight read fairly difficult material, whereas I take time in reading the music. I sometimes blame my poor eyesight and lack of new glasses, but the main cause of my relatively poor sight reading skills comes from the lack of practice and material.

I really hope people can get good sight reading material easily that is tailored to them and free. I don't want others following my footsteps in not practicing sight reading because they didn't have enough accessible material.


### Domain
_Describe the project's domain in five words._
Sight Reading Music Generation

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

A user would probably write some form of code, specifying the constraints of the music generation. Programming would probably look like code in Python. I believe this is a good way to interact with the problem domain because the only thing we need to do is specify constraints in the music generation. Writing statements is perhaps the easiest.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

Some random sheet music should be formed based on the constraints given. The program interacts with the user by giving the sheet music back. I think errors should occur if the constraints/specifications given to the program contradict each other. This should be resolved as a message or perhaps as a blank sheet of music.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to specify what kind of music you want. This includes the meter, time, rhythms, and possible harmonies. It could be possible for someone to write specific notes into the music, but I would limit the number of notes someone can write in. If someone wants to write all the notes, they could simply use some existing software. 

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There are several other DSLs in the domain. Milo Han has a small set of links
[http://www.randomsheetmusic.com/][Random Sheet Music] Randomly generates music for single clef instruments.

[http://www.link.cs.cmu.edu/melody-generator/][Melisma Stochastic Melody Generator ] Generates midi files based on constraints given by the users.

[https://www.cs.hmc.edu/~keller/jazz/improvisor/][Impro-visor] Generates single line jazz improvisations over lead sheets. It can be used to practice jazz improvisation.

[https://www.sightreadingfactory.com/][Sight Reading Factory] Commerical software that generates surprisingly good sheet music. Users pay to use it.

## The Project
This section examines whether the idea makes for a good CS 111 project.

There has been previous work as a CS 111 project. In addition, I believe this is still a problem worth tackling. There are a lot of intricacies and things I want out of an open-source DSL for generating sight reading music. With the combination of previous work and current work still to be done, it sounds like a potential project for this semester.

### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I would believe it is 40/60 in terms of design choices and implementation. I am particularly sensitive as to what I want out of good sight reading music, and I also believe others can benefit from well-made design choices. Of course, I shouldn't just use my judgement to make the design choices. I believe there is a bit more implementation that needs to be done to give it the functionality and ease of making music.

### Scope
_How big an idea is this? How ambitious is this project?_

It is fairly big because generating music randomly that is fairly coherent, interesting, and the right level of difficulty is hard. So I would like to say it is an ambitious project with a potentially high pay off.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This is a good idea for the design choices as well as the impact we can make. Music is widely practiced, so many would benefit sight reading. However, the difficulty and scope of the project might make it hard to realize the potential within a half semester.
