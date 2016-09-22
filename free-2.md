# Song Identifier


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

This idea meets the need of people who want to figure out what song they 
heard at the mall or on T.V. but don't remember much of it. Maybe they vaguely
remember some lyrics but not so much the tune. Or maybe they only remember the 
rhythm but don't remember any of the specific lyrics. Or maybe they even just 
remember how they felt while listening to the song. Right now, it's really 
difficult to figure out a song when you only have a vague recollection of it.
Sure, there are song identification apps like Shazam, but it requires you to have
your phone and internet access at that very moment the song is playing. But you
might only realize how much you like the song right after it's over. With my DSL,
the hope is that people will be able to identify the songs they heard in the past,
even if they don't remember much of it, and allow them to discover new ones along 
the way!


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_
A DSL would give the user a large range of methods for identifying a song.
There are basic things like lyrics that the user could input, but they could
input many other features such as the song's genre, mood, volume, and even rhythm
patterns. Rather than acting like a simple search engine, this DSL would allow the 
user to use many different kinds of parameters and combine this information to 
output song suggestions. Overall, the hope is that a user will be able to more
easily identify the songs they want to listen to again with the bits of recollection
that they have.


### Why you?
_What excites you about this idea? How did you come up with it?_

This idea excites me because music is such an integral part of people's daily
lives and discovering new music that one likes is such a great feeling. I came up
with this from talking to my friend who is a fellow music lover and personally just
experiencing a moment where I heard a song I really liked but was unsuccessful in
identifying it. I'm also a huge fan of Spotify and Genius, and I feel like this
project would be a good way to learn about their APIs. 


### Domain
_Describe the project's domain in five words._
Identifying and discovering new songs


### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_

I imagine there being some sort of GUI that allows the user to input all
of the possible ways of identifying the song that they're looking for. The user
could create new categories of identification (i.e. lyrics, rhythm, last location
heard, genre, mood, etc.) and input the information they have on these categories.
Although this wouldn't appear as a traditional programming language, I think this
is important because the user shouldn't have to invest much time in learning how
to use it. It should be intuitive to express the information they have, and the
output (a list of recommendations )should be fairly immediate.


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When the program runs it will query available online song databases, lyric
sites, and Spotify playlists based on the information that the user has inputed. 
It will notify the user if the input paramaters are too large to prevent the 
search from becoming too extensive. If there are no similar song matches, it
will prompt the user to attempt to input more information, but if the user is
stumped, it'll simply recommend somewhat random songs based on the limited
search inputs.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to identify songs and to gather new song recommendations based
on the information the user has on the song they want to find. I suppose the user
could also use it to just generate random songs to listen to based on how they're
feeling, but that would not be the primary purpose of the language, since the goal
is to satisfy the desire to figure out songs that a user has listened to before. It
would probably be impossible to get an output that isn't a song, since the search
query is limited to song or music-related databases; hence, this language is very
domain specific.


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I couldn't find any DSLs that allows the user to determine the search parameters
as well as inputing information to search. I looked at a lot of different music
identification search engines, such as [Musixmatch](https://www.musixmatch.com/) and [SpotSearch](http://www.spotsearch.se/), 
and I also looked at song identication apps, like [Shazam](http://www.shazam.com/) and [SoundHound](http://soundhound.com/),
but they all require specific search inputs. Perhaps this suggests that it 
isn't really feasible to determine a song without very specific search parameters,
and that if the information is organized to loosely than the search outputs will
be too random. Perhaps the limitation is also the sort of music data sets that one 
has access to. 


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I realize that the language design aspect of this project would probably be minimal,
and it's an indea that I would need to reconsider or specifiy better to act like a
DSL. The project is highly dependent on the input, and it gives the user perhaps too
much flexibility in determining what inputs they want to use. So there would definitely
need to be more structure and a sort of paradigm that dictates what kinds of search
parameters and inputs the user can choose from. The "systems" aspect would take up the
bulk of the time, because it would possibly require some sort of algorithm design and
text parsing in order to identify songs. It would also require significant knowledge
of how to use different APIs that contain song or lyric databases.


### Scope
_How big an idea is this? How ambitious is this project?_

Reflecting on this idea, I realize that it was easy to imagine it but seems very
impractical to execute. After thinking about this idea for a bit, I realize that
it is too ambitious because of all of the data I would need access to and a knowledge 
of how to sort through and categorize this data.


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_
In retrospect, I don't think this is a good idea for a project because it doesn't
seem like it will function very well as a programming language. Rather, it might 
just act like a glorified search engine, and executing this would not be the point 
of this project, which is to engage with the mechanics of language design. It initally
seemed like a good idea because I was very excited about having a useful music
application and being able to work withthe Spotify and Genius APIs, and maybe I can
extract more project ideas from thinking about this idea.

