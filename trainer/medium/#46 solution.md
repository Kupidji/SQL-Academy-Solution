### \#46
> [!NOTE]
> В каких классах введет занятия преподаватель "Krauze" ?
[Задание](https://sql-academy.org/ru/trainer/tasks/46)
```sql
SELECT name FROM Class
JOIN Schedule ON class = Class.id
JOIN Teacher ON Teacher.id = teacher
WHERE Teacher.last_name = 'Krauze'
GROUP BY name;
```