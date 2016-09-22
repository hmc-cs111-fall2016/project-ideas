# No computer project


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?

_What need is met by your idea?_ 
The need to understand information that is otherwise presented visually. 

_Who are you helping?_ 
Folks who are blind or visually impaired.

_What is that person's experience like now?_ 
The visually impaired are currently able to use Braille! 


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_
A DSL is appropriate because by nature, it is domain specific, given that it is only learned / used by those who are blind or visually impaired (or those who work closely with the blind and visually impaired).
It provides a language that is an abstraction of written human language and can be learned and used by the blind and visually impaired. It addresses the for users to understand human languages, and addresses the need by being a language that is primarily written with embossed paper that Braille readers can touch in order to receive a message. “Users can also write braille with the original slate and stylus or type it on a braille writer, such as a portable braille note-taker, or on a computer that prints with a braille embosser” [https://en.wikipedia.org/wiki/Braille].


### Why you?
_What excites you about this idea? How did you come up with it?_
Braille has already been developed and implemented in many languages and spheres beyond human language, such as art. 


### Domain
_Describe the project's domain in five words._
Communication needs of the visually impaired 


### Interface (syntax)
_How might the user interact with the language?_
According to Wikipedia, “Braille characters are small rectangular blocks called cells that contain tiny palpable bumps called raised dots. The number and arrangement of these dots distinguish one character from another. A full Braille cell includes six raised dots arranged in two lateral rows each having three dots. The dot positions are identified by numbers from one through six.[3] 64 solutions are possible from using one or more dots. A single cell can be used to represent an alphabet letter, number, punctuation mark, or even an entire word.[3]” [https://en.wikipedia.org/wiki/Braille]. The user can slide his or her fingers across a page with Braille dots to “read” what is communicated. 


_What does programming look like?_
According to Wikipedia, “Braille may be produced by hand using a slate and stylus in which each dot is created from the back of the page, writing in mirror image, or it may be produced on a braille typewriter or Perkins Brailler, or an electronic Brailler or eBrailler.” [https://en.wikipedia.org/wiki/Braille]

_Why is this the right way to interact with the problem domain?_ 
 This is the right way to interact with the domain because one sense that the visually impaired generally have is their sense of touch. It would be difficult to rely on senses other than one’s sense of touch as a standard form of communication, and of all the senses to be impaired (hearing, smelling), the sense of touch seems to be one that people generally have intact. 



### Operation (semantics)
_What might happen when a program runs?_
Braille isn’t a computer program that is run! :) 

_How does a program interact with the user?_
Braille traditionally interacts with the user by presenting raised dots on a sheet of paper, dots that the user brushes his fingers across to “read” the letters. 

_What kinds of errors might occur, and how might they be communicated to the user?_
1 possible error is that a braille sheet becomes worn down, making it difficult for the user to distinguish between different letters. The user would likely be aware of this upon touching the surface with the worn-down dots. 


### Expressiveness
_What should be easy to do in this language?_
Braille not only serves as a replacement for printed texts in many languages, but can also use the concept of raised dots to communicate an image. Given Braille’s origins as a language derived from the Latin alphabet, and given the fact that its letters were organized according to their position within the French alphabet, it should also be easy to represent other phonetic languages in Braille.

_What should be possible, but difficult?_
However, it might be difficult to represent non-phonetic languages in Braille (excluding non-phonetic languages that have romanized representations, such as Chinese), since many non-phonetic languages do not require the reader to read all the components of a word / character in succession from left to right or right to left. 

_What should be impossible or very difficult?_
Text can often be presented in different fonts, but a font would be difficult to capture in Braille. The challenge is that the variations between different fonts would still need to ensure that the letter is recognizable to the touch. 
Another challenge that Braille faces might be expanding the language. Even though English Braille alphabet is composed of all letters and symbols, what if there is a new symbol that needs to be represented, but the alphabet has already run out of possible combinations of 6 raised/non raised dots? What if Braille also wanted to represent symbols such as emojis? 


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links._
Another language that the blind/visually impaired could use to communicate and understand thought is through sign language that is spelled out into the hands of someone who is blind or visually impaired. 

http://www.lifeprint.com/ This website provides information and resources to help people learn ASL and improve their signing. 

_How well do they address the need?_
I think Braille is preferred to sign language because in order for a visually impaired person to receive and communicate information via sign language, he or she would need another person there to perform the sign language or speak it. It would be really interesting to hear of software that receives sign language footage as input and produces a sheet of paper with Braille.

_Are there any particularly admirable qualities of the language?_
I think it’s awesome that Braille can represent Western music as well! [https://en.wikipedia.org/wiki/Braille_music]

_Are there parts of the language you think could be improved?_
This isn’t inherent to the language itself, but the number of users of this language. There is generally a small market for Braille content, and very few people aside from the visually impaired (or those who work closely with the visually impaired) are motivated to learn Braille, so there is less information in Braille than ought to be. This impacts and is impacted by the fact that the production of Braille is more costly than regular ink-print production. 

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Braille that represents the English language has already been created!

### Scope
_How big an idea is this? How ambitious is this project?_
 I’m not sure what this question means, since Braille already exists. But if one were to represent another human language with Braille, that might be a challenging undertaking since it seems like many of the combinations of raised and lowered dots are used. It also wouldn’t be intuitive to design an entirely new system of Braille that doesn’t expand upon any of the symbols and patterns of existing Braille. It would be great if this new Braille sub-language would be syntactically similar enough to existing Braille sub-languages such that it would be intuitive for those who are learning the new sub-language, but the new sub-language must also be careful to not be too similar to existing sub-languages to the point where people could find the similarities indistinguishable and easy to mix up. 


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_
Given that Braille isn’t a computer programming language, I don’t think it would be a great project to work on! But it might be interesting create a computer DSL that helps people with creating Braille text -- maybe some language that converts spoken languages into the corresponding Braille text?

