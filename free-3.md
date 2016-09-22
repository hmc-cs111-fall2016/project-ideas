# Free project 3


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.

### What's the need?
_What need is met by your idea?_

I want to meet the need of having more convenient keyboard shortcuts for arranging music in MuseScore.

_Who are you helping? What is that person's experience like now?_

Many people who love music and want to compose music use a software like MuseScore, which can notate, on a musical staff, the notes that someone plays on the piano keyboard. However, not everyone owns a piano keyboard! 

_What would their experience be like if you could help them?_

Right now, users have to either purchase a special keyboard, or suffer through inputting very few notes at a time onto MuseScore. My DSL could greatly improve the efficiency of writing music.
 
### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL would be appropriate for my users because what they lack is the translation from more convenient laptop keyboard inputs into MuseScore. The domain specificity of this language is important; this language does not have to perform the function of a general programming language, but what it should do is provide just enough functionality for users to translate their computer keyboard strokes into MuseScore dication. If the language was not domain specific, the learning curve might be unnecessarily steep for the function/goal of the language, and might involve a lot of unnecessary elements that are unrelated to the user’s goals. 

### Why you?

_What excites you about this idea?_

I really enjoy arranging music, and would really enjoy a tool that makes the process more efficient! 

_How did you come up with it?_

I came up with it one day when I was really frustrated with the painstaking process of translating musical thoughts into sheet music via MuseScore, and I did an angry keyboard smash. Then, I realized how cool it would be if I could tell Musecore the tempo of my song, and then press the computer keyboard keys that correspond to the notes I wanted to dictate. Ideally, the composition software would also compare how long I hold the key down (lets say 700 milliseconds) to the BPM (tempo) of the tempo I determined, to notate not only the notes themselves but the duration of the notes.

### Domain
Music Composition 


### Interface (syntax)
_How might the user interact with the language?_

The language will provide a text input box that allows someone to type in the tempo in BPM, time signature, key, and clef. For example, the user could say that the song was in 96BPM per quarter note, in 4/4 time, in G Major, and in treble clef. Then, a new MuseScore file would be created, and prompt the user to decide how many voices/instruments were going to be involved in the piece. The user chooses one of the instruments, starts the metronome, and presses the keyboard keys representing the names of the notes he wants to notate, holding down the key presses for a long amount of time if the note was longer, and a short amount of time if the note was shorter. 

_What does programming look like? Why is this the right way to interact with the problem domain?_ 

I described a bit above about how programming would look like. I think this is the right way to interact with the problem domain, because I want the music composition process to be as fast and efficient as possible, even without a piano keyboard.


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the user?_

The program prommpts the user for details regarding certain features of the music, including the clefs, key signature, time signature, tempo, etc. Then, as the user is pressing down the keys, the sheet music shows a faint image of the notes in the score. If the note was a half note (2 quarter notes) and the time signature was 4/4, the user would see the note appear as a quarter note at first, and then after he/she held it down too long to be considered a quarter note, it turns into a half note on the score, contuining to update the value of the note according to the pre-set time signature and BPM until the user releases that particular key.

_What kinds of errors might occur, and how might they be communicated to the user?_

The user might press the key of a note that doesn't exist in a music context, for example. The program should not dictate any note, but show an error message that describes the mistake "Illegal input: keystroke not the letter name of a note" and provide suggestions for what the program thinks the user meant to press. 

### Expressiveness
_What should be easy to do in this language?_

It should be easy to notate notes, in any clef, in any key, of any duration. 

_What should be possible but difficult?_ 

It would be hard to do more difficult rhythms using computer keyboard keystrokes, since the user would have to be very rhythmically precise. However, the user can always make adjustments using the Musescore software, if his/her keyboard keystrokes could not best capture what he/she intended to compose.

_What should be impossible or very difficult?_

Honestly, this language seems very limited, and can only convey the name of the note and the duration of the note. It cannot express, for example, the dynamics of the note. However, this DSL is only meant to be an addition to what existing composition software can accomplish, so a user can very easily make adjustments after using my DSL.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. 

Melodica is somewhat a similar DSL! It can be found here: https://www.youtube.com/watch?v=JYRQPlm4WZo


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I don't think there will be a lot of language decisions -- the input I need only requires 4 basic pieces of information from the user (key signature, clef, tempo in BPM, and time signature). None of the semantics of the language will look very code-y at all! 

### Scope
_How big an idea is this? How ambitious is this project?_

I don't think this idea is too ambitious -- it's very easy to determine what keys are pressed and for how long they are pressed, and the time that the key is pressed can be compared to the designated BPM and key signature to determine the duration of the note relative to the BPM (tempo). The tricky part would be to translate that into a visual representation of the notes.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

I think this project really fits the bill of being a domain specific language, and will hopefully provide a helpful abstraction for the process of actually writing out each of the notes and their durations on a musical staff.

This might not be a good idea because it involves writing notes on a staff, which may require my language to communicate with an existing composition software. I can understand how to generate all the notes of a chord (given a root and key signature of a chord, I have a good idea about how to generate the names of the chords because the relationship between the notes in the chord is just dictated by their interval). I think a challenge would be to find a way to visually display the chord on the staff instead of just naming the notes in the chord.


