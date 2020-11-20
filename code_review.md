This document is a work in progress

# Code review guidelines for R users

> “The idea of code review is pretty simple: have other people review the code after someone wrote it.” - [Karl E. Wiegers](https://egoless.tech/code-review-essentials/)

## Checklist for reviewers
First make sure you understand the real-world context behind the code and the problem it is trying to solve. Ask the author if you’re not sure. Summarise your review before going into detail and always try to include some praise. There is no such thing as perfect code or a complete review. So maximise the impact of your review by limiting yourself to no more than:
* 1 hour of your time
* 300 words
* 10 most important points

### Expected behaviour during code reviews
Adapted from [Code Health: Respectful Reviews == Useful Reviews](https://web.archive.org/web/20201106154227/https:/testing.googleblog.com/2019/11/code-health-respectful-reviews-useful.html):

#### Both parties
* Assume competence and ask questions to gain understanding
* Provide rationale or context such as a best practices document or a style guide
* Don’t criticize the person. Instead, discuss the code

#### Reviewer
* Provide specific and actionable feedback
* Clearly mark nitpicks and optional comments with the prefix ‘Optional’

#### Author
* Clarify code or reply to the reviewer’s comment in response to feedback

Use this list as a prompt for what to review. But don’t feel limited by it. You can bring other things to the review that you think will help the author.

### Clearly organised files
Is it clear which file is the overarching script (i.e. that runs through all necessary steps and scripts)? Can you easily see how all the files relate to each other? Could scripts be split into categories? For example: utility functions, data import, and graphical output.

### Good coding practices
Don’t go into detail on specific style issues. If style comes up, recommend tidyverse and lintr.

### Does the code run?
Does it produce the expected and correct output?

### Understandable code
Would a new start have difficulty understanding?

### Complex, outdated, or unusual code
For example:
* Maps made with sp instead of the more modern sf
* Homemade functions or a non-Tidyverse function when Tidyverse would suffice
* Did the code need to be explained to you? Could it be simpler?

### Tests
Is input data being automatically checked for validity and sanity?
Are there any cases where it might break?

### Praise!
Did the author do something well?
Did you learn something from their code?

> If you’re reviewing the code of a more experienced coder, it is a chance to learn and you have every right to ask for an explanation if there’s something that is unclear. It’s in everyone’s interest that you understand what you’re reading and it could be that you don’t understand it because the author has made a mistake or over-complicated something. - [MOJ DASD Coding Standards](https://moj-analytical-services.github.io/our-coding-standards/)

## The benefits of code reviews
Adapted from [Humanizing Peer Reviews](https://web.archive.org/web/20200923160357/https:/www.processimpact.com/articles/humanizing_reviews.pdf):

### Benefits for analysts
* Better structured and documented work that is easier to understand and modify
* Better techniques learned from other developers
* Less time spent reworking code
* More robust designs that tolerate change
* Ability to use results from previous reviews to make decisions

### Benefits for managers
* Improved teamwork, collaboration, and coding skills
* Reduced chance of errors in outputs
* Increased chance of completing the project on time
* Reduced lifetime maintenance costs, freeing resources for other work
* Reduced impact from staff turnover through cross-training of team members
* Better and earlier insight into project risks and quality issues

## Volunteer as a reviewer
You are welcome to volunteer as a code reviewer; regardless of experience. Follow these steps:
1. Read/watch these materials (~90 mins):
    1. [Code Review Essentials](https://egoless.tech/code-review-essentials/)
    1. [Code Review Guidelines for Humans](https://phauer.com/2018/code-review-guidelines/)
    1. [Implementing a Strong Code-Review Culture](https://www.youtube.com/watch?v=PJjmw9TRB7s)
    1. [Humanizing Peer Reviews](https://web.archive.org/web/20200923160357/https:/www.processimpact.com/articles/humanizing_reviews.pdf)
1. Add your name to this list and [let Joseph Adams know](mailto:joseph.adams@nrscotland.gov.uk)
