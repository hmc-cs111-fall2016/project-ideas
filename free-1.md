# Free project 1: Music and Visual Art generated from keystrokes or text

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.

This project could be used by anyone looking to create animations and musical notes from within their web browser. 

### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

There isn't a particular need that the project would fulfill. Perhaps an innate "need to create art in a spontaneous and fun way and be able to share it with others". While a program like ContextFree is very methodical and has quite a steep learning curve, this project would allow users to be creative in a much easier and more engaging way while retaining the element of randomness that makes ContextFree interesting. 

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

N/A

### Why you?
_What excites you about this idea? How did you come up with it?_

I've always been fascinated by music visualization. My project draws inspiration from this website I came across on my Facebook newsfeed sometime last year: http://patatap.com/. Ever since I've seen it, I've wanted to build something like it, adding my own twists of course. 

### Domain
_Describe the project's domain in five words._

User-generated music and animations 

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

If I were to make an app that plays music in real time, the user could "interact with the langauge" through keystrokes. An alternative on a website could be through point-and-click but this may stifle creativity as a keyboard offers so many different options and would generally be more fun to play with. If it were a mobile app, touch could also be an option.

Another option could be to have the music be generated from text. Users could type words, sentences or entire paragraphs which would be parsed, interpreted then played as notes (length of the word could relate to how long the note is, and the first letter of the word could relate to the pitch of the note).  

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

What happens when the program runs would differ depending on if I want the notes to be played in real-time or interpreted from a set of words. There would be no errors as all inputs from the keyboard would be fair game. 

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to make music and animations sequences in this language. But impossible to solve tasks beyond this such as those involving data structures, algorithms or writing proofs. 

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

My inspiration, http://patatap.com/, has done a very good job already but there are a number of things that I'd do differently if I were to choose to pursue this project. For one, it would be cool to have a way to record sound and animation sequences. Currently patatap just allows you to play a sound with an accompanying animation - a visual piano if you will. In my version, I could have a "playground" mode where users could experiment before playing with the "recording" mode. In the "recording" mode, I could record certain sequences which would repeat in a loop, then allow users to add "layers" of sound and animation sequences on top. These layers can be added and deleted. As a super-stretch goal, I could allow users to send save and send recordings they've made. 

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

The "words" of this language is simply every key on the keyboard, and since there are no limitations on which the sequences that these keys are used, there aren't any language design decisions in the traditional sense. 

If I were to choose the option of translating text into music and sound, it would be very easy for the sound to devolve into some hodgepodge of unappealing sounds. So there would be the interesting problem of how to structure it in a way that would avoid this. If I were to pursue the real-time option, then there would be design questions of which keys should produce which notes (the most accessible keys producing the most standard sounds?), and how to implement the saving and editing the layers of sound (using the arrow keys, perhaps). 

### Scope
_How big an idea is this? How ambitious is this project?_
How big the scope of this project is would depend on whether I fork Patatap and add the features I mentioned above, or to do it all from scratch. Programming JavaScript or CSS animations and choosing a sound for each of the keystrokes could take quite a lot of time and would most likely require the use of certain frameworks which I would have to learn. The additional features could also take significant time to develop, especially if I want data persistence and the ability to send sequences to other people. 

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

It would be a good idea for a project because I'm very passionate about it, and it would be an exciting thing to be able to show to others - the domain is applicable to everyone and not a subset of engineers or domain experts. It may not be the best idea for a DSL because it does not techincally solve or simplify a problem to improve productivity. Which isn't necesarily a bad thing, there's a place for pragmatism and creativity. 

