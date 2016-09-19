# Free project 1

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

The language targets musicians interested in digital music synthesis.
Currently, there are two categories of tools which allow producers to generate
music using a computer.

The first is a type of software called a Digital Audio Workstation (DAW).
Popular DAWs like Pro Tools and FL Studio usually have built-in digital
"instruments" which user's can program by writing a MIDI score. These are
usually prefabricated instruments that can only be customized by changing
certain parameters. This makes it possible to get a range of sounds out of each
instrument, but it is hard or impossible to create completely new instruments.

Musicians interested in creating their own instruments can use a DSL called
CSound (which is taught at Mudd in MUS 80). CSound allows users to create
chains of oscillators -- primitive components used to generate a sine wave --
and effects like filters to literally build from scratch their own digital
instruments. This simulates the way the earliest synthesizers were used; the
musician would connect oscillators and other components using wires. CSound
takes this process and makes it digital.

But there's a problem with this current state of things: DAWs operate at a high
level, where the primitive unit is an instrument. CSound operates at a much
lower level, where the primitive unit is an oscillator (this fact and its
opcode-based syntax means it is used almost exclusively by academics). There is
a lack of tools in the middle. Musicians who want to create their own
instruments but don't want to deal with the low level of abstraction offered by
CSound have little recourse.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

The domain of instrument creation has very clearly defined primitives at the
level of abstraction I'm interested in. I will call these primitives sources
and effects.

A source is a sound generator, like a CSound oscillator. But a source generates
a more complex signal than an oscillator, and is in fact a particular
arrangement of many oscillators. A source is a pattern that can be described by
a few parameters, but that would have to be implemented over and over again
from the oscillator level in CSound. With only a few types of primitive sources
-- additive and subtractive synthesizers, frequency and amplitude modulation
synths, and physical models -- a wide variety of sounds can be created.

The second type of primitive is an effect. These do not produce sound, but
rather take a signal as input and output a different, transformed signal. In
CSound, effects must be implemented from filters and envelopes. At a more
intuitive (for musicians) level of abstraction, primitive effects would include
compressors and equalizers. These effects could be chained together with
sources to alter the sound produced by the sources.

A good tool for digital music synthesis should provide these primitives, and
should allow them to be composed by chaining in serial and in parallel. This
already sounds like a language -- we have vocabulary (sources and effects) and
fluency (the method for chaining).

### Why you?
_What excites you about this idea? How did you come up with it?_

I have been interested in making music of all kinds for years. I took Music 88 last year, and while I enjoyed learning CSound and using it to make music, I also felt frustrated that it is so difficult to use.

I was discussing potential project ideas with Daniel Zhang when the conversation turned to Melodica, and we both felt that it would be fun to make a music language like that. It seemed natural to me that there should be a language targeted at serious musicians which, provided the user is knowledgeable in the domain, is as easy to use as Melodica, but which provides more power and flexibility than a DAW. In short, I want to fill in the gap in this spectrum:

Simple ---------------> Powerful
Melodica -> DAWs -> ??? -> CSoud

### Domain
_Describe the project's domain in five words._

Instrument oriented digital music synthesis.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

There are two parts to programming. The first is defining instruments. This is
done by laying out a chain of sources and effects. These chains can be composed
by connecting the output of one chain to the input of another (the second chain
would have to start with an effect, which takes a signal as input). Chains can
also be connected in parallel using a component that takes multiple sounds as
input and produces a single sound as output.

The second part of programming is writing a score. A score uses various
instruments to produce a piece of music by playing a certain note on a certain
instrument at a certain time. Playing a note means giving the instrument any
inputs that it requires to start generating sound, such as pitch and amplitude.
There's some flexibility here: the score-creation process could be a textual
language that comes bundled with the instrument-creation language. This is what
CSound does. Or, the instrument language could be designed to interface with
existing methods for writing musical scores. For example, there could be a way
to assign each track in a MIDI file to a different instrument, and use the MIDI
messages like note-on, note-off, velocity and so on to pass parameters to the
instruments.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

The output of the program could be either a sound file or an actual sound.
Either way, the runtime looks the same; the only difference is whether samples
are written to a file or to the computers DAC. The basic runtime process
consists of reading "notes" from the score in chronological order, and calling
the correct instrument for each note. When the instrument is called, it starts
generating a signal from the first source in its chain. That signal is then
passed as the input to the next component of the chain, and so on until the end
of the chain. The resulting signal is written to the output.

There could be errors in the score, such as passing the wrong parameters to an
instrument trying to call an unknown instrument. A simple error message
describing where in the score the error occurred and what it was would probably
be enough to communicate to the user. In the instrument definitions, possible
errors include ill-typed connections. For example, trying to connect the output
of a source to another source, which does not use a signal as input, would be
an error. These could also be communicated as error messages.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to create instruments that are based on commonly-used patterns like frequency modulation or physical modeling. It should be harder, but possible, to create completely different kinds of instruments. This may mean exposing CSound-like primitives, but encouraging users to use the higher level constructs where possible.

It should be difficult or almost impossible to produce a complete song with this language. The language is not meant to be used for recording, mixing or mastering. More likely, the user would need to combine instruments written in this language with a fully-feature DAW to produce a complete song.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I have discussed [CSound](http://www.csounds.com/) fairly extensively. To
reiterate, it is not an adequate solution for most users because it requires
the programmer to think at a level of abstraction more suited to theorists than
to practical musicians.

I have also mentioned DAWs. There are many such programs, like [Pro Tools](http
://shop.avid.com/ccrz__Products?viewState=ListView&cartID=&categoryId=a3yi00000
000127AAA&&store=shop&gclid=CPai68yPlc8CFYRufgodL9MHgQ), [FL
Studio](https://www.image-line.com/flstudio/), and [Studio
One](http://www.presonus.com/products/Studio-One), to name a few. I'm not sure
if I would call these DSLs, although Prof. Ben might! In fact, these DAWs are
probably sufficient for the majority of digital music producers. But for those
who desire more flexibility than the prefabricated instruments allow, they are
not sufficient.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

The implementer would be able to leverage existing solutions for much of the
systems aspect. As an example, a prototype of this language could be a compiler
or transpiler that outputs CSound code, thereby using the existing CSound
infrastructure for actually generating audio. This leaves plenty of time for
language decisions to be made.

### Scope
_How big an idea is this? How ambitious is this project?_

I think this project is distinctly doable, given that most of the technical work could leverage existing solutions as described above. In fact, I believe it would be possible (though probably not recommended) to implement a prototype of this language using the CSound preprocessor.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

I think implementing this language would be a good exercise in designing a
small language that can grow, as described by Steele. The modular nature of the
chains of components which I have described seems perfect for building such a
language.

On the other hand, this may also be a drawback. It would be really easy to get
carried away with adding features, as I can already think of tons of built-ins
that would be cool to have. Avoiding feature creep will be a significant
challenge in building this language.

