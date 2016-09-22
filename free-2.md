# Free project 2


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea?_

Many people who love music and want to play the piano accompaniment for a song cannot read guitar chord tabs, but can read piano sheet music.

_Who are you helping? What is that person's experience like now?_

My project would meet the need of those who want chords to be presented in the form of notes on a musical staff, instead of in the form of a guitar tab sheet. 
Right now, to play the accompaniment of a song, a user has to:
Look up the chords on a site like https://tabs.ultimate-guitar.com
Read the letters and numbers that make up the name of a chord
Understand what notes are in a chord, given its name 
FIgure out how those chords can be played on the piano
If I could help them, they would be able to directly translate from the name of a chord to seeing a depiction of the chord, dictated on a musical staff. 
For example, my language would parse the name of the chord given by the user and translate the name of the chord (such as “GDom7”) into its notation on a musical staff (on sheet music). On the sheet music, the user would see 4 notes representing “G B D F”, which are the notes that make up the “GDom7” chord. 

_What would their experience be like if you could help them?_

The users would be able to more quickly play the accompaniment part of a song they like on the piano! Instead of having to search up the chords and try to decipher how to play each chord, my DSL will help them translate the name of the chord to an image of the musical staff with the chord notated on it.  

 
### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL would be appropriate for my users because what they lack is the translation from the name of a chord to visualizing 1) the notes that comprise the chord and 2) the intervals between the different notes. The domain specificity of this language is important; this language does not have to perform the function of a general programming language, but what it should do is provide just enough functionality for users to input the name of a chord and as output, see the chord dictated on a musical staff. If the language was not domain specific, the learning curve might be unnecessarily steep for the function/goal of the language, and might involve a lot of unnecessary elements that are unrelated to the user’s goals. 

Again, my users are people who can sight read sheet music but may not know much music theory. My DSL addresses the need because it puts a musical chord in the form of sheet music, which my users can read, instead of in the form of a guitar tab or simply the name of the chord, which would not be as easy to read and then quickly play.

### Why you?

_What excites you about this idea?_

I am fortunate to have perfect pitch, so it’s always been very easy for me to hear music and know how to play the melody and accompaniment on the piano. I also compose / arrange music using MuseScore, which is a free and relatively-intuitive software. However, I’m always thinking of composing tools for people who can read simple sheet music but do not have the musical theory background that I’ve been fortunate to develop. I think about people like my mom, who can read basic piano sheet music, but cannot read chord sheets (which only display the name and inversion of chords). This requires a much greater understanding of key signatures and intervals because the user is given the name of the chord and must infer the notes in a chord, whereas reading basic piano sheet music just requires pressing all the keys that the sheet music indicates.

_How did you come up with it?_

I came up with my idea for this project while looking at the DSL that played the Batman theme song from an Excel spreadsheet! 

### Domain
Translating chord names -> sheet music 


### Interface (syntax)
_How might the user interact with the language?_

The language will provide a text input box that allows someone to type in the name of a chord. The user will then select the clef that the chord is written in. The language will then display a generated image of the chord on a musical staff, and the user can save the chord and move onto translating another chord, most likely in the order the chords appear in a song. 

_What does programming look like? Why is this the right way to interact with the problem domain?_ 

The user simply has to type in the name of the chord, and then use checkboxes to decide what clef the chord is in (and other features I'm not thinking about now). This is the right way to interact with the problem domain because when pianists look up the chords for a song, they want to be able to play the music right away, and I want my program to be as hassle-free as possible. Also, typing in the name of the chord requires no understanding of music theory, which I do not expect for my users to have. 


### Operation (semantics)
_What might happen when a program runs?_

The program needs to break up the input into several features: the clef, the key signature or root of the chord, the type of chord it is (Major, minor, diminished  7th, etc.), and the inversion of the chord. After receiving the input, the program would then parse the three pieces of information, start with the clef and root of the chord, and build up interval by interval according to the type of chord it is. For example, the 2nd note in a major chord is a major 3rd interval above the root, whereas the 2nd note in a minor chord is a minor 3rd above the root. Then, the program would look at what inversion was specified (and if there was no inversion, assume a root position of the chord), and rearrange the order of the notes in the chord accordingly. 

_How does a program interact with the user?_

The program will prompt the user for the name of the chord that he/she wants to translate, offering 4 text boxes for the user to specify: the clef of the staff, the key signature or root of the chord, the type of chord it is (Major, minor, diminished  7th, etc.), and the inversion of the chord.


_What kinds of errors might occur, and how might they be communicated to the user?_

The user might type in the name of a chord that doesn't exist: for example, T Major with an inversion of 6/2. The program should display an error message and offer prompts for what the user might have intended to input. 


### Expressiveness
_What should be easy to do in this language?_

_What should be possible but difficult?_ 

_What should be impossible or very difficult?_


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


### Scope
_How big an idea is this? How ambitious is this project?_


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

