# In a SQL table, what is the difference between information in a row and information in a column?

> The information in a row is one object, the information in a column is one property.

# Demonstrate the basic structure for creating a new table called characters with the values name, age, description as strings, and an int id.

>CREATE TABLE characters(
  id int NOT NULL,
  name VARCHAR(255) NOT NULL,
  age VARCHAR(255),
  description VARCHAR(255),
)

# What is the difference between the following statements: DELETE FROM table_name; DROP TABLE table_name;

>Delete from deletes a value from the table. Drop table removes the enitre table and all its values.

https://github.com/Derek-Wallace/glistServer (connected to database)