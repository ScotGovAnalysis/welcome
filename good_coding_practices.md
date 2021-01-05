This document is a work in progress

# Good Coding Practices
Making code easier to understand and modify without changing it's behaviour

### Code Smells

> "Code smell is an evocative term for that vague feeling of unease we get when reading certain bits of code. It's not necessarily wrong, but neither is it obviously correct. We may be reluctant to work on such code, because past experience suggests it's going to be fiddly and bug-prone. In contrast, there's another type of code that just feels good to read and work on." - [Jenny Bryan](https://github.com/jennybc/code-smells-and-feels#:~:text=GitHub%3A%20%40jennybc%20%22Code%20smell%22%20is%20an%20evocative%20term,suggests%20it%27s%20going%20to%20be%20fiddly%20and%20bug-prone.)

## Contents
- [Make a README](#make-a-readme)
- [Use a style guide](#use-a-style-guide)
- [Write code for humans](#write-code-for-humans)
- [Comment code](#comment-code)
- [Avoid absolute file paths](#avoid-absolute-file-paths)
- [Keep scripts short](#keep-scripts-short)
- [Use functions](#use-functions)
- [Automate checks for input data](#automate-checks-for-input-data)
- [Code in the open](#code-in-the-open)

## Make a README 
  * Here is the [Gov Data Science guidance on writing READMEs](https://gds-way.cloudapps.digital/manuals/readme-guidance.html#writing-readmes)
  * Include
      * Contact details
      * How to run the code
      * A licence (Scottish Government default is [Open Government Licence](http://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/))
      * An estimate of run time if it takes longer than a couple minutes
  * README's should help the user: 
      * Understand what the project is
      * Learn how to use the project
  
## Use a style guide 
* The default for Scottish Government is the [Tidyverse styleguide](https://style.tidyverse.org/)
* Lint your code
    * **Linting**: The automated checking of your source code for programmatic and stylistic errors
    * [Lintr](https://github.com/jimhester/lintr) checks your code for style, syntax errors and possible semantic issues
* Use meaningful object names
    * `height_in_metres()` is better than `converter()` for a function that converts height into metres. This makes it more obvious what your code is doinganmd makes your code more readable

## [Write code for humans](http://douglasorr.github.io/2020-03-data-for-machines/article.html)
> "Code is read more often than it is written." — [Guido van Rossum](https://twitter.com/gvanrossum) (creator of Python)

> "Programs are meant to be read by humans and only incidentally for computers to execute." — Donald Knuth, The Art of Computer Programming"

Writing code that humans can understand is an investment to have maintainable and reusable code. If it is easy to read, maintenance and  will be much quicker in the future and it will be much easier for other people to work with your code. 
The shortest, most efficient code for the computer is likely not the optimal code for human readability. 

### Do
* `casewhen()` creates an a more readable way of dealing with many ifelse statements. `ifelse` statements can be very useful but can become hard to understand if too many are used.
### Don't
* Use deeply nested `for` loops or `ifelse` statements

## Comment code
> "When you feel the need to write a comment, first try to refactor the code so that any comment becomes superfluous." – Martin Fowler, Refactoring

### Do
* Where neccessary, comment code 
* Use comments to break up the code sections (Ctrl + Shift + R)
    ```
    # Load data ---------------------------

    # Clean data ---------------------------
    ```
* Explain _**why**_ it is doing what it is doing. This will make it easier for users to know what the code is for

    #### Good Comment:
    ``` 
    data %<% 
       select(1:161)  # column 161 is where the data stops and it becomes footnotes
    ```
    #### Bad comment:
    ``` 
    data %<% 
       select(1:161)  # selecting columns
    ```

### Don't
* Just explain *what* it is doing
* Remove any commented *just-in-case* code that isn't needed
* Rely on (un)commenting code to change behaviour
    * You can quickly lose track!

## Avoid absolute file paths
### Do
* Use relative file paths
    * Use the library [`here()`](https://www.rdocumentation.org/packages/here/versions/1.0.0)
      * `here()` finds your project files based on the current working directory at the time when the package is loaded.
    * Work within an [R Project](https://support.rstudio.com/hc/en-us/articles/200526207-Using-Projects)
      * R Projects act as your working directory, where the root is the directory created, or chosen, when setting up a new project.  
### Don't
* Use absolute file paths as this reduces the reproducability of the code
    * It won't work on another users computer
    * It won't work if any files move
      
## Keep scripts short
### Do
* Ideally keep to fewer than 250 lines. This makes scripts more manageable
* Break up and `source()` sections like data processing, and variable or function assigning
### Don't
* Keep everything for a large project in one script  
    * For example, break up the UI, Server & Golbal sections of a large [Shiny app](https://shiny.rstudio.com/articles/basics.html)

## Use functions
  * Functions allow you to automate common tasks rather than repeatedly writing the same code. [R for Data Science](https://r4ds.had.co.nz/functions.html) provides a good explanation for using functions. 
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
### Do
* Coding in the open encourages:
     * The use of good code practice so others can read your code
     * Collaboration
     * Code reviews and [pull requests](https://docs.github.com/en/free-pro-team@latest/desktop/contributing-and-collaborating-using-github-desktop/creating-an-issue-or-pull-request)
* Code in the open if you can, e.g. use [Data Science Scotland GitHub](https://github.com/DataScienceScotland)
### Don't
* Share sensitive information such as unpublished data, API keys or passwords

