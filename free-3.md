# Free project 3 (Computer Science Grading)

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

Grading in computer science becomes a difficult and involved task with large
classes. Many times a grader will leave the same comment on multiple students
code and have to specify where a students code went wrong and why they deducted
points on a rubric.

It would be useful if we adopted the DRY approach to grading and removed the
need to create redundent information. There should be a consice way of saying
on a rubric the line(s) of code that caused you to deduct points.

Natural language rubrics are not easily analyzed beyond scores in large categories.
By creating a formal markup, we could better summarize behaviors of students and
graders.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

Graders in CS are usually pretty comfortable with programming, so a language
would fit in. Furthermore, creating a formal DSL will require the graders to
be more precise in their feedback and allow professors to analyze larger grading
trends.

Having the feedback in a machine readable form would allow us to present it to
users in different ways and make it searchable.

### Why you?
_What excites you about this idea? How did you come up with it?_

Last semester I created an automated grading system that integrated testing
results with point assigned rubrics to automatically populate an electronic
rubric that TAs could comment and override. This system could only support
key value pairs and specific code comments were left on PDFs later on which felt
redundent.

### Domain
_Describe the project's domain in five words._

Efficient code feedback and grading.

### Interface (syntax)
_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

I imagine a program to look something like this:

```
include: common
assignment: "Hello, World"
feedback:
  style::category:
    -1 @ {1:56}: :common.problems.variables.names
    -0.5 @ {47:*-50:*}: :common.problems.semicolons
    -2 @ {62:*}: custom.("Custom deduction method comment")
```

that produces output like:

```
1> int a_var = 123123120931923012;

1 point was deducted based on the above line.
Please make sure you choose names for your variables with meaning.

47> public class MyObject {
48>    public MyObject(int x, int y) { super();;;;; }
49>    public void get() { return this;;;;;;; }
50> }

0.5 points were deducted based on the above lines.
Please make sure you only use one semicolon.

62> int myInt = 0;

2 points were deducted based on the above lines.
Custom deduction method comment.
```

where you can specify categories and then specific line numbers that describe
the deduction (or simply leave a comment).

I think this make sense since it is easy to read and efficient to write. It could
be presented alongside the document in the appropriate place making it more
readable.

Defining a grading "grammar" that can be course specifc with namespaced shortcuts
for longer comments creates a more efficient grading experience. It also allows
us to analyze trends. If we notice a bunch of `common.problems.semicolons`, we
can look into it further. Without a DSL, we have don't have an easy way to notice
trends across graders and students in larger courses.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When the program runs the feedback will be processed step by step expanding
each comment and point deduction into a formal document that is human readable.
It will link libraries and custom definitions and include the human readable forms.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to create custom categories and comment short cuts. Like those
in `common.*`. It should also be easy to do math in the points section, but nothing
more complicated than `+``-``*``\`. It should be impossibe to run or modify code
and override the overall structure of the rubric document.

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

Rubrics are currently in use, but other than that there is not a good way of giving
feedback that is correlated with point loss unless you are using a custom system.
I think because the syntax would take a bit of learning it has not been done yet.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Most of this project would be spend creating the architecture that translate the
markup document to  human readable form since the langugae will only have very
basic grammars and words and mostly rely on custom extensibility by the user.

### Scope
_How big an idea is this? How ambitious is this project?_

While this would be a neat project, it is not overly ambitious since its scope
is small and does not require a complicated syntax. The grammar for the project
would be fairly easy to define since it would be intentionally limited.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea
project?_

I think this is a good idea since the scope is sized reasonably where an end-to-end
product could be produced by the end of the semester (or, at the least, an MVP).
Any new grading schemes or tools are risky since they may effect the efficiency
of graders which has high stakes for students and budgets. Personally,
