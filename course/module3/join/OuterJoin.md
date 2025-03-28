### 1. Внешнее левое соединение
> [!NOTE]
> Выведите имя first_name и фамилию last_name каждого учителя из таблицы Teacher, а также количество занятий, в которых он был назначен преподавателем. Если преподаватель не был назначен ни на одно занятие, то выведите 0.
Для вывода количества занятий используйте псевдоним amount_classes.
```sql
SELECT T.first_name, T.last_name, COUNT(S.class) amount_classes FROM Teacher T
LEFT JOIN Schedule S ON S.teacher = T.id
GROUP BY T.id
```