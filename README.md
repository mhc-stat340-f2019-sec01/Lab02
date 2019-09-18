# Lab 02

## Description

Data on driving incidents was collected for all 52 states in the United states.
This lab will explore whether or not state-level factors contribute to Car insurance premiums.
The original goal of this dataset was to determine which state had the worst drivers.

![insurance](https://github.com/mhc-stat340-f2019-sec01/Lab02/blob/master/featured.jpeg)

## Organization

Instead of having a separate repository per student, we're going to work collaboratively in a single repository.  You can work by yourself or with another student in a team.

On the GitHub repository page for this lab, click "Fork" in the top right corner.  This will create a copy of the lab repository in your own account.  You will then clone this repository to RStudio.  If you're working in a team, only one of you needs to fork the repository.  Once you have cloned the repository, create a new .Rmd file with a name like "Lab02_teamname.Rmd", specific to your team.  In that R Markdown file, complete the Lab Tasks and Discussion items outlined below.  Then commit and push your work to GitHub.  Your work will go to your forked version of the repository.  Once you're ready, submit a pull request to merge your work back into the main class repository.  I'll demo how to do this next week Monday.

## Lab Tasks

* read in the data set `data/bad-drivers.csv`
  * (recommended) rename the columns to shorter nicknames (check out the `names` function)
* exploratory data analysis
  * present some pictures and a brief description of trends you see in the data, and how they may influence fitting a model.

* regression analysis
  * The target variable for our regression models is `Car Insurance Premiums ($)`
  * fit a simple linear regression model and save this model as `reg01`. 
  * fit a multiple linear regression model that includes the variable you used in your simple linear regression and save this as `reg02`.

* Cross-validation
  * **For both reg01 and reg02**
    * split your data into 5 cross-validation folds.
    * program a for loop that trains your model on 5 pieces of the data and evaluates on the "held-out" dataset.  (This for loop should iterate over all 4 training, testing sets.)
    * compute the MSE for each test set
    * compute the MSE averaged over each test set
  
## Discussion

  Please explain your model, making sure to reference the coefficients of the model and their significance.
  
  How does your multiple regression model compare the simple linear regression model, and how would you communicate these results to an audience? 
  
  How does the cross-validation MSE compare between your simple and multiple regression models?  What does this mean?
