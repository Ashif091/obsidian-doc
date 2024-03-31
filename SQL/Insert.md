
# VALUES
For example, if you have a table named "users" with columns `id`, `name`, and `email`, and you want to insert a new row into this table:
```sql
INSERT INTO users (name, email) VALUES ('John Doe', 'john@example.com');
```
# SELECT - FROM
**Copy the data from the source column to the new column in the target table:**

You can use an `INSERT INTO ... SELECT` statement to copy the data from the source column to the new column in the target table. For example:
```SQL
INSERT INTO target_table (column_name)
SELECT column_name FROM source_table;
```

