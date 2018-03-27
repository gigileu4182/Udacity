%% In memory
%% Durable storage

1. Database is persistent, it gives the data structures for storing and search our data. fast
2. allow multiple users to use at the same time, which is not possible with flat files.
3. relational database allows for querying and summarizing data. we can also do comparisons and set up constraints.
----------------

* type / meaning.. column is of the same "type" and "meaning"
  * meaning. geogia could be the font, the place, a pr's name etc.
  * type: string, integers..
 
###### sql over python
doing sorting and indexing are faster in sql

###### some queries
- limit... offset
- order by
- group by

###### tricks for join.
1. from ... join..., on ...==...
  - where ... == ...
2. notice that the columns I used for joining do not need to appear as the query result.
3. "group by" can not be followed by "where"
  - and be careful, "where" happens before "group by" / "count(`*`) as sum" ( I guess for the same reason as 
  why `group by` can not be followed by `where`)
  - :+1:.. the solution is to put having num = 1, which happens after "group by"!

###### problem set 2..
- 我忽然发现，真正SQL里面的问题都是一对多的。很少跟像计量里截面是一对一的？不可能。时间 is also involved.
- :+1:心得：**the order, given..!!! feedback, output, diligence!!!!**
- 

#### SQL lesson 3.
- normaliztion (works better with join and comparisons..)
  - rule 1: one thing with several rows.
  - rule 2. key is the identifier, the others describe the key.
  - rule 3. if not about the **key**, put the attribute the the other table!
  - rule 4. do not put things together so that it seems there is a
  relationship between them!
  
- declaration of relationships
  - references ..(another table) to maintain data integrity.
  
- foreign keys.
  - important!!!! reference to another table!
  
- self joins: why? join a table to itself..
  - allows us to find the attributes in common.
  - avoid the relationship between self and self!!!
  
- important!!! using DB-API
  - import lib 
  %% connect: lib.connect() 
  %% Cursor: lib.connect().cursor
  %% using cursor.execute() to run the query and fetch the results.
  %% remember to close !!!!!
  - be careful, when using select, you have to commit() or rollback()!!!
  - subqueries.select average() from (select ... from ...) as A;
  
  
