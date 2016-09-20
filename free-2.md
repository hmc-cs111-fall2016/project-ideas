# Free project 2
DSL for trading stocks

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

This DSL would allow people to have more control over how they buy and sell
shares.  Currently, most people invest in the market over long-term periods. 
Alternatively, they give their money to a hedge fund, who will buy shares for
them.  These hedge funds use complicated algorithms to determine at what price to
sell a stock, and how long it should be available for.  However, these techniques
or not available to typical investors.  Also, the code is typically written in C
for efficiency.  A DSL for the Stock Market would help people want to precisely
control the timing and price of their shares but do not want to give their money
to a hedge fund.  With this DSL they could create functions that react to the
market to determine the best investment strategy. 

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL is appropriate for users for a couple of reasons.  First of all, many people
who buy shares may not be familiar with coding.  Therefore, an API might be
a barrier to entry, and a language for this domain could be more accessible. 
Also, you could optimize this DSL for speed.  For the stock market, milliseconds
could make a huge difference, so it would be better to use a DSL that you can
optimize for this specific case than a general purpose language.  With a DSL, you
might also be able to create more complicated investment strategies that are based
off of market activity.

### Why you?
_What excites you about this idea? How did you come up with it?_

Jeb originally came up with this idea as we were watching lectures for Financial
Economics.  I am intrigued because this domain seems perfect for a DSL.  In our
lectures, Prof Evans talked about how traders would write their code using C to
make it as fast as possible.  He then talked about using Python to write C code,
and it seemed very cumbersome.  Their should be a language specific to stocks,
perhaps that compiles into C code, that is more intuitive.  Also, it seemed like
only hedge funds use code, but it should be possible for normal investors to have
finer control over their money.

### Domain
_Describe the project's domain in five words._

Market orders and limit orders.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

Users could create a list of different "strategies" (that could have parameters).
This "strategy" would return whether the user should place a limit or market order
to buy or sell, and at what price.  This strategy could take a stock as a
parameter and call other functions that look at the existing bids and offers to
determine the price.  It also might make sense to have different "states" so that
at a time you might want a stock to use a different strategy.  This way will allow
you switch between strategies easily and apply the same strategy to multiple
stocks.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

First you would list the stocks and strategies that you are interested in trading.
When you run a program, it would constantly evaluate all of your stocks and
determine whether the strategy says to buy or sell.  There are a few possible
types of errors.  First of all, if one of your strategies hits an infinite loop
then it would never get to evaluate the other strategies.  You could have a
background process that makes sure none of the strategies takes too long to
evaluate, and send an error message to the user.  Also, the program should make
sure that the results make sense, and that the user doesn't do something
strange. If shares cost $10 market price, the user shouldn't be selling them for
$1.  You could build these tests into the language, so that the user could make
sure that the functions return values they intend.  If it ever hit one of these
errors, then the trade wouldn't occur and an error message would appear.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to do anything specific to the domain, namely posting market
and limit orders.  It should also be easy to encode simple investment strategies
that depend on market prices.  It should also be easy to create many strategies,
switch between them, and apply different stocks to the same strategy.  Creating
more complicated strategies, for example ones that involve machine learning, might
be out of the scope of the domain, and could be difficult with this language.  In
order to allow users to customize their investment strategy as much as possible,
the language might have to allow for enough options to make the language Turing
complete.  Therefore, anything that is computable would hypothetically be
possible, but hopefully very difficult.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I do not think there are any DSLs in this domain.  I believe this is the case
because Prof Evans mentioned that brokers go at great lengths to write C code.  In
addition, if they use Python code to create C code, this is a pretty good
indication that no such DSL exists.  There are APIs from various
financial services companies like ETrade. However, these APIs pose the same issues
as mentioned above, specifically that they could be inaccessible to inexperienced
coders.  Also, these APIs seemed more specific to creating "custom trading
applications" instead of simple investment strategies.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

My initial impression is that the "systems" aspect would pose a significant
hurdle.  From there, you could start with a minimal language that only allows you
to view and post limit orders and base much of the syntax off of another language
like Python.  You could then build the language and create new syntax for the DSL.
The complicated parts of the "systems" include extracting online data about the
price of stocks, and allowing the user to specify a stock from an online list. 
Also, there are many security issues involved, since you wouldn't want to be able
to write a program that would trade somebody else's stocks.  To be a usable DSL,
the security issue could be a very time-consuming task.

### Scope
_How big an idea is this? How ambitious is this project?_

This idea is certainly bigger than the calendar DSL, and perhaps too big to be
done in a semester.  Both the language and the systems part could balloon to be
formidable tasks.  The systems part involves creating a secure way buy and sell
stocks, which could get complicated.  It would be possible to have the DSL merely
calculate what the user _should_ do, and leave the actual trading for the user,
but that would defeat the purpose of making it fast.  An ideal possibility would
be to leverage some existing trading API that already deals with security.  Also,
the language could get complicated, sense I would like to give the user as much
freedom as possible.  According to Prof Evans, many strategies involve complicated
algorithms and machine learning, and this could make the scope of the project
quite large.  However, if we keep the domain to less-complicated trades then that
could keep the scope of this project reasonable.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This could be a good idea because it meshes nicely with another course that I am
taking.  As I am learning about strategies in one class, I can apply them in
another and vice versa, which would improve my understanding in both.  In
addition, it is a topic that I am interested in, and I genuinely feel that this
domain could use a language.  The biggest issue could be the scope.  On the
systems side, this would involve learning some potentially undocumented APIs to
obtain data about the prices of stocks.  In addition, making a secure platform
seems like it would take a lot of time.
