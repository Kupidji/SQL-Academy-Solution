### \#10
> [!NOTE]
> Вывести вылеты, совершенные с 10 ч. по 14 ч. 1 января 1900 г.
[Задание](https://sql-academy.org/ru/trainer/tasks/10)
```sql
SELECT * FROM Trip
WHERE TIME(time_out) BETWEEN '10:00:00' AND '14:00:00'
AND DATE(time_out) = "1900-01-1"
```