### 1. Ограничение записей с начала таблицы
> [!NOTE]
> Отсортируйте список компаний (таблица Company) по их названию в алфавитном порядке и выведите первые две записи.
```sql
SELECT * FROM Company
ORDER BY name
LIMIT 2;
```

### 2. Ограничение количества записей со смещением
> [!NOTE]
> Выведите начало (поле start_pair) и окончание (поле end_pair) второго и третьего занятия из таблицы Timepair.
```sql
SELECT start_pair, end_pair FROM Timepair
ORDER BY start_pair, end_pair
LIMIT 2 OFFSET 1;
```