### Module 12 Challenge (noSQL Challenge)

## Instructions
The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

**Parts 1: Database and Jupyter Notebook Set Up**
Imported the establishments.json file in Terminal with the following command: 
mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json

* Created an instance of Mongo Client.
    * Confirmed the created database and data were loaded properly:
    * Listed the collection(s)
    * Found and displayed one document in the establishments collection using find_one and displayed with pprint
* Assign the establishments collection to a variable to prepare the collection for use.

**Parts 2: Update the Database**
Using `NoSQL_setup.ipynb` to import the .json file and make updates to the database. 
* Insert the new halal restaurant (Penang Flavours) which opened in Greenwich into the database.
* Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields
* Update the new restaurant with the BusinessTypeID you found.
* Dropped all establishments located in Dover from the database due to lack of interest (using delete_many).
* Used update_many to convert the latitude and longitude values from string to decimal numbers.

**Part 3: Exploratory Analysis**
Used `NoSQL_analysis.ipynb` to query relevant information for analyses and converted results into Pandas DataFrame.  

## Delivered Results For:
1. Which establishments have a hygiene score equal to 20?
   
   There were 41 establishments with a hygiene score of 20.
   
2. Which establishments in London have a RatingValue greater than or equal to 4?

    There were 34 establishments in London with a RatingValue greater than or equal to 4.

3. What are the top 5 establishments with a RatingValue rating value of '5', sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

   The top 5 establishments with a RatingValue of '5' sorted by lowest hygiene score nearest to "Penang Flavours" are: "Volunteer", "Plumstead Manor Nursery", "Atlantic Fish Bar", "Iceland", and "Howe and Co Fish and Chips - Van 17". 
   
4. How many establishments in each Local Authority area have a hygiene score of 0?
   
   There are 55 rows in returned, the first 10 rows returned were: 
    | _id | count |
    |-----|-------|
    |Thanet|1130|
    |Greenwich|882|
    |Maidstone|713|
    |Newham|711|
    |Swale|686|
    |Chelmsford|680|
    |Medway|672|
    |Bexley|607|
    |Southend-On-Sea|586|
    |Tendring|542|