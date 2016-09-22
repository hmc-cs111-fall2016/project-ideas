# Free project 2


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea?_

Many people who love music and want to play the piano accompaniment for a song cannot read guitar chord tabs, but can read piano sheet music. 

My project would meet the need of those who want simple accompaniment written out on a musical staff, instead of having to read and play piano accompaniment from the letters and numbers that make up a guitar chord lead sheet.

Right now, to play the accompaniment of a song, a user has to:
* Look up the chords on a site like https://tabs.ultimate-guitar.com
* Read the letters and numbers that make up the name of a chord
* Understand what notes are in a chord, given its name 
* FIgure out how those chords can be played on the piano

It’s a very slow process! 

If I could help them, they would be able to save guitar tabs from a website into some kind of file, and my language would parse the different chords and translate a guitar chord such as “GDom7” into its notation on a musical staff (on sheet music). On the sheet music, the user would see 4 notes representing “G B D F”, which are the notes that make up the “GDom7” chord. 

 
### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL would be appropriate for my users because what they lack is the translation from the name of a chord to visualizing 1) the notes that comprise the chord and 2) the intervals between the different notes. The domain specificity of this language is important; this language does not have to perform the function of a general programming language, but what it should do is provide just enough functionality for users to input the name of a chord and as output, see the chord dictated on a musical staff. If the language was not domain specific, the learning curve might be unnecessarily steep for the function/goal of the language, and might involve a lot of unnecessary elements that are unrelated to the user’s goals. 

### Why you?

_What excites you about this idea? How did you come up with it?_

I am fortunate to have perfect pitch, so it’s always been very easy for me to hear music and know how to play the melody and accompaniment on the piano. I also compose / arrange music using MuseScore, which is a free and relatively-intuitive software. However, I’m always thinking of composing tools for people who can read simple sheet music but do not have the musical theory background that I’ve been fortunate to develop. I think about people like my mom, who can read basic piano sheet music, but cannot read guitar tabs, because reading guitar tabs requires a much greater understanding of key signatures and intervals (the user is given the name of the chord and must infer the notes in a chord), whereas reading basic piano sheet music just requires pressing all the keys that the sheet music indicates.
However, guitar tabs are much more pervasive than basic piano sheet music, because guitar tabs provide a flexible chordal framework for a piece, a chordal framework that can be improvised upon and adapted to any instrument and genre.  

I came up with my idea for this project while looking at the DSL that played the Batman theme song from an Excel spreadsheet! 


### Domain
“Guitar chord”-based piano accompaniment generator.


### Interface (syntax)
_How might the user interact with the language?_

I’m envisioning for the user to look up chord tabs such as the one below:

http://www.heartwoodguitar.com/chords/swift-taylor-you-belong-with-me/

Given that the duration of each chord changes (for example, the D Major chord is played during the lyrics “You’re on the phone with your girlfriend, she’s upset” and then transitions to the A Major chord), I want the user to use an excel spreadsheet, write down the time signature and tempo of the song, and treat each excel cell as one beat. Then the user would input the name of the chord, each time it changes, onto the excel spreadsheet, taking into account the fact that each excel spreadsheet represents one beat. The user will then save the excel file as in some format that my language will be able to parse, and my language will communicate with a software such as MuseScore to produce the sheet music dictation of the chords and their respective lengths. I also want to be able to somehow incorporate lyrics so that onto the sheet music so that the user can sing along with the chords that are now dictated on a musical staff. I think this is the right way to interact with the problem domain, because I want to make sure that using this program requires as little musical theory knowledge as possible.

_What does programming look like? Why is this the right way to interact with the problem domain?_ 

Programming involves inputting chord names into an excel spreadsheet, where each cell represents one beat of the song. This is the right way to interact with the problem domain because people can visually represent the duration of the chords and people can simply copy and paste the chord names they want, either from existing guitar chords sheets or chords that they themselves want to incorporate into the song. Using this program won't require much music theory knowledge!


### Operation (semantics)
_What might happen when a program runs?_

The program will ask the user to upload a xsl file, and then the program will parse the file, create the sheet music score in a program like MuseScore, inform the user that it is loading, and then allow the user to download the MuseScore file when the program is done.

_How does a program interact with the user?_



_What kinds of errors might occur, and how might they be communicated to the user?_

One error I anticipate is if the uploaded file is the wrong file, and the program would show the error message “please make sure that you are uploading a xsl file”.

### Expressiveness
_What should be easy to do in this language?_

_What should be possible but difficult?_ 

_What should be impossible or very difficult?_


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I got the idea for this project from one of the first DSLs we looked at during class, the one that played the batman theme song. I’m utilizing the idea of representing one beat of a song in each excel cell, but other than that, this particular DSL doesn’t achieve the primary purpose I hope to achieve, which is to generate “guitar chord”-based accompaniment in sheet music.

I searched google with the following key words “guitar chord sheet music converter”, “sheet music generator”, “guitar tabs sheet music”, and didn’t find any existing DSL that is similar to my idea.
My goal is to represent simple chord names with a visual representation, on sheet music, of what musical notes those chords involve.

Guitar lead sheets are a tools that help people visualize chords (instead of just knowing the chord name) are fingering for playing chords on the guitar (for example, this: https://www.pinterest.com/pin/104427285083096774). As of now, guitar lead sheets, and not sheet music, are the standard “language” for communicating the chordal accompaniment of a song. I conjecture that this is because guitars are more accessible (to purchase, to learn how to play, and to transport) and are thus a more popular instrument for playing music.

Two other interesting DSLs include these two programs: 
* http://www.scales-chords.com/chordid.php
* http://www.chorderator.com/designer/
* 
But there exists neither a tool that 1) translates the name of a chord (G Dominant 7th, 1st inversion) to a chord sheet, nor a tool that 2) translates the name of a chord into sheet music, much less piano sheet music that takes into account the duration of the chord and the song lyrics that are sung whenever each chord is played. 
It’s exciting to realize that I don’t think my proposal exists yet! 


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I think that if someone were to work on this project, perhaps only 20% of the work is spent directly engaging in the language aspects of this project (e.g., making language design decisions). This DSL is very abstracted, and demands very little of the user’s ability to code in traditional programming languages. The user is only interacting with an excel spreadsheet. 
The bulk of the work would be spent on the "systems" aspects of the project (e.g., implementing a complicated semantics that doesn't require a lot of language design), because of the need for ----  


### Scope
_How big an idea is this? How ambitious is this project?_

I think the greatest challenge is to communicate information to an existing musical notation software. It’s very easy for me to see the excel spreadsheet and write sheet music, but I have NO IDEA how to automate that process. 
However, I know this process would involve teaching the computer about different types of chords, the structure of different intervals that compose a chord, so that I don’t have to explicitly teach the program every possible chord. 
Example: I teach my program about the structure of major chords, minor chords, diminished chords, major 7th chords, and dominant 7th chords. Each chord is comprised of and defined by a particular set of intervals between various notes. I would also teach the program about the different inversions that a chord can be presented in. The most challenging part of the project is, the program will need to learn what it means for a certain chord to have a given root or key signature, so that it would be able to generate all the possible chords given a basic set of rules. 


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

I think this could be an interesting project because it is truly a very domain-specific language and would be a useful programming language for those who can read sheet music.
One reason this might not be a good idea is that it requires a programming language to communicate with a music composition and notation software like MuseScore. Instead of asking the program to produce sheet music with the correct durations of each chord, and for the chord to match up with lryics, perhaps a better idea would be for the user to not be concerned about the duration of the chords and their relationship to the lyrics of the song, but to just produce a set of guitar tabs with different chords, a set of chords on the same sheet?


