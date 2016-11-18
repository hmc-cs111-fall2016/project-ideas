# Free project 1

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.

The project would serve people interacting with html and do web development. I
think a language that can streamline the writing of html and its interaction
with javascript and css would greatly benefit people that use these
technologies. There currently are a few (many) javascript modules and libraries
that try to do this. For example, jquery makes it easier to manipulate html on
a webpage. However, as we saw in class, jquery's syntax was very verbose and
at many points confusing. It has become bloated to become a large library. Most
casual users who just want to build a simple website do not need jquery.

I am looking more at something like JSX (https://facebook.github.io/jsx/).
However, JSX only officially works within the React framework. I like JSX due to
its clean syntax. If a DSL that uses JSX's syntax or something similar to
interact directly with how to write HTML and javascript for a page, then it
would be very nice.

### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

Writing HTML, CSS, and javascript is often more verbose than it needs to be,
often very repetitive (all the closing tags and so forth). People often have to
write long and winded HTML and CSS. Mix that with the fact that many normal
javascript functions are extremely verbose. A DSL that can clean everything up,
making all the components that are involved in web development easier to read
and debug, woudl be very helpful.

I am helping the people that do casual web development and don't necessarily
need or want all the APIs the javascript language itself provides. Their
experience right now is writing and reading very long files that really are not
that complex. But because of all the "FormComponent" and "createClass" funcs,
it takes long to write. Worst of all, it is hard to come back to and debug
because of the unnecessary complexity.

These people's experience with web development would be nicer, easier, and they
will be faster. If they don't need to close every tag, if they can just write
shorter functions and keywords that can be translated into normal (and longer)
HTML, CSS, and javascript, then their lives would be easier and more efficient.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

Because the DSL would be adding an abstraction layer over what they do now. The
DSL would allow the users to not have to touch the bare-metal code, but instead
write things that are shorter (i.e. shortcuts) that can be translated/compiled
into the correct code. It addressed the need by shortening the development time
and making code in this format nicer to read and debug.

### Why you?
_What excites you about this idea? How did you come up with it?_

This project idea excites me because I've written a lot of HTML, CSS, and JS in
the past year. I've explored many tools and framework that make things easier.
A good example is React. With React, I used the JSX syntax, which I thought was
a good abstraction that made code shorter to write than if I had written the
same things in plain javascript. However, it also didn't lose any meaning - once
I got the translation/abstraction, the code was cleaner to read, shorter, and
easier to debug. However, JSX is mostly accessible in React. Also, it would be
a little different (in my mind) if something similar could be used to write
html, css, and javascript without the React framework (as JSX is very custom for
React and things related to how React is used), so more work would be needed and
it would not just be a simple port from JSX.

### Domain
_Describe the project's domain in five words._

Making webdev easier and nicer.

### Interface (syntax)
_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

The user will interact with the language through coding. Programming would look
like the user is writing a dialect/hybrid of HTML, CSS, and JavaScript, but with
nicer syntax. This is the right way to interact with the problem domain because
people will still need to write code, but a DSL can make that simpler and nicer.
Since they are already writing code, they are not the people that use Wix or
Squarespace to create websites through drag-and-drop, but they would not be
averse to coding. However, they would be more efficient with smaller syntax and
needing to write less code.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

It should be able to compile and translate what the user has written in this
shorter syntax into proper HTML, CSS, and Javascript.

The possible errors that might occur are bad syntax from the user. This can be
communicated to the user through errors during the translation, or through
modifying the files (like what git does when there is a conflict).

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

Writing html/css/javascript should be easy to do in this language. Perhaps
deeper manipulations that should be done in pure javascript should be possible,
but difficult (and syntax would potentially be ugly, defeating its purpose).
Doing backend, none front-end work should be impossible or very difficult. This
means interacting with databases and servers should be impossible or very
difficult.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

Yes there are - I already gave an example of JSX
(https://facebook.github.io/jsx/). Others include handlebars
(http://handlebarsjs.com/) and dust (http://www.dustjs.com/). They address the
same need in different ways. Handlebars and dust both still suffer from too much
syntax. Thus, it is very hard to just pick up and read a file written in dust.
JSX is just the right amount of trimming and keeping the code informative, but I
am definitely biased as I worked with JSX for many months and am used to reading
JSX.

Each of the examples I gave try to make HTML/CSS/JavaScript easier to write, and
they succeed in different ways. JSX makes everything into an XML-like structure,
which is really nice for keeping track of things, especially in more complex
components. Handlebars make writing HTML like writing a json object, which is
very nice since it escapes the need to write tags (something that just grinds my
gears!). Dust also encourages you to abstract away the logic of your web page,
and its abstractions are a little less obvious.

The parts of the language that can be improved would be the kind of abstraction
they do. JSX is very nice in that it is very easy to blend javascript and HTML.
Handlebars makes it super easy to write HTML, but the javascript side of things,
in my experience, seem to get a little ugly because of some its language design.
Dust has the issue of just not letting you incorporate, well, any javascript in
your page, which I think is definitely an issue since though the target audience
probably do not do the most complex web development work, some flexibility in
allowing them to use some JavaScript (that which has not been nicely abstracted
for the user in this DSL) is a nice feature that would make the DSL more widely
used.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Probably half and half. If a nice language design can be done to meet some/all
of these goals, then it would be a useful DSL. Since there are very few examples
of DSLs in this domain that seem to be have "a nice language design", a lot of
effort will have to be spent on making design decisions.

Since this DSL will probably have to parse code that the user inputs, a lot of
effort will have to be spent on that front as well. Though, with a good language
design, the parsing and background abstraction translating/compiling should be
relatively easier.

### Scope
_How big an idea is this? How ambitious is this project?_

Seeing as there aren't that many DSLs in this domain, and depending on how much
of the web dev things this DSL should abstract, this can be quite a large idea.
Many projects and frameworks have aimed to "make web development easier" with
varying levels of success. This is definitely ambitious.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea
project?_

This would be a good idea for a project because it covers an interesting domain,
its implementation incorporate interesting things, and its langauge design
aspect would be very important.

This might not be a good idea for a project because it can potentially be very
broad. It would be hard to control the scope and estimate the time and effort
needed to implement all the designs.
