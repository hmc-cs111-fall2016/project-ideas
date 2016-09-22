# Free project 3

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

_Right now, without certain access and friends, it is difficult to play
different types of card games competitively (Magic, Pokemon, Netrunner,
etc.) because someone needs to buy the cards, which are not cheap, and
practice playing, which requires someone else. Currently, most people
choose not to play, for financial reasons or for lack of people to play
with. Hopefully, this DSL would get them excited enough that they could 
seek out people to play with because they would already know the game._

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

_These games have wide range of the types of cards that that can have. So,
having a DSL allows the user to have variable rules and variable cards. It
can do so by loading in the set of cards that the user will have, the set
of cards that the computer will have, and play the game from there._

### Why you?
_What excites you about this idea? How did you come up with it?_

_It excites me that more people could become involved in these card games,
so it can hopefully stop being only a nerdy elite who know how to play and
can teach others to play. Additionally, the number of elements involved
in creating this project would be interesting, from loading the different
rules in, to the different cards in, to actually having a computer play
with a person would be interesting. I came up with it by reading Prof Ben's
idea generation page. When he wrote down card games, I thought about my
experience trying to learn Magic. I was not interested in thinking about
the theory of the game because I was so new. However, it is such a 
strategy based game that without understanding the theory and strategy of
Magic, it's difficult to do well. I ended up playing with my brother,
who was happy destroying me without a question, but if I had tried to
play with a more experienced crowd I did not know, I would have felt like
an outsider because of my lack of experience._

### Domain
_Describe the project's domain in five words._

_Teaching card game novices basics_

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

_The user would have to load their cards into the program and tell the language
which version of the rules it ants to use. Programming looks like changing the
cards and rules to be able to play a game against the computer. This is the
right way to interact with the problem domain because there are so many cards
for any given game that it would be ridiculous to include all of them.
Additionally, card developers release new cards very often to continue to make
a profit, so a designer could not account for every single card. However, each
card has a certain template that it follows. So, once the language learns
that template, it will be able to understand any card that the user programs
into it._

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

_When a program runs, it will give the user a way to play the game with the
computer. The errors that might occur would be incorrect cards. For instance,
if a card did not have a certain field or the field was filled in with the
wrong type, the program should not accept it as a card. So, it would tell
the user which card was wrong and why and encourage the user to try the 
program again with a fix. Additionally, if a user tried to make a move that
was not allowed by the rules, the program should reset to the previous
position and tell the user that the previous move was not allowed._

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

_It should be easy to make new cards for a given game. It shoud be difficult,
but possible to make a completely new game because that would involve writing
all of the rules into place and describing how a card is set up. It should be
impossible to run a program in this language that just prints "Hello World."_

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

_There are currently programs that will let you play these games online with
other people (http://magic.wizards.com/en/content/magic-online-products-game-info
or http://www.pokemon.com/us/pokemon-tcg/play-online/). I admire that most of
them have info for new players and tutorials to help them get started. I wish
that there were more starter sets for players so that they would not have to
try to craft their own decks and ways for players to make their own cards, which
is not a part of these languages because they are owned by the company that
makes these games. I also wish that there were more variablity if people wanted
to try with a certain rule modified._

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

_Even discounting the UI interface of this project, ther would still be a large
amount of this project that would be semantics. The AI part of the language is
rather difficult because it has to follow the rules of the game and hopefully
be a competitive player to the point that it's moves are not self-destruction.
There would be a good amount of intereacting with the language design decisoins
by determining how the rules and cards would be given to the language, but it's
difficult for me to see this as the main part of the work._

### Scope
_How big an idea is this? How ambitious is this project?_

_This is rather ambitious. However, completing this for even one game is even
admirable and would be a solid project._

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

_This might be a good idea because it would be an interesting to look at how rules
can interact both with a user and with an AI system. Additionally, testing would be
easy at any point throughout the process because it would just involve writing
rules for the new feature added. It might not be a good idea because it may be too 
ambitious. Also, as mentioned in the sustainability question, it may be a lot of 
semantics without a lot of language decisions._
