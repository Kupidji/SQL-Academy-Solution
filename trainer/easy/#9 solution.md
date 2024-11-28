### \#9
> [!NOTE]
> Какие компании организуют перелеты из Владивостока (Vladivostok)?
[Задание](https://sql-academy.org/ru/trainer/tasks/9)
```sql
SELECT name FROM Company
JOIN Trip ON company = Company.id
WHERE town_from = 'Vladivostok';
```