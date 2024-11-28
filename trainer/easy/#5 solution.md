### \#5
> [!NOTE]
> Вывести количество рейсов, совершенных на TU-134
[Задание](https://sql-academy.org/ru/trainer/tasks/5)
```sql
SELECT COUNT(plane) count FROM Trip
WHERE plane = 'TU-134'
```