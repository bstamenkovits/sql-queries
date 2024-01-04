# SQL Queries
A repo containing common SQL queries.

**Table of Contents**
- [Filter Data](Notebooks/01%20Filter%20Data.ipynb)
- [Extractt Data](Notebooks/02%20Extract%20Data.ipynb)
- [Combine Data](Notebooks/03%20Combine%20Data.ipynb)
- [Subqueries](Notebooks/04%20Subqueries.ipynb)
- [Window Functions](Notebooks/05%20Window%20Functions.ipynb)

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


## Tech Stack
This repo mainly consists of IPythong Notebooks which run SQL querries from sqlite database files (.db files). MacOS comes with sqlite pre-installed, on windows you will need to download and install it manually. Any flavor SQL can be used, but most require a dedicated server to be run. SQLite databases can be run straight from .db files. 



### Ipython Notebook Setup
I am using VS Code and the [Jupyter Notebook](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter) extension automatically configure the ipython kernel. 

In addition the ipython sql package needs to be installed.

```
pip install ipython-sql
```

All the relevant packages can be found in [requirements.txt](requirements.txt)


### SQLite Installation
- [Download](https://www.sqlite.org/download.html) the files for the windows operation system
- Extract the zip files to a relevant folder (e.g. `C:\Program Files\sqlite`)
- Add the path to said folder to your system path 
- If you are using VS Code you may need to also update the PATH in the integrated terminal of VS Code `$env:Path = "$env:Path;C:\Program Files\sqlite"`

#### Import CSV Files to SQLite Database File
In order to simplify adding multiple csv files as tables to a database file (.db file) I have created a notebook file which does this automatically given the proper folder structure of the csv files. For more information see [csv_to_db.ipynb](Notebooks/databases/csv_to_db.ipynb)
