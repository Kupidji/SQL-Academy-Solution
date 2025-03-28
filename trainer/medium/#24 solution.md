### \#24
> [!NOTE]
> Определить кто и сколько потратил в июне 2005
[Задание](https://sql-academy.org/ru/trainer/tasks/24)
```sql
SELECT
    member_name,
    SUM(amount * unit_price) as costs
FROM FamilyMembers
         JOIN Payments ON member_id = family_member
WHERE MONTH(date) = 6 AND YEAR(date) = 2005
GROUP BY member_name;
```

