# Data-Modeling
Modeling and combination of 7 different Excel workbooks into a single consolidated file

# Introduction: 
This is part of my virtual experience program with forage working under an Accenture North America (abstract) as a virtual analyst. 
After going through my brief carefully, it states that my client wanted to see an analysis of their content categories highlighting the top 5 categories with the largest aggregate popularity.
My first task was to clean and model the data, and finally identify the columns that will be useful to achieve the goal of the analysis and merge them all from the provided datasets.
To complete this task, I used my knowledge of data Modeling learnt during the #30daysoflearning.


# Problem Statement: 
This exercise required three tasks to be completed:
1. Requirements Gathering: This involves looking at the goal of the project started in the introduction above then think about and determine which available datasets will be required to get the job done.
2. Data Cleaning: This ensures that the data is clean and ready for analysis. The end result should be a set of relevant data sets that are clean with each data set containing only the columns which are relevant to the completion of this task.
3. Data Modeling: Finally, the knowledge should be used to create a final data set containing all of the columns that will be needed to complete the task.

# Data Sourcing: 
I was provided with seven CSV files containing tables which I was to work with. The files were:
1. Users: This provides the code for all users that have interacted with the different contents and provided a reaction.
2. Profile: This provides basic information about the users including their age.
3. Session: This provides information about the amount of time and the type of device used during the interaction with the client's content.
4. Location: This provides information about the location of the users.
5. Content: This provides information about the type of content that was uploaded.
6. Reaction: This provides information about the reaction types of the users to the contents.
7. Reaction types: This is a fixed list of scores awarded by the client to different reaction types.

# Data Cleaning & Transformation:
After a critical review of the task, I came to realize that only 3 tables are important for the task. Which are
✓ Content
✓ Reaction
✓ Reaction types

The data was imported into power querry, ensured appropriate data types, removed empty rows and cleaned the data appropriately.

# Data Modeling: 
I started with the Reactions table as my base table, which shows all the reactions to particular content IDs, then I merged the content table to the reaction table using a LEFT JOIN and on the content ID. This will now allow us to categorize all the reactions received base on content categories.
I thereafter also used merged the newly formed table with the Reaction types table using LEFT JOIN, on the various reaction types and then assigned popularity scores to the various reactions received.
This formed a full new table containing all required columns for the analysis. I then closed and loaded the data into a worksheet, ready for analysis

# Data Analysis: 
Since, the client wanted to see the top 5 most popular content categories, I created a pivot table that groups all the reactions by content categories and sums the scores for each category, then filtered by sum of scores to show the top 5.
