# Free project 1

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.

A language for describing bridge hands in a manner that is easy to process by a
machine and by humans.  This would help people right down and save hands for
future study.  They could perform various operatinons on the hands, such as
searching for particular contracts, results, and other such metrics.

### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

I'm helping bridge players.  This would help bridge players who want to study
hands, share hands with other players, and just keep a database of hands.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL would be nice especially for making it easy to perform operations on the
hands.  For example if you just write a hand down on pen and paper it requires
work to search through the papers and find the hands.  Also you can't analyze
what the best result would've been if you played it optimally (not that there
are a few ways to define optimally here...).

### Why you?
_What excites you about this idea? How did you come up with it?_

I love to play bridge and often come across interesting hands that I play very
well and very poorly.  It would be nice to have an easy way to share these hands
with my friends.

### Domain
_Describe the project's domain in five words._

Bridge Players, Authors, and Enthusiasts

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

I think it should look like an easy to read text file with some particular
format.  Perhaps put the hand first, then the auction, then the order of the
cards played, then the result.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

I think the user would run the program by specifying what type of operation they
want to perform.  These options could include an analysis of the hand, a search
of all the hands in a folder, an exportation of the hand into a pretty format,
or other such useful operations.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to write down hands that way it is easily usable and would see
a good amount of use.  It should be easy to analyze and search for hands. It
should be difficult to play bridge using this DSL as this is a DSL for archiving
hand records not playing the game.  It should be difficult or impossible to
archive things not related to bridge hands.


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

[BridgeBase](http://www.bridgebase.com) offers the ability to export hands in a
.lin format, however this is hard to read.  Here is an example of a hand I
played: 
> pn|guplex,~~M12054,~
> ~M12052,~~M12053|st||md|1S58KAH269KDTKC34Q,S26JQH4D246JAC267,S349H37QAD3789C5A
> ,|rh||ah|Board 11|sv|o|mb|1N|an|notrump opener. Could have 5M. -- 2-5
> !C|mb|p|mb|2C|an|Stayman --   |mb|p|mb|2H|an|2-5 !C; 2-5 !D; 4-5 !H; 2-4 !S;
> 15-17 HC|mb|p|mb|4H|an|4+ !H; 10-13 total points |mb|p|mb|p|mb|p|pg||pc|C2|pc|
> C5|pc|CK|pc|C3|pg||pc|S7|pc|SA|pc|S6|pc|S3|pg||pc|C4|pc|C6|pc|CA|pc|CJ|pg||pc|
> D3|pc|DQ|pc|DK|pc|DA|pg||pc|SQ|pc|S4|pc|ST|pc|SK|pg||pc|H2|pc|H4|pc|HA|pc|H5|p
> g||pc|H3|pc|HT|pc|HK|pc|D4|pg||pc|CQ|pc|C7|pc|S9|pc|C8|pg||pc|DT|pc|DJ|pc|D7|p
> c|D5|pg||pc|S2|pc|HQ|pc|C9|pc|S5|pg||pc|D8|pc|H8|pc|H9|pc|D6|pg||pc|S8|pc|SJ|p
> c|H7|pc|CT|pg||pc|D9|pc|HJ|pc|H6|pc|D2|pg||

I think this could be more readable to humans.  Also I have difficulty finding
a way to process this data without writing something myself. It is nice that it
writes down pretty much all the information available at the table.

## The Project
This section examines whether the idea makes for a good CS 111 project.

I believe this would make a good CS 111 project since it is not overly difficult
and there is a large design element.

### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I think this is very much a problem about langauge design and not so implementation
heavy, especially for just describing and searching up hands.  If we wanted to
add features for analyzing hands I think that would increase the "system" aspects
of the project by a large amount, so perhaps that would be better to not implement
for a CS 111 project and just design how that part would work if we were to
implement it.  I think it would still be very useful without analysis features.


### Scope
_How big an idea is this? How ambitious is this project?_

I think this is not super amibitious.  Some of the analysis features could be
harder, but searching for things and designing an easy to read format should not
be too difficult I don't think.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

I think this is a very achievable project in a relatively short time frame, which
I think makes it a good candidate for a CS111 project.  On the other hand I'm not
sure if other people like bridge as much as I do, so it might be harder to find
classmates who want to work with me on it and are passionate about it.