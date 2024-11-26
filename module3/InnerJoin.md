###1. INNER JOIN.
> [!NOTE]
> Объедините таблицы Class и Student_in_class с помощью внутреннего соединения по полям Class.id и Student_in_class.class. Выведите название класса (поле Class.name) и идентификатор ученика (поле Student_in_class.student).
```
SELECT C.name, SinC.student FROM Class C
JOIN Student_in_class SinC ON C.id = SinC.class
```


###2. Многотабличный INNER JOIN
> [!NOTE]
> Дополните запрос из предыдущего задания, добавив ещё одно внутреннее соединение с таблицей Student. Объедините по полям Student_in_class.student и Student.id и вместо идентификатора ученика выведите его имя (поле first_name).
```
SELECT C.name, first_name FROM Class C
JOIN Student_in_class SinC ON C.id = SinC.class
JOIN Student S ON SinC.student = S.id
```

###3. Многотабличный INNER JOIN с фильтрацией строк
> [!NOTE]
>Выведите названия продуктов, которые покупал член семьи со статусом "son". Для получения выборки вам нужно объединить таблицу Payments с таблицей FamilyMembers по полям family_member и member_id, а также с таблицей Goods по полям good и good_id.
```
SELECT G.good_name FROM FamilyMembers FM
JOIN Payments P ON FM.member_id = P.family_member
JOIN Goods G ON P.good = G.good_id
WHERE FM.status = 'son'
```

###4. INNER JOIN с группировкой
> [!NOTE]
> Выведите идентификатор (поле room_id) и среднюю оценку комнаты (поле rating, для вывода используйте псевдоним avg_score), составленную на основании отзывов из таблицы Reviews. Данная таблица связана с Reservations (таблица, где вы можете взять идентификатор комнаты) по полям reservation_id и Reservations.id.
```
SELECT Res.room_id, AVG(Rev.rating) avg_score FROM Reservations Res
JOIN Reviews Rev ON Res.id = Rev.reservation_id
GROUP BY Res.room_id
```