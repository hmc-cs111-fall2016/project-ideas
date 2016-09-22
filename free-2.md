# Free project 2: Automated Excel spreadsheet population


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.

This project would serve people working in consulting, finance or accounting who want to automate or speed up the process of data retrieval and population of Excel spreadsheets. 

### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

People working in these fields often have to parse large amount of information, often in enormous PDF files. These documents like the 10-K contain data in tables that have to be manually copied and pasted into Excel spreadsheets with relationships and equations between cells systematically entered. This is often quite tedious and repetitive work - suggesting an opportunity for a DSL. With this DSL, certain simple equations could be simplified to commands, and strung together with the fluency of a programming language. Ideally, the use of this DSL would free up time and resources for people to devote on less mind-numbing activities. 


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

It would be able to automate some of this tedious work and improve productivity. 

### Why you?
_What excites you about this idea? How did you come up with it?_

It could potentially be a very useful DSL. I came across this idea after conversations with peers working in economic consulting and my personal experience in Econ classes like Intro to Accounting. 

### Domain
_Describe the project's domain in five words._

Automated Excel spreadsheet population

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

At the most basic level, a user could interact with the language on command-line. Although this is not very ideal as it may not be very user-friendly for non-programmers, but would suffice as a minimum-viable product. This would be the right way to interact with the problem domain because creating a web GUI would take away time from development of the MVP. 

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

An initial call to the program could isolate all the tables in the PDF and paragraphs containing keywords entered by the user. Certain frequently used equations can be functions in our language. Further terminal commands could recreate each table in Excel and replicate some of the relationships between the cells that are laborious to enter on Excel. As the behavior in each table usually varies, we would probably want to allow for each table to be analyzed and populated individually onto Excel. 

Certain errors might occur such as the user referencing a table outside of the array of stored tables, mistyping the names of functions, or providing an insufficient number or type of argument to these functions. We can communicate these errors to the user through terminal messages. 


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to transfer data from PDF'S into Excel spreadsheets, anything else should be impossible. 

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

No. Python has a library for extracting data from an Excel spreadsheet but not vice versa. There are online PDF to Excel converters but these simply hard-code the data and don't offer enough control over the formatting.


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

A significant amount of time would have to be spent researching people's needs and figuring out how to turn those into coherent, fluent commands. Inspiration could be taken from python's existing library to see what sort of data manipulation is possible and how they are carried out. 

### Scope
_How big an idea is this? How ambitious is this project?_
The idea involves several distinct steps, all of which can be very challenging. I have no idea how to parse through a PDF, let alone isolate the tables, although I know it is possible because it's been done already - though quite sub-optimally. The hardest part in my opinion would be recreating those equations and dependencies between cells, and doing it in a way that makes it easier than the way it's currently done in Excel. 


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

If I do choose to pursue this option, I have a great group of people with industry experience (CMC alumni, among others) to interview and get to the root of their needs. It would be a very real solution to a commonly experienced problem. This may not be a good idea because I am unsure of how well one could even simplify writing Excel macros and whether this idea is truly feasible. The people I have spoken with are not programmers so it is difficult for them to imagine what is and isn't feasible with a DSL. 
