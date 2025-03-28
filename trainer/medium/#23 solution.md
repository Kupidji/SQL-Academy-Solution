### \#23
> [!NOTE]
> Найдите самый дорогой деликатес (delicacies) и выведите его цену
[Задание](https://sql-academy.org/ru/trainer/tasks/23)
```sql
SELECT good_name, unit_price
FROM Goods G
         JOIN Payments P ON G.good_id = P.good
         JOIN GoodTypes GT ON G.type = GT.good_type_id
WHERE GT.good_type_name = 'delicacies'
ORDER BY unit_price DESC
    LIMIT 1;
```

