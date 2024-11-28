### \#6
> [!NOTE]
> Какие компании совершали перелеты на Boeing
[Задание](https://sql-academy.org/ru/trainer/tasks/6)
```sql
SELECT DISTINCT name FROM Company
JOIN Trip ON company = Company.id
WHERE plane = 'Boeing'
```