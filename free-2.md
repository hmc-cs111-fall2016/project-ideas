# Free project 2


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

This language would help individuals take a more active role in managing their
finances. Currently, small investors have a few options: invest in a large
mutual fund and let the pros take care of it, or subscribe to an online
brokerage site like Interactive Brokers and use their tools. There are two
needs not met by these options: ease of use, and flexibility.

To use tools like Interactive Brokers, the trader must have some technical
knowledge, including familiarity with jargon that may seem arbitrary. For
example, what is a limit order? What is a market order? There are two prices
listed here; will my market order to buy clear at best bid or best ask? A more
intuitive vocabulary could lower the technical barriers of entry to trading.

Algo-trading or high-speed trading is a technique that is all but off limits to
ordinary traders. According to Prof. Evans, most commercial trading software is
written in C, which obviously requires a technical knowledge lacked by most
traders. Why not have a DSL specifically designed to make trading operations
easy, and open up this technique to more than just large corporations?

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

There are so many different types of investment strategies that a user might
want to try that a non-language application would be insufficient. Instead, we
should provide the user with the basic functions of trading and some means for
implementing financial logic, and let the user construct their strategy by
combining these basic functions.

### Why you?
_What excites you about this idea? How did you come up with it?_

I'm currently taking Financial Econ with Prof. Evans, and in a recent lecture
we learned about spread arbitrage and algo-trading, which I found very
interesting. Prof. Evans was careful to point out that, by carefully selecting
stocks which are not heavily computer-traded, a small trader could make a
reasonable profit by implementing a trading algorithm. He even suggested that
we Mudders should try it out.

I believe that this opportunity should be open not just to Mudders and other
technically savvy people, but to anyone with an interest in taking a more
active role in managing their finances.

### Domain
_Describe the project's domain in five words._

Intuitive automation for trading stocks.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

I imagine the language as a set of commands that can be used to describe a portfolio and a strategy. The most basic commands might look like:
```
BUY <x> SHARES OF <company a>
SELL <y> SHARES OF <company b>
```

There should also be some logic associated with these simply buy/sell orders:
```
BUY <x> SHARES OF <company c> IF THE PRICE FALLS BELOW <dollar amount>
SELL <y> SHARES OF <company d> FOR <dollar amount>
```

There should also be a way to interact with the state of the market:
```
IF SPREAD(<company e>) IS MORE THAN <dollar amount> THEN <do something>
```

Finally, the user may not want to specify companies explicitly, but rather execute some strategy for any company that meets a criterion, like:
```
FOR COMPANIES WITH SPREAD <dollar amount> AND VOLUME <shares/day> <do something>
```

I've written these example commands in a natural language-like pseudo-code to
reflect the intention to make the language accessible to nontechnical people.
However, I do not think that natural language is the best way to go (see
AppleScript). One of the challenges in designing the syntax for this language
would be in striking the best balance between preciseness and readability.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When a program runs, the strategy is executed as described by the user. This
will mean placing market and limit orders on the user's behalf, monitoring the
state of the market and reacting as specified, and searching for companies
which meet the user's criteria for being viable target stocks.

Besides the obvious sorts of syntax errors, there are a variety of runtime
errors that we could expect. For example, what should happen if the user's
strategy recommends buying a stock but the user does not have enough liquid
funds in their account? Since trading strategies are often designed to work of
a long period of time, programs written in this language will likely be left to
run unmonitored. Therefore, reporting these errors could be tricky. One
possible solution would be to send the user a notification, maybe via email,
alerting them that a problem has occurred and, if possible, asking them to
choose from a list of potential solutions. If the runtime cannot determine any
potential solutions, it could simply let the user know which part of their
strategy caused the error, and the user could patch up that edge case.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to automate simple trades of the sort that people would
usually just do manually. It should be possible, but probably more difficult,
to specify a sophisticated strategy for engaging in real-time, high-speed
trading. It should probably not be possible to create such a complex and
performant strategy as to be able to compete with the large algo-trading firms,
because including enough features and complexity in the language to enable that
would likely make the language to hard to learn for the target audience.
Instead, user's should be encouraged to select stocks where they will not be
competing with those firms, and the language should provide features which make
it easy to select those stocks dynamically.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

Most online brokers, including Interactive Brokers, offer an
[API](https://www.interactivebrokers.com/en/index.php?f=5041) for customers
interested in automated trading. Unfortunately, these require familiarity with
at least one programming language and environment. For example, the Interactive
Brokers API is exposed to Java, C++, C#, ActiveX, and DDE. Learning any of
these technologies is more than should be required of someone who is not
interested in programming in general, but only wants to be able to perform
automated trades.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

The aforementioned APIs could be used as the backend for the language, so most
of the semantic work would be in translating DSL commands to API calls. While
this would certainly be nontrivial, the APIs would eliminate the need to have a
great deal of technical domain knowledge, so that a CS 111 student could
probably manage at least a prototype of this language.

### Scope
_How big an idea is this? How ambitious is this project?_

I think this project is definitely on the more ambitious side. Implementing the
full language with all of the features I have described would be difficult.
However, a prototype with a limited feature-set would be very feasible for a
half-semester's work. For example, the prototype could have features for simple
market and limit orders, and perhaps leave out the more complex stock-selection
logic. I think this would still be a useful exercise, and if the language were
designed so that the additional features could easily be added in at a later
date, it may even serve as a basis for future work, in or out of class.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

I see this as a good opportunity to combine knowledge from multiple
disciplines, namely CS and economics. In addition, the somewhat large scale of
the project would force the implementer to practice discipline in striving for
a minimum viable product, as they would have to make decisions that prioritize
the more important features and design the language in such a way that it could
grow easily, a la Steele's suggestions.

The scope of the project is also a drawback, because it is unlikely to be
brought to a satisfying conclusion by the end of the semester; there will be
more work to do. In addition, designing a language aimed at nontechnical people
would be interesting, but would probably require the implementer to go out of
their comfort zone.
