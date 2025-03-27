### 1. Минимальная стоимость жилья в текущей категории
> [!NOTE]
> Из таблицы Rooms вывести поля home_type и price, а также добавить колонку min_price_by_type, в которой необходимо вывести минимальную стоимость жилья для текущего типа жилья (home_type). Для вычисления минимальной стоимости нужно использовать оконную функцию MIN.
```sql
SELECT
    home_type, price,
    MIN(price) OVER (PARTITION BY home_type) as min_price_by_type
FROM Rooms;
```

