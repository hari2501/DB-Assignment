1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.
   The "Product" table has a column named category_id, which serves as a foreign key referencing the id column in the "Product_category" table.
   This indicates that each product belongs to a specific category defined in the "Product_category" table.
   The relationship between them is established through the foreign key category_id in the "Product" table, referencing the primary key id in the "Product_category" table.
   One Product Belongs to One Category: Each product belongs to one specific category. This is a one-to-many relationship where one category can have multiple products but each product belongs to only one category.
   One Category Can Have Many Products: This implies that each category can encompass multiple products.
   The relationship between the "Product" and "Product_Category" tables is a one-to-many relationship, where:
   Each record (or product) in the "Product" table corresponds to one category in the "Product_Category" table.
   However, each category in the "Product_Category" table can be associated with multiple records (or products) in the "Product" table.

2. How could you ensure that each product in the "Product" table has a valid category assigned to it?
   In the "Product" table, the category_id column is a foreign key referencing the id column in the "Product_category" table. By defining a foreign key constraint,
   you enforce referential integrity,ensuring that every value in the category_id column of the "Product" table corresponds to a valid id in the "Product_category" table.
   Syntax:
    ALTER TABLE Product
    ADD CONSTRAINT 
    FOREIGN KEY (category_id)
    REFERENCES Product_category(id);
