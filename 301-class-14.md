![](https://www.edureka.co/blog/wp-content/uploads/2019/10/Normalization-in-SQL.jpg)

# Introduction to Database Normalization

Database normalization is a database schema design technique, by which an existing schema is modified to minimize redundancy and dependency of data.

Normalization split a large table into smaller tables and define relationships between them to increases the clarity in organizing data.

## Some Facts About Database Normalization

1. The words normalization and normal form refer to the structure of a database.
2. Normalization was developed by IBM researcher E.F. Codd In the 1970s.
3. Normalization increases clarity in organizing data in Databases.

Normalization of a Database is achieved by following a set of rules called 'forms' in creating the database.

![](https://i.ytimg.com/vi/mUtAPbb1ECM/maxresdefault.jpg)

### First Normal Form (1NF)
Each column is unique in 1NF.

![](https://1.bp.blogspot.com/-82XMENexHmc/VjY6LH0mbhI/AAAAAAAAANs/YqaDIbImszY/s1600/1NF.gif)

### Second Normal Form (2NF)
The entity should be considered already in 1NF, and all attributes within the entity should depend solely on the unique identifier of the entity.

![](https://www.essentialsql.com/wp-content/uploads/2014/06/SecondNormalFormSampleData3.png)


### Third Normal Form (3NF)

The entity should be considered already in 2NF, and no column entry should be dependent on any other entry (value) other than the key for the table.

If such an entity exists, move it outside into a new table.

3NF is achieved, considered as the database is normalized.


### Fourth Normal Form (4NF)
Tables cannot have multi-valued dependencies on a Primary Key.


### wFifth Normal Form (5NF)
A composite key shouldn't have any cyclic dependencies.

Well, this is a highly simplified explanation for Database Normalization. One can study this process extensively, though. After working with databases for some time, you'll automatically create Normalized databases, as it's logical and practical.

