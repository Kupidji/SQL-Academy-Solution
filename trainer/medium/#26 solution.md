### \#26
> [!NOTE]
> Определить группы товаров, которые не приобретались в 2005 году
[Задание](https://sql-academy.org/ru/trainer/tasks/26)
```sql
SELECT good_type_name
FROM GoodTypes
WHERE good_type_id NOT IN (
    SELECT type
    FROM Goods
             JOIN Payments ON good_id = good
    WHERE YEAR(date) = 2005
    )
```

