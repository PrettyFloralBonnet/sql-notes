## First queries
`SELECT * FROM table;` returns all columns in the table.  
`SELECT column FROM table;` selects a specific column.  
## Renaming columns
`SELECT column AS "Nicely Named Column" FROM table;` renames the column.
## Column concatenation
`SELECT CONCAT(column1, 'my text', column2) FROM table;` concatenates data from the columns whose names are passed to the CONCAT function, as well as any text (in single quotes) that is passed to it.

**NOTE**: The part about using single quotes with **text** is actually crucial. Single quotes are used to represent text in SQL. Double quotes are reserved for column and table names.

Renaming will still work here:

`SELECT CONCAT(column1, ' my text ', column2) AS "My Concatenated Column" FROM table;`

Note that when passing an argument to the `AS` keyword, double quotes are used. Double quotes are associated with column names.

## Functions in SQL

### Aggregate functions

Aggregate functions aggregate data, meaning they take all of the data in the table and produce a single output.

* `AVG()` - calculates the average of a set of values
* `COUNT()` - counts rows in a specified table or view
* `MIN()` - gets the minimum value from a set of values
* `MAX()` - gets the maximum value from a set of values
* `SUM()` - calculates the sum of values

### Scalar functions

Scalar (non-aggregate) functions perform operations on each individual row of data, and they produce multiple outputs.
