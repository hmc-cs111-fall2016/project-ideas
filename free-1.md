# Free project 1

## The user and a language
This section describes who the project would serve and why a language might be a good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

I wish to create a DSL that makes it easy for users to plan a diet/meal.
A lot of applications allow users to record what they've been eating and 
tell them how much calories they've consumed. However, it's hard to find 
anything that helps users plan meals beforehand, taking their dietary 
restrictions, specific goals of their diet (e.g. how much weight they wish to
lose), what kind of diet they want to be on (e.g. cutting carbs, cutting 
sugar) into consideration.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

This DSL will make it intuitive and easy for users to specify the type of 
diet they want to be and specity their own amount of calories they would like to consume. For example, they would be able to customize their meal plans
by defining their diet as a variable, and they would be allow to call functions on the variable for miscelleneous settings. Then, at the end, the program will return a specific meal plan or instructions for the user.

### Why you?
_What excites you about this idea? How did you come up with it?_

Recently, I decided to be on a diet and tried out a few weight 
loss apps. Usually, the way they work is that they let the user
know the amount of calories consumed and nutrition facts.
While this is useful, I found it frustrating that none of the 
apps help the user plan meals beforehand and their inference of 
whether diet is going well or not is soley based on the number of
calories.

### Domain
_Describe the project's domain in five words._

customized planning of diet meals

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

I vision that the user would be led to define their diet as a variable and call
different functions on the variable to specify different settings like diatary restrictions. Some of the basic fucntions would be something "remove" to remove any ingredients that the user is allergic to and "cut_half" to cut things like carbs in half of what they usually consume.

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

Perhaps, the program can be run on terminal and at the beginning, it will list
all the available functions. First, the user would be asked to name their diet, therefore, defining a variable, and then call different functions on the 
variable (this can be done one by one, or in a batch mode). And when the user calls a function that indicates the end of setting up, the program will return specific instructions or meal plans for them. 


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

Things that are easy to do in this langauge are specifying different settings for the users' meals and, unlike any other apps of this sort, to have different settings for breakfast, lunch, and dinner, or different days of a week. 
Something that would be difficult is to track their meals. Since there are a lot of apps that allow the user to record their meals, I feel that there's no need for this DSL to do so. This DSL's featuers will mostly focus on helping the user do something about their diet/meals beforehand, rather than afterwards. 


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well do they address the need? Are there any particularly admirable qualities of thelanguage? Are there parts of the language you think could be improved?_

One of the apps I mentioned I tried out is "myfitnesspal" (https://www.myfitnesspal.com/), which is essnetially a calorie counter. It makes it easy for the user to track what they have been eating and count calories they've been consuming. However, again, it does not let the user plan meals beforehand or evaluate how they are doing on their diet based on anything other than number of calories.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I believe building the systems aspects of the project would take slightly longer than the language aspects. 
A public API for myfitnesstracker or other calorie counters might be used.


### Scope
_How big an idea is this? How ambitious is this project?_

The project is not that ambitious in a sense that it does not have too many features or complicated settings, since the goal of the project is to let the user specify their needs intuitively and very simply. However, I can imagine this DSL being integrated into some of the calories counter/weight loss apps.

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea project?_

I believe this project is suitable for the DSL class, because its domain is very narrow and specific. 
I can imagine running into problems when trying to use the API of the calorie counter/weight loss apps due to their limited access for the public.

