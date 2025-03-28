### \#21
> [!NOTE]
> Определить товары, которые покупали более 1 раза
[Задание](https://sql-academy.org/ru/trainer/tasks/21)
```sql
SELECT good_name
FROM Goods G
         JOIN Payments P on G.good_id = P.good
GROUP BY good_name
HAVING COUNT(*) > 1;
```
