### 1. Обновление имени у пользователя
> [!NOTE]
> Измените имя у "Wednesday Addams" на новое "Tuesday Addams".
```sql
UPDATE FamilyMembers
SET member_name = 'Tuesday Addams'
WHERE member_name = 'Wednesday Addams';
```

### 2. Обновление стоимости у всего жилья
> [!NOTE]
> Обновите стоимость всех комнат в таблице (Rooms), добавив к текущей 10 единиц
```sql
UPDATE Rooms
SET price = price + 10;
```