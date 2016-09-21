# Free project 3 - Form-Fitting Venn Diagrams

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Venn diagrams display data in a cool and organized way. Many programs or apps 
already exist for drawing Venn diagrams, but the ones I found don't adjust the 
circles according to the text within. For example, some programs make the users 
specify the exact size of the circles and data. Thus, it takes many tries to 
format venn diagrams exactly as envisioned. But what happens if the data 
changes? Then people would have to repeat this struggle.

I want to design a DSL that, given text for each circle (and intersection of 
circles), creates an image rendering of the venn diagram with the text snugly 
inside the circles. Basically, circles are auto-formatted according to the text.


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

At first, I was debating if this should be an app or a language. But I think I 
can make it a language if I break down venn diagrams into "data", "category", 
"unions", and "intersections", and "none" (things outside all the circles). 
Then, it's just a matter of creating the data for each category and 
intersecting them.

Thus, users can easily create data (building blocks) and connect them 
through intersections.

### Why you?
_What excites you about this idea? How did you come up with it?_

![venn diagram image](/Cyberchase.png)

Yes, I watch Cyberchase. It's a great show.

Wouldn't it be nice if our data could obediently go into their assigned 
circles?

### Domain
_Describe the project's domain in five words._

Venn diagrams with fitted text.


### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

I might create text files that contain information about the data and how they 
relate to one another.

This creates a venn diagram of fruits organized by color.

```
R = strawberry, apple, raspberry
Y = banana, lemon
B = blueberry

R and B = grape, prune
R and Y = orange, peach
B and Y = lime, kiwi

R and Y and B = rotten fruit

None = blackberry
```

Making the data and connections simple is the right direction for creating a 
DSL that can be understood by new and old programmers. I might have to clarify 
the categories though.


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When a program runs, the text file containing the info is sent through a 
parser. Then the DSL tries to create a venn diagram with the given information. 
For now, I was thinking of using a command-line interface, but I would 
eventually evolve to a user interface.

Some errors include not having enough information (i.e. creating an 
intersection without the two corresponding categories). I could either throw 
error message or create an image of the intersection without the two 
categories. Obviously, this makes my work harder but then users can see that 
they're missing something.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to create venn diagrams with text that fit inside the circles.

It is possible (not necessarily difficult) to create art with circles and text, 
especially if I allow unicode characters with funky symbols.

It should be impossible to do my Algs homework, do math, make sounds, or really 
anything outside of art.


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There are tons of venn diagram makers on the internet. They're more like apps 
than DSLs. I only looked at a few that didn't make me pay or register.

[Meta Chart](https://www.meta-chart.com/venn) has a venn diagram maker, but 
users must specify the size of the circles. Sizing the intersection is the most 
unintuitive part because the size is represented by a number, and it is unclear 
how the intersection size relates to the other circles. It also takes many 
trials to form-fit the data with the circles.

[SoftSchools](http://www.softschools.com/math/venn_diagram/venn_diagram_maker/) 
also has a free venn diagram maker. This is more closely to my idea of 
simplicity. Instead of worrying about the size number, users can create circles 
by dragging the corner of the image (a common image resizing technique). While 
it is more intuitive that Meta Chart, SoftSchools still runs into the problem 
of readjusting the circle sizes if the text changes drastically.


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I think this is a 50-50 language/system project. Rendering images is the most 
"systems" aspect. And if I make a user interface, I'll spend a lot of time 
working on that (I don't have much front-end experience). But I will have 
to think a lot about the underlying language design. I have to consider what is 
"intuitive" to humans (unions vs. OR, intersections vs. AND) and how to make it 
easy to create intersections.


### Scope
_How big an idea is this? How ambitious is this project?_

Venn diagrams should be simple enough to do in a half-semester. I'm worried 
that this project is on the boring side, but maybe that's because I'm not a 
target user. Rather, I think elementary teachers and business people are more 
likely to use this project.


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This project can make people's lives easier because they don't have to struggle 
with other computer programs (or messily sketch by hand). It can add fluency to 
otherwise unintuitive apps that focus on the exactly formatting of both the 
circles and the text. My DSL would allow auto-formatting of the circle, 
eliminating one user-controlled variable.

On the other hand, I'll only be the 1000th person to try making venn diagrams 
on a computer. Another drawback is that without a user interface, it'd be hard 
for non-programmers to use my DSL. They won't learn programming languages just 
to make a venn diagram. But I should design my DSL in code before making a user 
interface.
