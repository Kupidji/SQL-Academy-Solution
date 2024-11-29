### \#13
> [!NOTE]
> Вывести имена людей, у которых есть полный тёзка среди пассажиров
[Задание](https://sql-academy.org/ru/trainer/tasks/13)
```sql
SELECT name FROM Passenger
GROUP BY name
HAVING COUNT(*) > 1
```