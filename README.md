# Accenture-North-America (Social Buzz Analysis)
I am currently working as a Data Analyst at Accenture, where I collaborate within a larger team, with each member having distinct roles and responsibilities. Our team has recently been assigned a new project for a client named Social Buzz. This opportunity is particularly exciting for me, as I hope to earn a promotion, and it provides a chance to showcase my data analysis and visualization skills.

## Task 1: Project Understanding
My first task is to read the brief from Social Buzz and complete a short knowledge check before the call. 

####  What To Do?
- Understand the client and business problem at hand.
- Identify the requirements that need to be delivered for this project.
- Identify which tasks to focus on as a Data Analyst.


## Task 2: Data Cleaning & Modeling
Identify which datasets will be required to answer the client’s business question, Clean the datasets and merge them to prepare the data for analysis and determine the answer to the client’s business question
The client has sent through:
- 7 data sets - each data set contains different columns and values
- A data model - this shows the relationships between all of the data sets, as well as any links that you can use to merge tables.

 ####  What To Do?
- Requirements gathering
- Data cleaning
- Data modelling

**Tool Used:** Google Sheet

**Step 1:** So, the first step is to use the  data model provided to identify which datasets will be required to answer business question - which is to to figure out the top 5 categories with the largest popularity.

Solution: (Data set required)
- Reaction dataset
- Content dataset
- Reaction Types dataset.

NOTE: Popularity is quantified by the “Score” given to each reaction type. We therefore need data showing the content ID, category, content type, reaction type, and reaction score. So, to figure out popularity, we’ll have to add up which content categories have the largest score.

**Step 2:** Data Cleaning
Data cleaning is a common and very important task when working with data.

What you need to do:
First: Open the three data sets

Second: Clean the data by:
- removing rows that have values which are missing,
- changing the data type of some values within a column, and
- removing columns which are not relevant to this task.
- Think about how each column might be relevant to the business question you’re investigating. If you can’t think of why a column may be useful, it may not be worth including it.

**Step 3:** Data Modelling

SOLUTION:

Step 3.1: Duplicate Reactions sheet and rename the copy to Cleaned Data
Open Cleaned table.
Insert two new columns for Category and URL after the last column of your Reaction table.

Step 3.2: Use VLOOKUP for Content_Type
In the first cell of the Content Type column (e.g., E2), enter the following formula: =VLOOKUP(B2, Content!B:E, 3, FALSE) then,Drag the fill handle down to apply the formula to the rest of the cells in the Category column.

Step 3.3: Use VLOOKUP for Category
In the first cell of the Category column (e.g., F2), enter the following formula: =VLOOKUP(B2, Content!B:E, 4, FALSE) then,Drag the fill handle down to apply the formula to the rest of the cells in the Category column.

Step 3.4: Use VLOOKUP for URL
In the first cell of the URL column (e.g., G2), enter: =VLOOKUP(B2, Content!B:F, 5,FALSE) then,Drag the fill handle down to apply the formula to the rest of the cells in the Category column.

**Step 4:** Merge with Reaction Types
- In Cleaned data , insert two new columns for Reaction Sentiment and Reaction Score
- In the first cell of the Reaction Sentiment column (e.g., H2), enter: =VLOOKUP(C2, ReactionTypes!B:D, 2, FALSE) then,Drag the fill handle down to apply the formula to the rest of the cells in the Category column.
- In the first cell of the Reaction Score column (e.g., I2), enter: =VLOOKUP(C3, ReactionTypes!B:D, 3, FALSE) then,Drag the fill handle down to apply the formula to the rest of the cells in the Category column.

**Step 5:**  Figure out the Top 5 performing categories

First: Add up the total scores for each category. To do this, open a new sheet, name it as Popular Category and fill column A with Category from Cleaned data and in column B1 write "Scores" then use the following formulars to get the scores.
- Studying: =SUMIF('Cleaned Data'!F:F, 'Popular Category'!A2,'Cleaned Data'!I:I)
- healthy eating: =SUMIF('Cleaned Data'!F:F, 'Popular Category'!A3,'Cleaned Data'!I:I)
- technology: =SUMIF('Cleaned Data'!F:F, 'Popular Category'!A4,'Cleaned Data'!I:I)
- food: =SUMIF('Cleaned Data'!F:F, 'Popular Category'!A5,'Cleaned Data'!I:I)
- cooking: =SUMIF('Cleaned Data'!F:F, 'Popular Category'!A6,'Cleaned Data'!I:I)
- dogs: =SUMIF('Cleaned Data'!F:F, 'Popular Category'!A7,'Cleaned Data'!I:I)
- soccer: =SUMIF('Cleaned Data'!F:F, 'Popular Category'!A8,'Cleaned Data'!I:I)
- public speaking: =SUMIF('Cleaned Data'!F:F, 'Popular Category'!A9,'Cleaned Data'!I:I)
- science: =SUMIF('Cleaned Data'!F:F, 'Popular Category'!A10,'Cleaned Data'!I:I)
- tennis: =SUMIF('Cleaned Data'!F:F, 'Popular Category'!A11,'Cleaned Data'!I:I)
- travel: =SUMIF('Cleaned Data'!F:F, 'Popular Category'!A12,'Cleaned Data'!I:I)
- fitness: =SUMIF('Cleaned Data'!F:F, 'Popular Category'!A13,'Cleaned Data'!I:I)
- education: =SUMIF('Cleaned Data'!F:F, 'Popular Category'!A14,'Cleaned Data'!I:I)
- veganism: =SUMIF('Cleaned Data'!F:F, 'Popular Category'!A15,'Cleaned Data'!I:I)
- Animals: =SUMIF('Cleaned Data'!F:F, 'Popular Category'!A16,'Cleaned Data'!I:I)
- culture: =SUMIF('Cleaned Data'!F:F, 'Popular Category'!A17,'Cleaned Data'!I:I)

Second: Click on the filter beside Scores and Sort Z-A to get the top 5 category.

## Task 3: Data Visualization & Storytelling

####  What To Do?
- Choose the data visualizations that best support the story you want to tell to the client
- Create a PowerPoint presentation that reports on the client’s content performance

How many unique categories are there?
How many reactions are there to the most popular category?
What was the month with the most posts?

####  Report: Tool Used (POWERBI)
![buzz1](https://github.com/user-attachments/assets/9fe87b12-5f9a-4f91-8386-72fce629f38e)

![buzz2](https://github.com/user-attachments/assets/5c046979-efe6-4e61-bad5-597f86a5026c)

####  Insights
- There are a total of 25,000 posts.
- There are 16 unique categories, 4 content types, and 16 reaction types.
- January has the highest number of posts, followed by July, August, October, while April has the least posts.
- The total reactions for the five most popular categories are Animals, Science, Healthy Eating, Technology, and Food.
- There are 4 content types: Photo, Video, GIF, and Audio, with distribution rates of 26.8%, 25.4%, 24.7%, and 23.0%, respectively.
- The most popular reactions out of the 16 available reactions are "Super Love," "Adore," "Want," "Cherish," and "Love."
- Sunday is the day with the most posts, followed by Friday, Monday, Wednesday, Thursday, Tuesday, and Saturday, which has the least.

####  Recommendations
- Focus on Popular Categories: Prioritize content in Animals, Science, Healthy Eating, Technology, and Food to maximize engagement.
- Leverage Content Types: Create more photos and videos (26.8% and 25.4% engagement) while experimenting with GIFs and audio for variety.
- Boost Engagement with Reactions: Craft emotionally appealing posts to encourage reactions like "Super Love," "Adore," and "Love."
- Optimize Posting Times: Post more on Sundays and Fridays, and consider running campaigns in April to boost engagement.
- Run Seasonal Campaigns: Take advantage of high engagement in January and explore tech trends for technology-focused posts.

## Task 4: Present to the Client 
Tool Used (Tiktok & Google Slide)


