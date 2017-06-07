Create a Database Go to http://localhost/phpmyadmin/ Click the “New” link on the upper left corner (under recent tables) Fill out the “Database Name” field with “my_first_database“. Click the “Create” button

Create a Table Click “my_first_database” on the left side of the screen On the “Create Table” section, fill out the Name with “products” and Number of Columns with “6“ Click “Go” button

Fill out the fields with id, name, etc. Click the “Save” button

Insert Data Click the “products” table. Click the “Insert” tab.

Fill out the form. Click the “Go” button.

Great job! We now have a database, a table inside the database and a record inside the table.

Creating a table using SQL commands

CREATE TABLE animals ( id MEDIUMINT NOT NULL AUTO_INCREMENT, name CHAR(30) NOT NULL, PRIMARY KEY (id) );

INSERT INTO animals (name) VALUES ('dog'),('cat'),('penguin'), ('lax'),('whale'),('ostrich');

SELECT * FROM animals;
