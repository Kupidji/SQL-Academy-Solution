### 1. Добавление нового товара
> [!NOTE]
> Добавьте новый товар в таблицу Goods с именем «Table» и типом «equipment». В качестве первичного ключа (good_id) укажите количество записей в таблице + 1.
```sql
INSERT INTO Goods
SELECT MAX(good_id) + 1, 'Table', (
    SELECT good_type_id FROM GoodTypes
    WHERE good_type_name = 'equipment'
) FROM Goods
```