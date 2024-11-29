### \#11
> [!NOTE]
> Выведите пассажиров с самым длинным ФИО. Пробелы, дефисы и точки считаются частью имени.
[Задание](https://sql-academy.org/ru/trainer/tasks/11)
```sql
SELECT name FROM Passenger
WHERE LENGTH(name) = (SELECT MAX(LENGTH(name)) FROM Passenger)
```