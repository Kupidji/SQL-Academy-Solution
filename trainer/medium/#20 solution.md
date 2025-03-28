### \#20
> [!NOTE]
> Сколько и кто из семьи потратил на развлечения (entertainment). Вывести статус в семье, имя, сумму
[Задание](https://sql-academy.org/ru/trainer/tasks/20)
```sql
SELECT
    status,
    member_name,
    SUM (unit_price * amount) AS costs
FROM FamilyMembers FM
         JOIN Payments P ON FM.member_id = P.family_member
         JOIN Goods G ON P.good = G.good_id
         JOIN GoodTypes GT ON G.type = GT.good_type_id
WHERE GT.good_type_name = 'entertainment'
GROUP BY member_name, status;
```

