### 1. Округление до чисел кратных 10-ти
> [!NOTE]
> Выведите список цен всего доступного жилья (из таблицы Rooms), округлённых к ближайшему кратному 10-ти числу. Например, если цена равна "9676", то после округления она будет равна "9680". Для вывода цены используйте псевдоним rounded_price.
```sql
SELECT ROUND(price, -1) rounded_price FROM Rooms
```