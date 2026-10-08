# Online Food Delivery Management System (MongoDB)

## Overview

The Online Food Delivery Management System is a NoSQL database project that demonstrates how MongoDB can be used to store, manage, and analyze customer order data and feedback. This project showcases practical NoSQL operations, making it easy to add, search, update, delete, and sort customer records based on various demographics such as age, gender, occupation, family size, and delivery feedback.

## Project Details

* Database Name: foodDeliveryDB

* Collection Name: customers

* Dataset Focus: Customer demographics, purchasing behavior, and delivery feedback.

## Data Structure

Each document in the customers collection follows this JSON schema based on the dataset:

{
  "Age": 20,
  "Gender": "Female",
  "Marital Status": "Single",
  "Occupation": "Student",
  "Monthly Income": "No Income",
  "Educational Qualifications": "Post Graduate",
  "Family size": 4,
  "Customer Type": "Frequent",
  "Pin code": 560001,
  "Output": "Yes",
  "Feedback": "Positive"
}


## MongoDB Operations Implemented

This project covers a wide range of essential MongoDB queries and database management techniques:

### 1. Database & Collection Management:

* Creating and switching databases (use foodDeliveryDB)

* Creating collections (db.createCollection("customers"))

### 2. CRUD Operations:

* Create: Bulk insertion of records using insertMany().

* Read: Fetching records using the find() method.

* Update: Modifying customer feedback based on specific criteria using updateOne() and the $set operator.

* Delete: Removing records using deleteMany().

### 3. Advanced Querying & Filtering:

* Projection: Displaying only specific fields (e.g., fetching only Age, Gender, and Feedback).

* Exact Match: Filtering by attributes like "Occupation": "Student" or "Feedback": "Positive".

* Comparison Operators: Using $gt, $gte, and $lte to find customers within specific age brackets or family sizes.

* Multiple Conditions (AND): Finding records that match multiple criteria simultaneously (e.g., Female customers who gave Positive feedback).

* Logical Operators (OR): Using $or to fetch customers matching one condition or another (e.g., Graduates OR Post Graduates).

### 4. Sorting and Aggregation:

* Sorting: Organizing results by Age or Family size in Ascending (1) and Descending (-1) order using sort().

* Limiting Results: Fetching the "Top 5 Oldest Customers" by chaining .sort() and .limit(5).

* Counting: Using countDocuments() to get the total number of customers.

## How to Run This Project

1. Install MongoDB and MongoDB Compass (or use the Mongo Shell / mongosh).

2. Open your Mongo terminal or Compass mongosh interface.

3. Switch to the database by typing: use foodDeliveryDB

4. Create the collection: db.createCollection("customers")

5. Import your dataset (via Compass UI using "Import File" or by running the insertMany query provided in the queries list).

6. Execute the various find(), sort(), and updateOne() queries to explore the dataset.

## Conclusion

This project serves as a foundational guide to understanding core MongoDB concepts. It highlights the flexibility of NoSQL databases in handling real-world e-commerce datasets, analyzing customer behavior, and managing unstructured data efficiently.
