### 1. Создание представления
> [!NOTE]
> На основании таблицы Student создайте представление ViewStudent, содержащие только поля id, first_name и last_name.
```sql
CREATE VIEW ViewStudent AS
SELECT id,
       first_name,
       last_name
FROM Student;
```