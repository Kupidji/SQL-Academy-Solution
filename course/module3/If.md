### 1. Условный вывод строки
> [!NOTE]
> Из таблицы Rooms выведите идентификаторы сдаваемых жилых помещений (поле id) и наличие телевизора в помещении: если телевизор присутствует выведите «YES», иначе «NO». Для вывода наличия телевизора используйте псевдоним has_tv.
```sql
SELECT id, (
    IF(has_tv, 'YES', 'NO')
) AS has_tv
FROM Rooms 
```

### 2. Замена null на строку
> [!NOTE]
> Из таблицы Teacher выведите имена (поле first_name), отчества (поле middle_name) и фамилии (поле last_name) учителей. Если отчество у учителя отсутствует, выведите в поле middle_name значение «Empty».
```sql
SELECT first_name, (
    IFNULL(middle_name, 'Empty')
) AS middle_name, last_name FROM Teacher
```