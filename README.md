# nosql-challenge

# Overview

As a contractor of the food maganize, Eat, Safe, Love, we will evaluate some ratings data in order to help journalist and food critics determine where to focus future articles. The ratings data was obtained from the UK Food Standards Agency, that gives establishments food hygiene ratings. 

Purpose: To gain a better understanding of MongoDB and PyMongo utiziling data on food ratings. The project is divided into three parts: Database and Jupyter Notebook Set Up, Update the Database, and Exploratory Analysis.

# Resources
[Establishments](Resources/establishments.json)

Programs used: MongosDB, Python, Jupyter Notebook, Py Mongo

# Part 1: Database and Jupyter Notebook Set Up
File used: [Database and Jupyter Notebook Set Up](NoSQL_setup_starter.ipynb)

In this part, the focus is on setting up the database and Jupyter Notebook environment. 

-First ensure that you are in the correct path where the 'establishments.json' file is located then import establishments.json using the mongoimport command:

 
    mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json
    
Then the following was completed for set up:

-Creating a database named "uk_food" and a collection named "establishments".
-Importing PyMongo and Pretty Print libraries.
-Creating an instance of the Mongo Client and listing the databases.
-Listing the collection(s) in the "uk_food" database.
-Using find_one() and pprint to display one document from the establishments collection.


# Part 2: Update the Database
File used: [Database and Jupyter Notebook Set Up](NoSQL_setup_starter.ipynb)

In this part, the database is updated with new data and modifications. The following were completed: 

-Inserting the supplied data for the "Penang Flavours" restaurant into the establishments collection.
-Performing a query to find the BusinessTypeID for "Restaurant/Cafe/Canteen" and returning the BusinessTypeID and BusinessType fields.
-Updating the "Penang Flavours" document with the correct value for BusinessTypeID.
-Performing a query to delete all documents in the collection where "Dover Local Authority" is the value for LocalAuthorityName.
-Performing a count_documents() check before and after the removal of the Dover documents.
-Using update_many() to convert the latitude and longitude fields from strings to decimal numbers and RatingValue to integers

# Part 3: Exploratory Analysis
File used: [Analysis](NoSQL_analysis_starter.ipynb)

In this part, exploratory analysis wa performed on the database. The following was analyzed: 

-Answering Question 1: Finding establishments with a hygiene score equal to 20.
-Answering Question 2: Finding establishments in London with a RatingValue greater than or equal to 4.
-Answering Question 3: Finding the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant "Penang Flavours".
-Answering Question 4: Finding the number of establishments in each Local Authority area with a hygiene score of 0, sorting the results from highest to lowest, and printing the top ten local authority areas.
