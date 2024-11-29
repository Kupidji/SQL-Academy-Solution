### \#14
> [!NOTE]
> В какие города летал Bruce Willis
[Задание](https://sql-academy.org/ru/trainer/tasks/14)
```sql
SELECT town_to FROM Trip
JOIN Pass_in_trip ON Pass_in_trip.trip = Trip.id
JOIN Passenger ON Passenger.id = Pass_in_trip.passenger
WHERE Passenger.name = 'Bruce Willis'
```