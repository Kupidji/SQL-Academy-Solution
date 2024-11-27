### 1. Категоризация отзывов
> [!NOTE]
> Из таблицы Reviews выведите идентификаторы отзывов (поле id) и их категорию: для рейтинга 4-5 проставьте категорию «positive», для 3 проставьте «neutral», а для 1-2 - «negative». Для вывода категории рейтинга используйте псевдоним rating.
```sql
SELECT id,
CASE
    WHEN rating IN (5, 4) THEN 'positive'
    WHEN rating = 3 THEN 'neutral'
    ELSE 'negative'
END AS rating
FROM Reviews;
```