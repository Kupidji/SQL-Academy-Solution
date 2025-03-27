### 1. Ранг жилья в текущей категории по цене
> [!NOTE]
> Из таблицы Rooms вывести id, home_type и price у всех жилых помещений, а также в отдельной колонке room_rank вывести ранг данного жилого помещения в его категории (home_type) по цене, используя для этого функцию DENSE_RANK так, чтобы самое дешёвое жилое помещение имело ранг 1, следующие за ним по цене — 2 и так далее.
```sql
SELECT
    id,
    home_type,
    price,
    DENSE_RANK() OVER(PARTITION BY home_type ORDER BY price) as room_rank
FROM Rooms;
```

### 2. Время, прошедшее с предыдущего вылета
> [!NOTE]
> Дополните запрос так, чтобы найти разницу во времени между вылетами среди рейсов одной компании.
В качестве результирующей выборки выведите идентификаторы компаний (в поле company), время вылета их рейсов (в поле time_out) и время (в поле time_diff), прошедшее с предыдущего вылета в формате ЧЧ-MM-СС. Если это был первый рейс компании, то в поле time_diff нужно вывести "00:00:00".
```sql
SELECT
    company,
    time_out,
    TIMEDIFF(
            time_out,
            FIRST_VALUE(time_out) OVER (
            PARTITION BY company 
            ORDER BY time_out
            ROWS BETWEEN 1 PRECEDING AND CURRENT ROW
        )
    ) AS time_diff
FROM Trip
```
