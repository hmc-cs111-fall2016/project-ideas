# Free project 2


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_
My domain specific language would help people who play fantasy sports games,
most specifically (fantasy soccer)[https://fantasy.premierleague.com/].
Oftentimes, fantasy sports leagues are created with entrance fees and prize 
money involved. Therefore, it is important to keep track of your squad and team
throughout the season. However, it is nearly impossible to _always_ substitute
injured or unavailable players before each gameweek because of the inherent
nature of time: injuries can happen at any minute, and we can't keep constantly
check our fantasy sports. I propose creating a DSL that a) allows people to 
create the most optimized team selection at the beginning of the season, and b)
substitute and trade players in their squad automatically.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_
A DSL is appropriate because fantasy sports are very click-heavy and it does
not make sense for it to be. Optimization problems where you are given limited
funds and asked to make the best decisions are solveable by computing and
mathematics, so there should be some automation and algorithms involved despite
the "any given Sunday" nature of sports. Through a language, it is
possible to ask and answer more optimization questions. It's also possible to
run a script at particular time intervals to check for injuries and such.

### Why you?
_What excites you about this idea? How did you come up with it?_
I was an avid fantasy sports player, but I haven't participated recently
because I was losing my entrance fee every single year without ever winning,
largely because I couldn't discipline myself to check the fantasy league
consistently. Therefore, I think it makes a lot of sense to automate fantasy
sports for the mundane things like substituting injured players. Furthermore, I
find it ridiculous that there isn't a way to mine the fantasy database such that
I can create the best team.

### Domain
_Describe the project's domain in five words._
Automating and optimizing fantasy sports. 

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 
I imagine the language would look similar to the following: 
```
account = new Account(user, authToken)

account.OptimizedTeamSelection(
	Budget: 100m, 
	NumberPlayers: 15,
	MinimumOffence: 8.5,
	MinimumDefence: 4.0
)

account.UpdateTeam(
	Injuries: True,
	Suspensions: True,
	CheckInterval: 1.0,
)


```

The OptimizedTeamSelection function would take in parameters to customize
the type of players a user wants for their team, and the UpdateTeam function
takes in parameters to update the team at specified intervals. This currently
lacks fluency, so there would need to be more options and customization.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_
When the program runs, for the optimized team function, we'd output some JSON or
other data format with the players selected and their traits to allow the user
to assess whether this is the team he wants to select. For the update team
function, we would update the user's fantasy team on the fantasy
sports website.  Errors may be if the account does not exist, if the buget is
too low. This would be outputted when the script is run in some pop-up
notification possibly from the browser since we will be trying to access the 
account in the browser. 


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_
It should be easy to express what type of players you would like in a fantasy
team and as a result get the optimized team for the constraints given. It should
also be easy to access the fantasy players database and identify the best
available players given certain constraints. Furthermore, it should be easy to
automate checking unavailable players on your team and specify intervals
to automatically update the players on your roster. It should be impossible to
do almost anything else. We want this to be the case because this is for a very
specific domain and we don't want to do be able to do anything else.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_
No there are currently no DSLs in this domain. This is almost certainly because
there is no open API for accessing the fantasy sports data. There is an API
available for Yahoo sports fantasy, but it seems there are no programs to interact
with this. 

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_
I imagine language design would not be a lot of the time spent because it will
be very limited.  Interacting with the browser and re-creating the data set in
absence of an API would be the bulk of the time spent on this.

### Scope
_How big an idea is this? How ambitious is this project?_
This is not that ambitious in my opinion. I feel that the more difficult part of
this is creating a top notch algorithm rather than designing a great language.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_
This would be a good idea for a project because I think if done properly and
well, it could impact many people given that the fantasy sports community is 
large.  However, it would not be that great because I feel that the language 
design aspect is very limited, and this seems to be more of an API or 
command line application more than anything.
