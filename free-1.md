# Free project 1 - Musical Ornaments Sampler

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Classical and baroque music often feature musical 
[ornaments](https://en.wikipedia.org/wiki/Ornament_(music)), such as trills, 
mordants, and turns. These serve as embellishments to the overall melody.
However, ornaments are quite ambiguous in how people should play them. 
Different composers interpret them differently, and even time period affects 
when ornaments should be played in relation to the beat. Unless musicians are 
well-versed in music history, they may not realize the specific interpretations 
desired by each composer. 

Of course, people might argue that music should be left ambiguous because music 
is a subjective art. However, if musicians want to play according to a 
composer's style, they must learn and understand the different interpretations 
of musical ornaments.

I want to help musicians hear the subtle differences among various 
interpretations of the same ornament through a computer program. Currently, 
people have been hard-coding trills and turns, but they are inflexible about 
tempo and different interpretations. My project would generate short music 
samples featuring these ornaments as well as the various interpretations. Then, 
I would play them back to the user so they can see and hear these differences.


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

The current problem is that one ornament marking can have many different 
interpretations. A grammar can help improve the clarity of these notations. 
Moreover, if I can break ornaments into small pieces, then it is easy to 
concatenate these snippets and play them back to the user. Creating these 
building blocks is part of language design.


### Why you?
_What excites you about this idea? How did you come up with it?_

I had played piano before college (mostly un-classical music), but I just 
started taking piano lessons at Scripps. Playing ornaments isn't difficult in 
itself, but I don't have the intuition of knowing what specific composers want. 
I am gradually gaining experience with different composers' interpretations, 
but I think it would be nice to have a computer program to help other musicians 
understand musical ornaments.

My biggest inspiration happened during piano lessons last week. My teacher 
was talking about baroque music when she pulled out a giant poster (with tiny 
font) of musical ornaments and how different composers played them. Looking 
at it was overwhelming because the notes were so complicated!


### Domain
_Describe the project's domain in five words._

Generating and playing ornament samples.


### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

In the very far future, I want users to snap pictures of small music pieces, 
send it through my DSL, and then hear different interpretations come out of it.

But since I have no computer vision experience, I'll settle with this:

```
// Assume 12-tone equal temperament system

turn = { 
	key = C
	turnBase = C
	relative = 0 1 0 -1 // C D C B pattern
}

trill = {
	key = C
	trillBase = C
	relative = 0 1 // C D pattern
}

play(trill * 1/2, turn) // play trill for a half-note, followed by a turn
```

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When a program runs, it will try to compose ornaments based on the given data. 
Then, it will play the notes (possibly through MIDI). I also want a component 
that suggests different composer's interpretations, but I don't know how. I'm 
also not sure how viable this project is.

One error is not using pitches within the 12-tone equal temperament system. 
That would be the user's fault and I would throw an error explaining that. 
Another error is not constructing the trill as the user wants it to be. I'm 
still not sure how the language will be designed, but I want to make it easy to 
construct ornaments. Hopefully I can get user feedback that asks if my 
rendering matches their expectations.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to create musical ornament patterns and play them back 
through audio.

It would be possible to manipulate this program such that people can compose masterpieces based on slow trills and other ornaments.

It is very difficult for this language to do my Algs homework or anything 
unrelated to music. But even non-ornamental music would be difficult to 
generate or play because the focus is on fast embellishments, not actual 
melodies.


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I haven't found any DSL that specifically does this. I was thinking about 
Musescore, which is a program that allows users to compose music digitally. 
Musescore is great as a composition software, but playback is secondary, so 
Musescore does not play trills or turns (only marks the notation). 
According to this [forum](https://musescore.org/en/node/56281), some people 
have tried to hard-code ornament playbacks, but they are inflexible about 
different tempos and interpretations. 

Coding musical ornaments is difficult precisely because of their many 
interpretations; there is no one way to play them. Thus, I think Musescore 
avoids implementing trills and turns due to potential arguments about the 
"correct" way to play them.


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Honestly, a lot of this work would focus on the "systems" aspects because 
dealing with audio is hard. And I'm not sure how this DSL would be implemented. 
But breaking ornaments into small patterns is a part of language design. 
Moreover, the language design involves connecting these pieces not only in 
sequence, but also by tempo and other embellishments.


### Scope
_How big an idea is this? How ambitious is this project?_

This is an ambitious idea because I'm trying to encode music that 
currently has ambiguous encodings. I also have little direction into my 
project, so it feels big.


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This might be a good idea because I am trying to make different musical 
interpretations clearer. In addition, this could potentially be used by people 
in the music domain, since ornaments are difficult for computers to express.

One drawback is that I can't see how this DSL would grow. There is only a 
finite number of ornaments and a finite number of interpretations, even if this 
number is large. And I want to limit this interpretation project to just 
musical ornaments. I'm not saying DSLs must grow, but at the same time, aren't 
well-designed languages able to grow?
