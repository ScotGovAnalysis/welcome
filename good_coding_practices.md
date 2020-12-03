# Good Coding Practices
Making code easier to understand and modify without changing it's behaviour

### Code Smells

"Code smell is an evocative term for that vague feeling of unease we get when reading certain bits of code. It's not necessarily wrong, but neither is it obviously correct. We may be reluctant to work on such code, because past experience suggests it's going to be fiddly and bug-prone. In contrast, there's another type of code that just feels good to read and work on." - [Jenny Bryan](https://github.com/jennybc/code-smells-and-feels#:~:text=GitHub%3A%20%40jennybc%20%22Code%20smell%22%20is%20an%20evocative%20term,suggests%20it%27s%20going%20to%20be%20fiddly%20and%20bug-prone.)

## Contents
- [Make a README](#make-a-readme)
- [Comment code](#comment-code)
- [Use a style guide](#use-a-style-guide)
- [Avoid absolute file paths](#avoid-absolute-file-paths)
- [Keep scripts short](#keep-scripts-short)
- [Nested for loops and ifelse statements](#nested-for-loops-and-ifelse-statements)
- [Use functions](#use-functions)
- [Automate checks for input data](#automate-checks-for-input-data)
- [Code in the open](#code-in-the-open)



## Make a README 
  * Here is the [GDS guidance on writing READMEs](https://gds-way.cloudapps.digital/manuals/readme-guidance.html#writing-readmes)
  * Include
      * Contact details
      * How to run the code
      * A licence (SG default is [OGL](http://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/))
      * An estimate of run time if it takes longer than a couple minutes
  * README's should help the user: 
      * Understand what the project is
      * Learn how to use the project
      
      
## Comment code
  * Where neccessary, comment code 
  * **DO** 
      * Explain _**why**_ it is doing what it is doing. This will make it easier for users to know what the code is for
  * **DON'T** 
      * Don't just explain *what* it is doing
      * Remove any commented *just-in-case* code that isn't needed
      * Don't rely on (un)commenting code to change behaviour
          * You can quickly lose track!
  
## Use a style guide 
  * The default for Scottish Government is the [Tidyverse styleguide](https://style.tidyverse.org/)
  * Lint your code
      * **Linting**: The automated checking of your source code for programmatic and stylistic errors
      * [Lintr](https://github.com/jimhester/lintr) checks your code for style, syntax errors and possible semantic issues
  * Use meaningful object names
      * `height_in_metres()` is better than `converter()` for a function that converts height into metres. This makes it more obvious what your code is doinganmd makes your code more readable
  
## Avoid absolute file paths
  * **DO**
      * Use the library [`here()`](https://github.com/krlmlr/here)
      * Work within an [R project](https://support.rstudio.com/hc/en-us/articles/200526207-Using-Projects)
  * **DON'T** 
      * Use absolute file paths as this reduces the reproducability of the code
          * It won't work on another users computer
          * It won't work if any files move
      
## Keep scripts short
  * A reasonable length is ideally less than 250 lines. This keeps them more manageable
  * **DO**
      * Break up and `source()` sections like data processing, and variable or function assigning
  * **DON'T**
      * Keep everything for a large project in one script
          * For example, break up the UI, Server & Golbal sections of a large [Shiny app](https://shiny.rstudio.com/articles/basics.html)
  
 
  
## Nested for loops and ifelse statements
  * **DO**
      * `casewhen()` creates an a more readable way of dealing with many ifelse statements. `ifelse` statements can be very useful but can become hard to understand if too many are used.
      * **Stop Early!** Move quick `stop()`s and `return()`s to the top of the function
          * * When `if` statements `stop()` or `return()` they do not need an else
          * [Example](https://github.com/rhi-batstone/code_best_practice/blob/main/early_stops.PNG) from [Jenny Bryan](https://github.com/jennybc/code-smells-and-feels/blob/master/2018-07_user-brisbane-bryan.pdf)
  * **DON'T**
      * Don't use deeply nested `for` loops `ifelse` statements
   
  
## Use functions
  * **D**on't **R**epeat **Y**ourself [(DRY)](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)
      * If you are repeating code, create a function to do it for you
  * Use several smaller functions rather that one large one. This includes small, well named, helper functions
  * Use the built in proper functions to simplify 
      * `if(is.numeric())` is better than `if(class(x) == "numeric" || class(x) == "integer")`
 
## Automate checks for input data
  * Automate the new data checks so you don't miss anything unexpected. Especially if you expect the data to be updated
  * For example, automate checks for:
      * Outliers
      * NA's
      * Class
      * Expected column names
      
  
## Code in the open 
  * Code in the open if you can [Data Science Scotland GitHub](https://github.com/DataScienceScotland)
  * Coding in the open encourages:
      * The use of good code practice so others can read your code
      * Collaboration
      * Code reviews and [pull requests](https://docs.github.com/en/free-pro-team@latest/desktop/contributing-and-collaborating-using-github-desktop/creating-an-issue-or-pull-request)
  * **DON'T**
      * Share sensitive information such as unpublished data, API keys or passwords
  
## Reduce object clutter
  * If you have many objects, consider nesting them into a list to keep the environment tidy



