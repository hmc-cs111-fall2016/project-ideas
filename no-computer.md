# Circle of Paranoia


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_
My non-computer DSL idea is actually an abstract game I am in the process of 
creating for my analog game design class. The game is called ["Circle of Paranoia"](https://docs.google.com/document/d/1WssK6n2gQf6TpReBtXNDcGkmX7z2NeDntuUo4jmU3aI/edit?usp=sharing), 
and the game meets the need of people who are bored and want to play an amusing 
game that requires some spatial thinking! It is a very accessible game that young
kids could play using luck, but for adults, it could be a very competitive strategy
game. Many abstract strategy games require a lot of time, but this game is pretty 
short and fun to play in your spare time. 


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_
In this game, I would consider the different colored pieces as the vocabulary
of the DSL, and the different positions on the board as the governing syntax. 
The DSL is necessary for the players to communicate their moves and to become
closer to reaching an end state of the game. They use the language by swapping 
one piece with a piece in a different position on the circle or in the center of
the circle. The "code" is modified during each player's turn when they must swap
a piece. 


### Why you?
_What excites you about this idea? How did you come up with it?_
This idea excites me because I'm looking forward to play testing it with others
and seeing their reactions. It's nice to make something that brings out a 
competitive spirit in people and allows them to have some fun. I came up with it
while brainstorming ideas with some of my peers in my game design class.


### Domain
_Describe the project's domain in five words._
Two-player, abstract strategy board games


### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 
The user interacts with the language by swapping their colored pieces with
other pieces on the board. They observe the entire board at each turn, and 
they try to pick the best move by reasoning through the outcomes of different
swaps. Involving the whole board throughout the entire game is an intentional
choice that forces the user to be thinking about many different moves each
turn. The language environment is complex, even though the vocabulary of the
language is quite simple.


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_
When the game is in play, the position of the colored pieces indicates the state
of the game to the user. The game state changes with each player's turn. When the 
user has many pieces lined up across from each other, it indicates to the them that 
they are close to winning. If a user makes an illegal move, it is up to their 
opponent to call them out! 


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_
It is easy to swap colored pieces in this language and easy to observe the entire
state of the game, or "program". It is difficult to make "sneaky" changes in this
language, since the user's opponent can always observe the moves they are making.
It is impossible to create a computer program with this language. :)


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_
There are many other abstract strategy games like [Chess](https://en.wikipedia.org/wiki/Chess), [Checkers](https://en.wikipedia.org/wiki/Draughts), [Connect Four](https://en.wikipedia.org/wiki/Connect_Four),
and more! They all involve two sets of distinguished pieces that are placed on different
positions on a playing board, and they all provide a fun activity that also 
requires people to utilize logic and strategy. However, chess and checkers especially
require a big investment in time, which might make them more undesireable to play
for a casual user.


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_
Language, which involves defining vocabulary and rules, takes 90 percent of the
time. Abstract games are all about language, and facilitating a way for players
to communicate to each other to come closer to a winning end state. Decisions 
involve things like how many colored pieces each player should get, how many 
positions should be on the board, and the different ways a player is allowed to
swap pieces. The rest of the time is spent basically designing the aesthetic of
the board and pieces.


### Scope
_How big an idea is this? How ambitious is this project?_
It's a relatively small idea that can be implemented with very few materials -
just some colored paper and pen. The project is ambitious in the sense that
it requires a lot of thinking to make a functional game that isn't impossible or
too easy to win, and it requires a lot of playtesting. But overall it's very fun
to implement and watch people play it.


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_
This is a good idea for a project in that it requires few outside skills to implement
and can be physically modified easily. It does require a lot of playtesting, which can 
be tedious, and requires the help of several other people.
