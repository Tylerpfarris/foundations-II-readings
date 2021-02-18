# READ 09

## Database Normalization

- A process used to organize a database into tables and columns. the main idea with this is that a table should be about a specific topic and oly support topics included. 

- 3 main reasons for database normalization:
  - minimize duplicate data
  - minimize or avoid data modification issues
  - simplify queries

- modification anomalies
  - Insert anomaly
  - Update anomaly
  - Deletion anomaly

- make data more accessible by putting it in tables serving a single purpose

- 3 common forms of database normalization:
  - First Normal Form - The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.
  - Second Normal Form - The table is in first normal form and all the columns depend on the table’s primary key.
  - Third Normal Form - the table is in second normal form and all of its columns are not transitively dependent on the primary key.

  - The forms are progressive. 


## SQL BOLT

- the tutorial went over  JOINS in particular INNER JOIN and OUTER JOINS
