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
