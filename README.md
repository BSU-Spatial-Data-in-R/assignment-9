# Assignment 9: Fitting models to your dataframe

You built a dataframe for analysis in Assignment 7 using the National Forest boundaries that we used in class (I've written a function for you to download and unzip this in the `/code/` folder), a dataset describing the cost of natural disasters fromm 1999-2020 (described in [this paper](https://www.nature.com/articles/s41597-023-01955-0) and available at `/assignment07/ics209-plus-wf_incidents_1999to2020.csv` folder. a land use dataset (`/assignment07/land_use_pnw.tif`), and the wildfire hazard dataset (`/assignment07/wildfire_hazard_agg.tif`). Now it's time to fit some models to explain the cost of natural disasters. By the end of this assignment you should be able to:

* Fit multiple types of models to your data
* Evaluate the performance of your model 
* Generate predictions based on your model


## Instructions

1. After you've joined the assignment repository, you should have this file (named Readme.md) inside of an R project named assignment-9-xx where xx is your github username (or initials).

2. Once you've verified that you've correctly cloned the assignment repository, create a new Quarto document. Name this file assignment-9-xxx.qmd and give it a title (like M Williamson Assignment 9). Make sure that you select the html output option (Quarto can do a lot of cool things, but the html format is the least-likely to cause you additional headaches). We'll be using Quarto throughout the course so it's worth checking out the other tutorials in the getting started section.

3. Copy the questions below into your document and change the color of their text.

4. Save the changes and make your first commit!

5. Answer the questions making sure save and commit at least 3 more times (having 4 commits is part of the assignment).

6. Render the document to html (you should now have at least 3 files in the repository: Readme.md, assignment-9-xx.qmd, and assignment-9-xx.html). Commit these changes and push them to the repository on GitHub. You should see the files there when you go to github.com.


## The Assignment

1. Use the variables that you chose from assignment 7 along with the wildfire hazard and land use dataset to attribute each disaster in the disaster dataset.
2. Fit a Poisson regression using your covariates and the cost of the incident data (using `glm` with `family=poisson()`)
3. Fit a regression tree using your covariates and the cost of the incident data (using `caret` package `method=`rpart`)
4. Fit a random forest model using your covariates and the cost of the incident data (using `caret` package `method= 'rf'`)
5. Use cross-validation to identify the best performing model of the 3 that you fit
6. Convert all of your predictors into rasters of the same resolution and generate a spatial prediction based on your best performing model
7. Plot your result

