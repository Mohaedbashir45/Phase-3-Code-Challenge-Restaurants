#### **Phase 3 Code Challenge: Restaurants**

For this assignment, we'll be working with a restaurant review domain. We have three models: `Restaurant`, `Review`, and `Customer`.

For our purposes, a `Restaurant` has many `Review`s, a `Customer` has many `Review`s, and a `Review` belongs to a `Restaurant` and to a `Customer`.`Restaurant` - `Customer` is a many-to-many relationship.

****Note****: You should draw your domain on paper or on a whiteboard _before you start coding_. Remember to identify a single source of truth for your data.

#### **Topics**

- Table Relationships  
  
- Class and Instance Methods  
  
- Database Querying  
  
- SQLite3  and the Cursor Object. 

#### **Instructions**

Build out all of the methods listed in the deliverables.

The methods are listed in a suggested order, but feel free to tackle the ones you think are easiest. Be careful: some of the later methods rely on earlier ones.

**_**Remember!**_** _This code challenge does not have tests. You cannot run `pytest`._

You'll need to create your own sample instances so that you can try out your code on your own. Make sure your relationships and methods work in the console before submitting.

You are also encouraged to use a `main.py` file to create sample data to test your models and relationships.

Writing error-free code is more important than completing all of the deliverables listed - prioritize writing methods that work over writing more methods that don't work. You should test your code in the console as you write.

Similarly, messy code that works is better than clean code that doesn't. First, prioritize getting things working. Then, if there is time at the end, refactor your code to adhere to best practices.

****Before you submit!**** Save and run your code to verify that it works as you expect. If you have any methods that are not working yet, feel free to leave comments describing your progress.

#### **What You Need to Have**

You need to have test data and models for the initial `Restaurant` and `Customer` models, and an SQL table with data for some `Restaurant`s and `Customer`s.

The schema currently looks like this:

#### **restaurants table**

Column

Type

name

String

price

Integer

#### **customers Table**

Column

Type

first_name

String

last_name

String

You will need to create the SQL query for the `reviews` table(model) using the attributes specified in the deliverables below.

#### **Deliverables**

Write the following methods in the classes. Feel free to build out any helper methods if needed.

#### **Database.**

Before working on the rest of the deliverables, you will need to create all tables.

- A `**Review**` belongs to a `**Restaurant**`, and a `**Review**` also belongs to a `**Customer**`. In your script, create any columns your `**reviews**` table will

need to establish these relationships.

-   The `**reviews**` table should also have: - A `**star_rating**` column that stores an integer.

After creating the `**reviews**` table , use the `main**.py**` file to create instances of all your classes so you can test your code.

****Once you've set up your tables****, work on building out the following deliverables.

#### **Object Relationship Methods**

Use cursor query methods where appropriate.

#### **Review**

- **`Review customer()`**

- should return the `Customer` instance for this review

- `**Review restaurant()`**

- should return the `Restaurant` instance for this review

#### **Restaurant**

- `**Restaurant reviews()`**

- returns a collection of all the reviews for the `Restaurant`

- **`Restaurant customers()`**

- returns a collection of all the customers who reviewed the `Restaurant`

#### **Customer**

- `**Customer reviews()`**

- should return a collection of all the reviews that the `Customer` has left

- `**Customer restaurants()`**

- should return a collection of all the restaurants that the `Customer` has

reviewed

Check that these methods work before proceeding.

#### **Aggregate and Relationship Methods**

#### **Customer**

- **`Customer full_name()`**

- returns the full name of the customer, with the first name and the last name concatenated, Western style.

- **`Customer favorite_restaurant()`**

- returns the restaurant instance that has the highest star rating from this customer

- **`Customer add_review(restaurant, rating)`**

- takes a `restaurant` (an instance of the `Restaurant` class) and a rating

- creates a new review for the restaurant with the given `restaurant_id`

- **`Customer delete_reviews(restaurant)`**

- takes a `restaurant` (an instance of the `Restaurant` class) and

- removes ****all**** their reviews for this restaurant

- you will have to delete rows from the `reviews` table to get this to work!

#### **Review**

- **`Review full_review()`**

- should return a string formatted as follows:  
_Review for {insert restaurant name} by {insert customer's full name}: {insert review star_rating} stars._

#### **Restaurant**

- `**Restaurant fanciest()**, this method should be a class method`  
  
- returns __one__ restaurant instance for the restaurant that has the highest price  
  
- **`Restaurant all_reviews()`**- should return a list of strings with all the reviews for this restaurant  
  
formatted as follows:  
  
**[****"Review for {insert restaurant name} by {insert customer's full name}: {insert review star_rating} stars.",****"Review for {insert restaurant name} by {insert customer's full name}: {insert review star_rating} stars.",****]**

Once you're done, submit your **private** repo and add your TM as a collaborator for grading. Happy Coding!

## Rubric

Week 3 Code Challenge (1)

Week 3 Code Challenge (1)

Criteria

Ratings

Pts

This criterion is linked to a Learning OutcomeFolder Structure

4  pts

No Description

All files and necessary files included.

3  pts

No Description

Most files included, important files missing

2  pts

HTTP Methods

Several important files missing.

1  pts

No Description

Incomplete Folder Structure

0  pts

No Description

4  pts  

This criterion is linked to a Learning OutcomeAggregate and Relationship Methods

4  pts

Full Marks

All required methods (Customer.full_name(), Customer.favorite_restaurant(), Customer.add_review(), Customer.delete_reviews(), Review.full_review(), Restaurant.fanciest(), Restaurant.all_reviews()) are correctly implemented and return the expected results.

2  pts

No Description

Some methods are implemented but may not return the correct results in all cases.

1  pts

No Description

Most or all methods are missing or do not function as intended.

0  pts

No Marks

No implementation

4  pts  

This criterion is linked to a Learning OutcomeObject Relationship Methods

3  pts

Full Marks

All object relationship methods return accurate and relevant results.

2  pts

No Description

Most object relationship methods return accurate and relevant results.

1  pts

Partial

Object relationship methods have major issues.

0  pts

No Marks

All object relationship methods are missing or incorrect.

3  pts  

This criterion is linked to a Learning OutcomeDatabase Setup and Schema Design

4  pts

Full Marks

SQL tables (restaurants, customers, reviews) are correctly created with appropriate columns to establish relationships between Restaurant, Customer, and Review models.

2  pts

No Description

SQL tables are created, but some columns or relationships are missing or incorrectly defined.

1  pts

No Description

Most SQL tables are not created or are severely lacking in necessary columns and relationships.

0  pts

No Marks

No implementation

4  pts  

Total Points:  15

[Previous](https://moringa.instructure.com/courses/614/modules/items/92013)[Next](https://moringa.instructure.com/courses/614/modules/items/96987)
