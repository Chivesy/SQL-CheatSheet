# SQL-CheatSheet  
SQL-lite CheatSheet using examples learned from CodeAcademy SQL course.  
SQL -- Structured Query Language

## Basic Vocab
Relational database -- database that organizes information into one or more tables.  
Table -- a collection of data organized into rows and columns.  
 
## Statement Commands  

| Command       | Purpose                                             | Example                                                                 |
| ------------- | -------------                                       | -----                                                                   |
| CREATE TABLE  | Statment to create a new table in database          | CREATE TABLE table_name ( column1 datatype, column2 datatype, ... );    |
| INSERT INTO   | Clause to add a new row to a table                  | INSERT INTO celebs (id, name, age)                                      |
| VALUES        | Clause that indicates the data being inserted       | VALUES (1, 'Justin Bieber', 22);                                        |
| SELECT        | Clause to query data from database                  | SELECT name FROM celebs;                                                |
| *             | Wild card symbol to select every item in column     | SELECT * FROM celebs;                                                   |
| ALTER TABLE   | Clause that modifys a columns in the table          | ALTER TABLE celebs ADD COLUMN twitter_handle TEXT;                      |
| UPDATE        | Clause that modifys a row in the table              | **UPDATE** celebs SET twitter_handle = '@taylorswift13' WHERE id = 4;   |
| SET           | Clause to indicate column or row to edit            | UPDATE celebs **SET** twitter_handle = '@taylorswift13' WHERE id = 4;   |
| WHERE         | Clause that indicates which row(s) to update        | UPDATE celebs SET twitter_handle = '@taylorswift13' **WHERE** id = 4;   |
| DELETE FROM   | Clause that lets you delete rows from a table       | DELETE FROM celebs WHERE twitter_handle IS NULL;                        | 
 
 
## Constraints  
CREATE TABLE celebs (  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   id INTEGER PRIMARY KEY,   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   name TEXT UNIQUE,  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   date_of_birth TEXT NOT NULL,  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   date_of_death TEXT DEFAULT 'Not Applicable'  
);  
   
| Constraints | Purpose |
| ----------- | ------- |
| PRIMARY KEY | PRIMARY KEY columns can be used to uniquely idetify the row. Prevents the ability to add another row with a identical value.       |
| UNIQUE      | UNIQUE columns have a different value for every row. Similar to PRIMARY KEY except a table can have many different UNIQUE columns. |
| NOT NULL    | NOT NULL columns must have a value. Attempts to insert a row without a value for NOT NULL will cause a constraint violation.       |
| DEFAULT     | DEFAULT columns take an additonal argument taht will be the assumed value for an inserted row if new row does not specify a value. |
    
                                                                                            
