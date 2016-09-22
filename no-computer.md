# No computer project


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

My language is for people who want to tell a story, but don't have the time or ability to write down everything that's in their head. It will allow a creator to organize many little stories so that a common story emerges from the collection. I believe, with Bret Victor, that there are many people with ideas trapped in their heads, and that too often these ideas come out "stillborn or stunted".

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

How else would you tell a story? All I want to do is change the granularity of the language used, from English words to mini stories. A language also makes sense here because it presents a great opportunity to design an extensible language: users can write and add their own mini stories to the set, and they can share their extensions with the community.

### Why you?
_What excites you about this idea? How did you come up with it?_

Funnily enough, the night before writing this response I was contemplating the
idea of telling a story through a series of short, unrelated anecdotes. I find
it fascinating that a deep character can be developed just by giving away brief
flashes of their life, and I like the way the selection of which stories to
tell has roughly as much impact on the big story as the content of the small
stories does. But as interesting as this idea seems, I wondered when I would
have time to try it.

Today, as I was rewatching Victor's talk, desperately hoping that his ideas
would stir something up in me, it just clicked. Victor perfectly describes the
tragedy of lost ideas, and I realized that my idea could easily become one of
them, just because of lack of time. And worse -- how many people with similar
ideas can't get their ideas out? How many stories will be lost? Anything that
might prevent that from happening excites me.

### Domain
_Describe the project's domain in five words._

Big stories emerging from small.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

The syntax of the language consists of a set of short, unrelated stories, somewhere between a paragraph and one to two pages. All the stories are told from the first person. The narrators are not necessarily the same, but not necessarily different (this means that consistency is important; details from the different stories cannot contradict each other). There should be stories told about various times in the narrator's life, from childhood to adulthood. The stories should cover a range of emotions and character traits, and they should range from hilarious to harrowing.

These stories can be printed on cards, from which the creator can choose a subset to put in any order to create the life story of the narrator, told in chunks. Even though the stories are not related, I believe that the language will have fluency as an emergent property; the more one reads of the assembled story, the more one will feel as if they know the narrator. The character will be developed as much through the contents of the stories as through the creator's judgment of what the narrator should choose to reveal about him or herself.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

A "program" running means someone reading the assembled work of the creator. As
this happens, the reader will (hopefully) enjoy the individual stories. After
having read enough of them, they will start to develop a picture of the
narrator, hopefully learning something new about the character with each mini-
story. Ideally, the stories would start to change in meaning depending on the
context established by the particular set of stories chosen, and the order they
are placed in. In this way, the reader may even see the same mini-stories in
several different big stories, without realizing or caring about the
repetition.

The only errors I can think of are consistency errors, which are liable to
happen with this kind of collage literature. These would have to be
communicated through feedback to the creator and to the authors of the mini-
stories which conflict. This is where the language needs an active community if
it's to work. Given that, errors could be shared via this community.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to create a story with a single narrator whose life makes for
an engaging story. It should be difficult but possible to craft a more
complete, linear, chronological life story, as opposed to a story which gives
the reader a feel for the character but leaves gaps in the timeline or
otherwise neglects some details. It will be impossible to create stories that
do not follow the first-person isolated stories form.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There are similar DSLs. In HSA 10, Creative Disruption, I learned about several
of them. I believe the Oulipo created a few, although I'm finding it difficult
to remember specifics and I'm not having luck Googling. I remember one in
particular, although I can't recall the title or author. The story was printed
on large stylized playing cards, and each card focused on a different member of
the royal court. The story was a mystery, and by shuffling the cards, the user
could change the outcome of the story.

I am not aware of any DSLs which focus specifically on developing a character
via narrative, like the one I have proposed here.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

This language is unique in that almost the entirety of the design process would
be consumed by creating the vocabulary, the "keywords". In this case,
"keywords" are short stories of several hundred words or more. While designing
the keywords is technically a part of designing the language, it fails to
address many of the interesting parts of language design which we're learning
about in this class.

### Scope
_How big an idea is this? How ambitious is this project?_

This depends entirely on how big the "starter set" of stories is going to be.
It would not be difficult to write, say, 10 to 20 short stories in the course
of the semester. It would be impossible to write 50, especially since the
difficulty of the task will increase exponentially with the number of stories
as coherency and consistency becomes an issue.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This language illustrates the benefits of a scalable language, and the
community aspect of it is interesting. That is something that none of my other
projects address as directly as this. I also think a log of very interesting
"programs" could come out of this language, which makes it an intriguing
project.

The major drawback is as described above: most of the time creating this
language would be devoted to writing, not necessarily to designing the language
itself from a big picture perspective. This would be enjoyable, but might be
out of place for a CS class, as opposed to an English class.
