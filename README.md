Final Project — Annotated List of R Functions
=============================================

-   [Mandatory deadlines](#mandatory-deadlines)
-   [Guidelines](#final-project-guidelines)
    -   [Annotating the R functions](#annotating-the-r-functions)
    -   [List of R functions](#list-of-r-functions)
    -   [Merging into the master branch](#merging-into-the-master-branch)

Mandatory deadlines
-------------------

-   **Annotations first draft:** 12:00pm noon on Thursday, June 21st

-   **Peer reviews:** 6:00pm on Thursday, June 21st

-   **Annotations final draft:** 9:00am on Friday, June 22nd

Read the section [**merging into the master branch**](#merging-into-the-master-branch) for instructions on the peer review process.

Guidelines
----------

**Purpose** — A significant portion of the course is dedicated to learning how to use R and the `tidyverse` ecosystem to wrangle and explore data, and then analyze it using statistics. Remembering the different functions, how they are used, and what problems they solve requires consistent practice and review. This is why it's important to have a set of notes that explain how a function works in your own words, which can be referenced long after you've completed this course.

**For your final project** — Each student will be assigned a set of functions that we used during the course that you are responsible for annotating. Everyone's annotations will need to be merged into a single, uniform document that will ideally serve as a useful reference after the course is complete. To get the class started, this starter repository has been set up with a notes template containing a pre-filled example for the `ggplot2` syntax and how to use `geom_histogram()`. Use these examples as inspiration for how to put together notes on the other functions in R.

### Annotating the R functions

Unless told otherwise, when writing notes for a function, include the following:

-   The function's name

-   The important inputs

    -   If the input was used in class or for a homework assignment, then it's important

    -   For `ggplot2` functions, include a separate subsection for important aesthetic mappings (see example in your template file)

-   A summary — 1 or 2 sentences — of what the function does

-   An example showing how to use the function

    -   **Your example cannot use the same dataset as the examples found in the help documentation or from class.** For example, when explaining the `dplyr` function you should not use the `presidential` dataset, but you *can* use a dataset from one of the homework assignments.

### List of R functions

Your notes should discuss the following packages and functions:

-   The [`ggplot2`](http://ggplot2.tidyverse.org/) package

    -   `geom_histogram()`, `geom_boxplot()`, `geom_point()`, `geom_bar()`, `geom_col()`, `stat_ecdf()`, `geom_smooth()`, `facet_wrap()`, `facet_grid()`

    -   Basic instructions on how to change the axes labels and give the plot a title

-   The [`readr`](http://readr.tidyverse.org/) package

    -   `read_csv()`, `read_rds()`, `write_csv()`, `write_rds()`

-   The [`dplyr`](http://dplyr.tidyverse.org/) package

    -   `select()`, `slice()`, `rename()`, `recode()`, `arrange()`, `filter()`, `mutate()`, `group_by()`, `summarize()`, `count()`, `cume_dist()`, `combine()`, `pull()`

-   The [`tibble`](http://tibble.tidyverse.org/) package

    -   Instructions on manually creating a data frame using `data_frame()`

-   The [`tidyr`](http://tidyr.tidyverse.org/) package

    -   `gather()`, `spread()`, `separate()`, `unite()`

-   The [`rvest`](https://github.com/hadley/rvest) package

    -   Instead of notes for each function, describe the procedure for using the [SelectorGadget extension](http://selectorgadget.com/) with `read_html()`, `html_nodes()`, and `html_text()` to perform basic webscraping tasks

-   Statistics functions

    -   Summary statistics functions: `mean()`, `median()`, `sd()`, `IQR()`, `min()`, and `max()`

    -   Linear modeling: `lm()`

    -   Instructions on how to create a Q-Q plot using `geom_qq()` from `ggplot2` and then plot the **ideal reference line** to check for deviations from normality

-   The [`infer`](https://github.com/andrewpbray/infer) package

    -   Describe the inputs for the four functions: `specify()`, `hypothesize()`, `generate()`, and `calculate()`, see the [class 16 slides](http://summer18.cds101.com/doc/class16_slides.pdf) for guidance

    -   Instructions **with an example** on how you use `infer` to conduct a hypothesis test: how you simulate the null distribution, and how you calculate the *p*-value

        -   Test must be between two variables (one response variable and one explanatory variable), one explanatory variable must be categorical, the response can be either categorical or numerical

        -   Example should show how we compute the *p*-value for a one-sided test and for a two-sided test

    -   Instructions **with an example** on how you use `infer` to find a confidence interval using bootstrapping, including how you would find different size intervals, for example a 90% interval or a 95% interval

        -   Confidence interval must be computed for a **difference** of two values, such as *means* or *proportions*

        -   Consult the [class 17 slides](http://summer18.cds101.com/doc/class17_slides.pdf) for guidance on how to correctly compute the upper and lower bounds!

-   The [`modelr`](https://github.com/tidyverse/modelr) package

    -   **An example** of showing how to plot a simple linear model with one explanatory variable on top of the data in a scatter plot using `data_grid()` (or `seq_range()`), `add_predictions()`, and `geom_line()` from `ggplot2`

    -   Instructions **with an example** on how to use `add_predictions()` to create *observed versus predicted values* plots

    -   Instructions **with an example** on how to use `add_residuals()`, `add_predictions()`, and `geom_ref_line()` to create *residual versus predicted values* plots

    -   Instructions **with an example** on how you interpret the *observed versus predicted* and *residual versus predicted* plots to determine whether the conditions for using a linear model are met: **linearity**, **nearly normal residuals**, and **constant variability**

Remember, these notes are ultimately for you, so think about what you would find helpful when you refer back to these.

### Merging into the master branch

Students will complete their annotations in separate branches of the final project repository, writing their annotations under the appropriate header. When your annotations are complete, you will need to have your work merged into the `master` branch of the repository. Before you can do this, you will need to have your work edited and reviewed by one of your classmates. This will be completing using Github's **Pull Request** functionality. The instructor will set up the **Pull Requests** and assign the peer reviewers. In order to indicate that you are ready for a review, you should post the following in the discussion box of the **Pull Request**:

> My annotations are ready for review @username

**You will need to replace `@username` with your reviewer's actual Github username.** You should also send your reviewer a direct message on Slack or email him or her to begin the review. After you receive your feedback, you will use the suggestions to update and correct your submission. After your edits are complete and commited to your branch, message the instructor on Slack to check to see that you've satisfied the reviewer's comments. If you have, the instructor will approve the merge and add your contribution to the master version of the document.

-   **First drafts of your annotations must be commited to your branch by 12:00pm noon on Thursday, June 21st**

-   **Peer reviews must be completed by 6:00pm on Thursday, June 21st**

-   **Final edits should be commited no later than 9:00am on Friday, June 22nd.**

