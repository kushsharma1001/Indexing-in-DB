# Indexing-in-DB (DB Optimization and Fine Tuning)

https://dataschool.com/sql-optimization/how-indexing-works/

Testing the indexing advantages:
Add indexes to your table.
Run the query now:
EXPLAIN ANALYZE SELECT * FROM friends WHERE name = 'Blake';

If adding an index does not decrease query time, you can simply remove it from the database.

### To remove an index use the DROP INDEX {IndexName} command: DROP INDEX friends_name_asc; <br/>
### To create index: create index {name of the index} on {tableName} (Column1, Column2 ...) <br/>
Note that in multi column based index, order of columns matter. Hence, always try all permutations. <br/>

### After a certain period, always reindex your indexes: <br/>
### a) Reindex an index: reindex index {indexName <br/>
### b) Much better is to reindex entire table: reindex table {tableName}

### Add unique constraint in a column: alter table {tableName} add constraint {constraintName} unique (columnName);

 # Explain Options
  ![image](https://user-images.githubusercontent.com/22798697/116071456-8e2f1200-a6ab-11eb-8bef-1009f5495bd4.png)
