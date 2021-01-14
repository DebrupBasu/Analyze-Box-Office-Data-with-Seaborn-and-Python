# Analyze-Box-Office-Data-with-Seaborn-and-Python
Part 1
Task 1: Data Loading and Exploration

   
Load the data sets into memory using pandas and display the first few entries. The TMDB data set contains 7400 movies and a variety of metadata.

Task 2: Visualizing the Target Distribution

The TMDB Box Office Prediction database was initially released so that teams could treat it like a regression problem and predict the worldwide box office revenue of 4400 movies provided in the test file. 
    We will use this feature rich database for data analysis and data visualization in this project. 
    In the next project, we will use the same database for feature engineering and feature visualization.  
    To proceed to feature analysis, we first need to visualize the target. Using Seaborn's distplot function, we will plot the distribution of movie revenues. To illustrate the skew, we will also plot the distribution of revenue on a logarithmic scale using np.log1p.

Task 3: Comparing Film Revenue to Budget

 Just as we did in Task 2, we will create two subplots: one for the distribution of the budget; the other to plot the log budget against log revenue. 
    Perform the log transformation to make the distributions more manageable. 

Task 4: Do Official Homepages Impact Revenue?

 Use the data to demonstrate the effect of an official homepage on movie revenue. 
    Create appropriate features to indicate the presence of official movie homepages. We can use Seaborn's catplot function to plot the revenues for movies with and without homepages using our newly created features.

Task 5: Distribution of Languages across Films

  As Hollywood is known globally, we would expect the data to support our intuition that English movies generate the highest revenue. 
    In this task, we will use box plots to test this hypothesis. We might be surprised that our intuitions about the world may not always align.

Task 6: Common Words in Film Titles and Descriptions

  Identify trends across movie titles and descriptions and their effect on revenue. 
    Generate word clouds for movie titles and descriptions. Word Cloud is a data visualization technique used for representing text data in which the size of each word indicates its frequency or importance. 

Task 7: How do Film Descriptions Impact Revenue?

  To identify which words have the highest impact on revenue, we tokenize and vectorize movie titles and descriptions, fit a linear regression model to it, and use ELI5 to display the high impact words.


Part 2

Task 1: Analyzing Movie Release Dates

   In Part 1, we focused on exploratory data analysis. In this task, we identify the release_date column as ripe for feature engineering.

Task 2: Preprocessing Features

   Before we can create new features based on release_date, we need to define a function to process the dates and convert them to a standard datetime format. 
    Perform data imputation to account for missing values, after which we will apply our processing on the training and test sets.

Task 3: Create Features Based on Release Date

   Now that we have standardized the date format, define a function to create new columns for the year, weekday, month, week of the year, day, and quarter. 

Task 4: Using Plotly to Visualize the Number of Films Per Year

   We will use Plotly to create an interactive visualization of the number of films released per year in both the training and test sets.   
    We use the generic go.Scatter function from plotly.graph_objects, and specify the mode argument to choose between markers or lines. 

Task 5: Number of Films and Revenue Per Year

   In this task, we will visualize both the number of films and total revenue per year, and the number of films vs the average revenue per year. 
    We will be able to compare and contrast trends we observe to that of the previous task.

Task 6: Do Release Days Impact Revenue?

   Is it reasonable to assume that movies released on weekends will gross higher revenues? 
    Let's put this assumption to the test in this task by creating a categorical plot of the day of the week on the x-axis and revenue on the y-axis. 
   

Task 7: Relationship between Runtime and Revenue

   We will create two plots in this task. The first describes the distribution of the duration of films. The second plots revenue against duration. Let's find out if the data illustrates the optimal duration of a movie to maximize revenue.
