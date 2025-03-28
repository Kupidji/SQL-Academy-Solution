### \#25
> [!NOTE]
> Определить, какие товары не покупались в 2005 году
[Задание](https://sql-academy.org/ru/trainer/tasks/25)
```sql
SELECT good_name
FROM Goods
WHERE good_id NOT IN (
    SELECT good
    FROM Payments
    WHERE YEAR(date) = 2005
)
```

