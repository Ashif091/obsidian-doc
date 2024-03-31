![[Pasted image 20240317092556.png||400]]
# Remove one raw
  
To remove the row with `id` equal to 4 from the table, you can use the `DELETE` statement with a `WHERE` clause specifying the condition. Here's how you can do it:
```sql
DELETE FROM your_table_name WHERE id = 4;
```

# Remove one column 
For example, if you have a table named `employees` and you want to remove the column named `salary`, you would use:

```sql
ALTER TABLE employees DROP COLUMN salary;
```

