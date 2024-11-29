### \#12
> [!NOTE]
> Выведите идентификаторы всех рейсов и количество пассажиров на них. Обратите внимание, что на каких-то рейсах пассажиров может не быть. В этом случае выведите число "0".
[Задание](https://sql-academy.org/ru/trainer/tasks/12)
```sql
SELECT Trip.id, COUNT(passenger) count FROM Trip
LEFT JOIN Pass_in_trip ON Trip.id = Pass_in_trip.trip
GROUP BY Trip.id;
```