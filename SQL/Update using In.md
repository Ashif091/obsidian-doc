![[Pasted image 20240316173113.png||400]]
  
To increase the salary by 100 for employees named "luffy" and "zoro", you can use the `UPDATE` statement with a `WHERE` clause to specify the condition. Here's how you can do it:

```sql
UPDATE your_table_name
SET salary = salary + 100
WHERE employee_name IN ('luffy', 'zoro');
```

