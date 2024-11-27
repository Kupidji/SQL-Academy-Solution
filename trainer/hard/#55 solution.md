### \#55
> [!NOTE]
> Удалить компании, совершившие наименьшее количество рейсов.
[Задание](<link>)
```sql
WITH temp AS (
    SELECT company, COUNT(*) as trip_count FROM Trip
    GROUP BY company
),
min_company AS (
    SELECT company
    FROM temp
    WHERE trip_count = (SELECT MIN(trip_count) FROM temp)
)

DELETE FROM Company
WHERE id IN (
    SELECT * FROM min_company
);

SELECT * FROM Company
```
