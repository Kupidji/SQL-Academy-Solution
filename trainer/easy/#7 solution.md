### \#7
> [!NOTE]
> Вывести все названия самолётов, на которых можно улететь в Москву (Moscow)
[Задание](https://sql-academy.org/ru/trainer/tasks/7)
```sql
SELECT DISTINCT plane FROM Trip
WHERE town_to = 'Moscow'
```