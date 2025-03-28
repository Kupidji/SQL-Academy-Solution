### \#19
> [!NOTE]
> Определить, кто из членов семьи покупал картошку (potato)
[Задание](https://sql-academy.org/ru/trainer/tasks/19)
```sql
SELECT status FROM FamilyMembers FM
JOIN Payments P ON FM.member_id = P.family_member
JOIN Goods G ON P.good = G.good_id
WHERE g.good_name = 'potato'
GROUP BY status
```