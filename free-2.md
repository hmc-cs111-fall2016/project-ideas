# Free project 2 (Intelligent Playlists)


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

Playlists of songs are currently a simple ordering of specific tracks to play.
If a music listener wants to hear new music without explicitly saying what
they want to hear they may turn to discovery services like Spotify or Pandora;
however, these services lack fine-grained control over what songs you listen to
usually relying on factors like what you've listened to in the past and whether
or not you thumbs up a song.

It would be extrmeley nice if one could specify with more paramaeters what they
want to listen to. For instance, specify a genre and a deviation from that genre,
the number of songs per artist or band to be played in given amount of time, or
beats per minute of a song in the playlist.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A simple thumbs up or thumbs down (or even an invisble predictive algorithm) do
not offer enough control. With a DSL, one could specify what they want to hear
with more expressiveness and clarity. This DSL would need to be more natural
feeling than most programming langugaes to engage the most number of users.

### Why you?
_What excites you about this idea? How did you come up with it?_

This was a personal idea generated out of my frustration with Spotify's auto playlists
being too redundent and wanting a way to specify weights for artists and bands
that I wanted to listen to.

I ran it by a few friends to get their feedback and they thought it would be a
neat idea to pursue and implement.

### Domain
_Describe the project's domain in five words._

Intelligent and controllable playlist creation.

### Interface (syntax)
_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

Since this langugae would target people with a variety of backgrounds in programming&mdash;
mostly people without experience&mdash;I imagine a Scratch-like visual language.

The blocks however, would be more tailored to music playlists. Some examples include:
+ artist: specifies an artist of a song
+ band: specifies a band
+ song: specifies a song name directly
+ not: negates an expression so you could express things along the lines of
       "I don't want to listen to ABBA".
+ redundency: number of songs belonging to an entity and a time in which you
  would like to hear them
+ divergence: specify the divergence factor from the current song
+ bpm: specifies beats per minute of the song

While I think it may be easier to implement a DSL that looks like a programming
langugae, a visual language would be easier to learn and an artistic
component to the playlist. Each playlist would, through its visual prgamming,
have its own artwork/fingerprint.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

A program will begin at the start node and work its way down through the flow
of the playlist making choices for next songs based on the current node it is
in. A song will play (or be queued up) and retrieved from a library of music.
With each step, the computer will indicate which block it is on making it easier
for users to adjust it. Ideally this DSL would have access to Spotify or
another music service where we have a large volume of choices and freedom to
play them.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to make an ordered playlist like the traditional method and
it should be easy to pick random songs or albums. New discovery should be easy.
It should not be able to cut tracks; it should be able to play them back at differnent
volumes and maybe speed up or slow them down. It should not be a DJ program.
It should be possible to reproduce a playlist through seeding random generators
so I could share a playlist with you that you could then edit to your own liking.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

After researching other DSLs in this domain, the closest I could find would
be DJ programming and sound manipulation lanaguges. I think there isn't one
specifically for playlists (unless you count "thumbs-upping" or "-downing" a song)
since people don't want to put much effort into making a playlist. I think, however,
that a few minutes of time investment upfront could make for a much better
playlist listening experience.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

This project would require user reasearch determining the best way to create
a DSL that is easy to grasp for users. Maybe the visual idea is not any easier
than creating a typed PL in the classic sense.

Once the langugae is created and an interpreter is built, there will be a fair
amount of backend work to feed off Spotify&mdash;although they have a really
useful and easy-to-learn API.

### Scope
_How big an idea is this? How ambitious is this project?_

If the project involves making a typed DSL (typed as in using a keyboard not
in the sense of datatypes) it will be less big of a project compared to having
the goal of creating a visual language/program.

Ultimately, the backend will be quite a bit of work: how does one compute
the "divergence" of songs? Interfacing with a music library will also be fairly
challenging.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea
project?_

Many people could use this, but for the most part, people are already satisfied
with the way they listen to music. It could help people discover new music, but
for users who already know exactly what songs they want to listen to, it seems
like a DSL would make more work for them.
