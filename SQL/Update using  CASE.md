  
To change the values of the `id` column from 4 to 3 and from 5 to 4, you can use the `UPDATE` statement with a `CASE` expression. Here's how you can do it:

```sql
UPDATE your_table_name
SET id = CASE 
           WHEN id = 4 THEN 3
           WHEN id = 5 THEN 4
           ELSE id
         END
WHERE id IN (4, 5);

```

