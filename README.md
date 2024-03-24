# nosql-challenge

# Eat Safe, Love - Analysis of UK Food Ratings

Summary: 
The analysis for "Eat Safe, Love," a food magazine, focused on checking hygiene ratings given by the UK Food Standards Agency. This explains how the database was set up, imported, and exploratory analysis was done using a Jupyter Notebook.

Section 1: Database and Jupyter Notebook Setup

Database Creation and Data Import:
Data from establishments.json was imported into a MongoDB database named "uk_food" and a collection named "establishments", by using terminal commandline with the following:
">mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json"

Library Import and MongoDB Connection:
Necessary libraries such as PyMongo for MongoDB interaction and Pretty Print (pprint) for data display were imported. A Mongo Client instance was created to establish the connection.

Database Confirmation:
The existence of the "uk_food" database was verified by listing databases in MongoDB. Additionally, the presence of the "establishments" collection within the database was confirmed. A document from the "establishments" collection was displayed using the find_one method and pprint. The "establishments" collection was assigned to a variable for further use.


Section 2: Database Update

Modifications to the Database:
Information for a new halal restaurant, "Penang Flavours" located in Greenwich was added. The BusinessTypeID for "Restaurant/Cafe/Canteen" was identified and updated for the new restaurant accordingly. Establishments within the Dover Local Authority were removed.

Data Type Conversion:
The update_many method was employed to convert latitude and longitude to decimal numbers. Similarly, update_many was used to convert RatingValue to integer numbers.

Section 3: Exploratory Analysis

Exploratory Analysis to Address Specific Questions from "Eat Safe, Love":
Establishments with a Hygiene Score of 20:
Displayed establishments with a hygiene score of 20, providing count, the first document, and a Pandas DataFrame.

High-Rated Establishments in London:
Highlighted establishments in London with a RatingValue greater than or equal to 4, presenting count, the first document, and a Pandas DataFrame.





