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
First: Add up the total scores for each category. To do this, open a new sheet, name it as Popular Category and fill column A with Category from Cleaned data and in column B1 write "Scores" then use the following formulars to get the scores. .
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




