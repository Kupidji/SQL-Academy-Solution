### 1. Удаление всех записей
> [!NOTE]
> Удалите все записи из таблицы Payments, используя оператор DELETE.
```sql
DELETE FROM Payments;
```

### 2. Удаление c условием
> [!NOTE]
> Удалить запись из таблицы Goods, у которой поле good_name равно "milk"
```sql
DELETE FROM Goods
WHERE good_name = 'milk';
```

### 3. Удаление c JOIN
> [!NOTE]
> Измените запрос так, чтобы удалить товары (Goods), имеющие тип деликатесов (delicacies).
```sql
DELETE Goods FROM Goods 
JOIN GoodTypes ON Goods.type = GoodTypes.good_type_id 
WHERE GoodTypes.good_type_name = 'delicacies';
```