# No computer project (Composable Rock Climbing Holds DSL)


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

In indoor rock climbing, a routesetter will take a variety of plastic climbing
holds and arrange them on the wall (which contain holes every three to six
inches) to compose or set a rock climbing route. Climbers then try to ascend the
route. While routesetters can be extremely creative with how they angle the
holds and how they combine them, they are limited by the different shaped holds
they have.

I would like to empower the routesetter with being able to make their own
holds out of reusable composable pieces to allow for more creativity and tighter
budgets. Currently, if a routesetter wants a hold that is a different shape from
what they have, they must purchase it. Additionally, indoor rock climbing would
become a lot more interesting if there were an increased variety of holds
reducing the predictability for climbers. Many gyms purchase all their holds
from the same manufacturer thus frequenters of the gym eventually know exactly
what they are about to grab without getting to it first. In outdoor climbing,
you never know how "good" or "bad" a hold is until you get to it which offers
an extra challenge and more fun!

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

As I mentioned before, if a routesetter does not have a hold in the shape they
want, they must purchase it specially. Creating a physical DSL would allow
routesetters to purchase smaller composable pieces that could be combined to
create holds they envision without having to make extra purchase.

### Why you?
_What excites you about this idea? How did you come up with it?_

Before arriving at college, I used to competively rock climb and thus spent
a lot of time in indoor climbing gyms both climbing and setting routes on
occasion. It would have been a very useful experience to get practice with
a variety of shapes that aren't pre-determined by the manufacturer since when
you go and compete at other gyms and competitions, they will use holds you may
have never encountered before.

I had this idea since I noticed many gyms have to make a huge investment in
differnt climbing holds when at any given time, only half of which are on the
wall. I would like to eliminate the need for needing to have this huge stock
of holds.

To a routesetter, I think it would open up the creative possibilities immensely
by adding another huge factor of variability in the way in which a routesetter
can compose a route.

### Domain
_Describe the project's domain in five words._

Extensible indoor rock climbing routesetting.

### Interface (syntax)
_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

A user would take a rectangular base plat and stack on interlocking dodecahedra
to build the general shape of a hold and then overlay a reusable heatsetting
plastic that can be organically shaped further over the base shape that is
composed from the tesselatting dodecahedra. This final composed piece could then
be fixed to the wall and broken down later to be reused.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When the pieces are composed together, they can then be fixed to a wall and then
a climber could climb on them. While writing a program, a user could try to add
pieces that don't fit together and they will physically notice this and be unable
to do so.

Structurally a routesetter could create a hold that is not physically sound which
they would find out through testing.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to make new climing hold shapes and hard to create structurally
unstable shapes. It should be easy to spot an error when composing pieces and
impossible to not lock pieces together.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There exist climbing holds that are meant to be rotated to simulate different
positions. However, there are not holds to make other holds. By adding the option
of this, we extend the creative possibilities infinitely.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

A lot of time would be needed to best determine what shapes to make the base
pieces out of and then work on how they would structurally fit together. Once an
initial design is set out, it would be necessary to model them and physically
produced them&mdash;perhaps on a 3D printer. They would then need to be tested
and refined further to come up with an actual useable piece.

### Scope
_How big an idea is this? How ambitious is this project?_

This project would be particularly challenging since it ultimately involves
physical prototyping and testing. Even a 3D model of it would be fairly
complicated becuase it involves many pieces being put together.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea
project?_

This is an interesting take on DSLs and would be very fun to work on since it
is not directly involving a computer; however, because of the prototyping and
physical limitations it may not be suited for this course. It would create
a new and interesting way to create holds, but perhaps it is not for the better.
The current methods do provide a lot of variablity and do not require constructing
each hold manually which is a time consuming process.
