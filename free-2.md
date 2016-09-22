# Free project 2


## The user and a language
This section describes who the project would serve and why a language might be a good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

This DSL will allow the users to create coloring pages with any pictures
they have or a picture found on Google randomly from the keywords the users input using this DSL.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

Its domain is very specific in a way that it edits pictures to create coloring pages. Recently there has been an increase in the number of adults who do coloring in their leisure time and they sometimes find themselves having to buy a whole coloring book, even if they are not found of every single page in it, because it contains a few pages they really like. So this DSL would allow the user to create a coloring page with a picture they live, without having to purchase it. 

### Why you?
_What excites you about this idea? How did you come up with it?_

I've recently got into coloring and I've found it very frustrating looking for coloring books, because a lot of them have a few pages that I like but not enough for me to buy the entire book. Also, when I came across great photos or pictures, I wished that I had them in coloring pages version.

### Domain
_Describe the project's domain in five words._

Simple production of coloring pages.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

I imagine the program can be run on the terminal. At first, the user will be able to import a picture they already own, or input keywords to get a picture randomly from Google.
The user might find it inconvenient that they can't see the final product of their coloring page on the terminal since this program is not interactive that way.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy for the user to generate coloring pages with pictures they already own or pictures found on Google based on their input keywords. They will also be able to specify their own arbitrary settings such as removing all colors from the original pictures except purple.
However, it would be impossible or very difficult for the user to take a peak on the final product before the program ends. In other words, they wouldn't be able to interact with the final product in real-time.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I had no idea this existed before I just did some research, there's a website that allows users to convert photos into coloring pages, https://www.reallycolor.com/. I want my DSL to essentially do the same thing, but also provide users with different settings such as removing all colorings except a certain color.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Developing language aspects of the project would be time-consuming since manipulating colors and other things of photos can be hard. But I don't imagine this project needing to integrate with any APIs. 
And the system part would be less time-consuming, since most of it would be converting the picture into a sketched veresion of it, possibly in a pdf.

### Scope
_How big an idea is this? How ambitious is this project?_

I think this project is ambitious for me in a way that it's going to require a lot of image manipulation, which I've always found hard. 

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea project?_

This project is suitable as a DSL class project, since it has a very narrow and specific domain. However, the scope of the project might be a barrier because it will be very time-consuming and require me to do a lot of self-learning beforehand about image manipulation.

