### \#8
> [!NOTE]
> В какие города можно улететь из Парижа (Paris) и сколько времени это займёт?
[Задание](https://sql-academy.org/ru/trainer/tasks/8)
```sql
SELECT town_to, (
    TIMEDIFF(time_in, time_out)
) flight_time FROM Trip
WHERE town_from = 'Paris'
```