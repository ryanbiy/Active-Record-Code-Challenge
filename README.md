# Active-Record-Code-Challenge
Product Review Code Challenge
# Introduction
This project focuses on implementing a product review system within an e-commerce domain. The project involves three models: User, Review, and Product. A User can review multiple Products, and each Review belongs to a User and a Product.

# Products Review Diagram

# Topics Covered
This assignment covers the following topics:


Active Record Migrations
Active Record Associations
Class and Instance Methods
Active Record Querying
# Instructions
Complete the implementation of the provided methods. Although the methods are listed in a suggested order, you can tackle them in any way you find suitable. Remember to create sample instances and test your code in the console before submission.

To test your code, you can use the provided tool by running rake console. This will open a pry session with your classes defined, allowing you to test your methods interactively. You can also use the seeds.rb file to create sample data for testing.

# Deliverables
# Migrations
Before working on the other deliverables, create a migration for the reviews table. The reviews table should have the following columns:

star_rating (integer)
comment (string)
Foreign keys to establish relationships with the User and Product tables.
After creating and running the migration, use the seeds.rb file to create Review instances for testing.

Object Association Methods
Implement the following methods using Active Record association macros and query methods:

# Review:

Review#user: Returns the User instance for this Review.
Review#product: Returns the Product instance for this Review.
Product:

Product#reviews: Returns a collection of all the Reviews for the Product.
Product#users: Returns a collection of all the Users who reviewed the Product.
# User:

User#reviews: Returns a collection of all the Reviews given by the User.
User#products: Returns a collection of all the Products reviewed by the User.
Test these methods using the rake console to ensure they work as expected.

Aggregate and Association Methods
Implement the following methods:

# Review:

Review#print_review: Puts a string formatted as follows: "Review for {product name} by {user name}: {review star_rating}. {review comment}."
# Product:

Product#leave_review(user, star_rating, comment): Creates a new Review in the database associated with this Product and the User. Takes a User instance, a star_rating (integer), and a comment (string) as arguments.
Product#print_all_reviews: Puts a string representing each review for this product. Each review should be formatted as follows: "Review for {product name} by {user name}: {review star_rating}. {review comment}."
Product#average_rating: Returns a float representing the average star rating for all reviews for this product.
# User:

User#favorite_product: Returns the product instance that has the highest star rating from this User.
User#remove_reviews(product): Removes all the User's reviews for a specific Product. This requires deleting the associated rows from
