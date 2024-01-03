# SQL 
A repo containing common SQL queries

**Table of Contents**
- [Filter Data](Notebooks/01%20Filter%20Data.ipynb)
- [Extractt Data](Notebooks/02%20Extract%20Data.ipynb)
- [Combine Data](Notebooks/03%20Combine%20Data.ipynb)
- [Subqueries](Notebooks/04%20Subqueries.ipynb)
- Window Functions

```
pip install ipython-sql
```

## SQL Order of Execution
SQL code is not processed in the order that it is written, the actual order of execution of the operations is:
<!-- |Operation |Description |
|--|--|
| `FROM` 		|first SQL will access the table from which data should be grabbed|
| `JOIN` 		|then SQL will access other tables that are joined with the initial table|
| `WHERE` 		|then SQL will apply a filter on the data in the (joined) table|
| `GROUP BY` 	|next SQL will group the data in the (joined) table if applicable|
| `HAVING` 	|then SQL will apply a filter on the grouped data in the (joined) table|
| [...]		|Window Functions|
| `SELECT` 	|then SQL will look at which columns from the table the user has requested|
| `DISTINCT`	 |the select operation will return a column, from which the unique values can be extracted|
| `UNION`		|then SQL can combine the resulting columns with other tables using set operations|
| `ORDER BY` 	|then SQL will sort the values in the resulting table|
| `OFFSET`		|then SQL will ignore a set of values in the resulting table|
| `LIMIT / TOP` 	|finally SQL will output part of the table| -->

- `FROM` 		first SQL will access the table from which data should be grabbed
- `JOIN` 		then SQL will access other tables that are joined with the initial table
- `WHERE` 		then SQL will apply a filter on the data in the (joined) table
- `GROUP BY` 	next SQL will group the data in the (joined) table if applicable
- `HAVING` 	then SQL will apply a filter on the grouped data in the (joined) table
- [...]		Window Functions
- `SELECT` 	then SQL will look at which columns from the table the user has requested
- `DISTINCT`	 the select operation will return a column, from which the unique values can be extracted
- `UNION`		then SQL can combine the resulting columns with other tables using set operations
- `ORDER BY` 	then SQL will sort the values in the resulting table
- `OFFSET`		then SQL will ignore a set of values in the resulting table
- `LIMIT / TOP` 	finally SQL will output part of the table

