# Free project 1

## The user and a language
The first language I would like to consider is one for music composers. It would help them organize ideas about compositions into structures they create, simulating a top-down approach to composing music.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

My idea satisfies the need of organization when composing music. We will be helping composers of any skill level organize their compositions. The main reason why I'd like to build a language for organizing composition structures is because a current person's experiences in composing is done on paper or in a language not built for organizing composition structures. There are a lot (like, really, a lot) of langauges that focus on creating music and aiding musicians. But I haven't come across one solely dedicated to organization yet. I hope that the language I am thinking of helps people efficiently organize their thoughts in compositions and frees them to think of other aspects of composing music such as harmony, rhythm, and textures. From here, the hope is that the less time spent thinking about organization leads to more time/efficiency on the other aspects.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

One reason why I see a DSL as a potential solution is because current music software includes a lot of other things. Many programming languages, libraries, and APIs that implement ways to create music focus on making it possible to make cool sounds and patterns. But instead of having that affect one's compositions (following the Sapir-Whorf hypothesis), having a programming langauge specific to enhancing one's compositional creativity would decrease the impact of languages on musician's compositions. A DSL can be used as a preliminary tool or a tool in conjunction with other music software. As stated above, the end goal is to let users easily think of problems other than the structure of a composition that arise when composing.

### Why you?
_What excites you about this idea? How did you come up with it?_

I am interested in music in different ways. I take piano lessons, do chamber music, play gamelan, play jazz, and am a part of the Pomona College Orchestra. So music (at least classical and jazz) has been a large part of my life, starting when I was fairly young.

I took an independent study in composition with Prof. Alves two years ago, and I learned a couple of things. One is that all pieces, regardless of their genre, always had a plan behind them. Regardless of whether randomness is involved, I believe that almost all music depends on structure and organization. The structure doesn't have to be rigid. For example, a structure can be just 3 sections that have completely random notes, rhythms, and dynamics. However, humans tend to enjoy music they understand, and having structure helps them understand the music.

Overall, this idea is inspired by my struggles in composition, and my hope that composing can be easier for everyone.

### Domain
_Describe the project's domain in five words._

Music Composition Organization

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

I'm not sure how the user would interact with the language. It might be have a gui where people can edit a flow chart. It might also just be something like a regular language. However, I'd like to make sure that the user is able to clearly see the organization.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

The hope is to output some form of visualization of the structure of the composition. This may be an outline, a flow chart, or something that depends on the type of composition wanted.

Certain errors that might occur is if the structure does not have an end to it. There might be cycles in the structure created by the user, and unless the cycle doesn't last forever, it should be detected by the program. The error should be told to the user when the program is run. It might also warn the user as the music is being created.

As probablisitic decisions might be made in navigating the structures, the program might also want to warn the user if a structure is able to last really long. For example, if there were a 0.1% chance of getting through a structure because of several other probabilistic decisions made, it would be also good to notify the user.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to create blocks of sections that are part of the structure. It should also be fairly easy to relate the blocks to each other. One might point to the other, or there might be other stuff as well.

I am debating whether or not users should be able to input notes or audio into the structures. This kind of stuff may be possible or may be impossible.

I'd like to see people be able to create large structures if they want (after all, some people might be interested in really long music). These large structures might just be a composition of medium sized structures. I hope this kind of stuff is also just as easy.

It would be interesting to see if the user is able to import their work from other languages/software into the blocks and only at that level. This would let the user test out the music, but make it impossible for them to actually annotate the music. This is something I am still considering.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I do not think there are any DSLs like this. I think the main reason why is that programming languages that involve music often involve some form of audio input. This may be typing notes, playing on a midi keyboard, or singing through a mic. To be honest, having easy audio input is a great way to stimulate creativity. However, I don't believe programming languages for music has great support for showing easily organizing and showing the desired structure of a composition in progress. Of course, I could be wrong about all this, and there could be a PL like the one I described. However, nothing I've searched so far has really made me believe so.

## The Project
This section examines whether the idea makes for a good CS 111 project.

I think the project would be interesting as a project because it requires me to make many design decisions. In addition, it will probably require interaction with users in the domain. The project might not work out, but I think it's a different approach that might influence users in the domain into a different way of thinking about programming languages with music. This kind of uncertainty would certainly help exercise our training as DSL makers/designers.

### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_


### Scope
_How big an idea is this? How ambitious is this project?_

I think this project is on the medium side of ambitiousness. We don't have to get all the features I want to make it functioning. 

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

