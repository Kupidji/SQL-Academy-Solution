### 1. Функция STR_TO_DATE
> [!NOTE]
> Пропишите формат строки во втором аргументе функции STR_TO_DATE, чтобы функция корректно отработала и вернула дату, на основании переданной первым аргументом строки.
```sql
SELECT STR_TO_DATE('Date: 31 December 2023', 'Date: %d %M %Y') AS date
```

### 2. Определение возраста
> [!NOTE]
> Выведите имена (поле member_name) и возраст для каждого человека из таблицы FamilyMembers. Для вывода возраста используйте псевдоним age.
```sql
SELECT member_name, TIMESTAMPDIFF(YEAR, birthday, NOW()) as age FROM FamilyMembers
```