# PyMySQL
Імітація бази даних &lt;PyMySQL>

Встановіть модулі:
- pip install prettytable

Далі запустіть застосунок через main.py

# Інструкція по застосунку:

1. CREATE table_name (column_name [INDEXED] [, ...]); - створення таблиці.
 - CREATE students (name, group);
 - CREATE cats (id INDEXED, name INDEXED, favourite_food);

2. INSERT [INTO] table_name (“value” [, ...]); - додавання нового рядка з даними до таблиці.
 - INSERT INTO cats ("1", "Murzik", "Sausages");
 - INSERT cats ("2", "Pushok", "Fish");

3. SELECT FROM table_name [WHERE condition]; - формування вибірки із таблиці table_name:

    condition := column_name operator "value"
    | (condition) AND (condition)
    | (condition) OR (condition)
    | operator  := ( = | < ).

 - SELECT FROM cats;
 - SELECT FROM cats WHERE (name < "Murzik") OR (name = "Pushok");

                +----+--------+----------------+
                | id |  name  | favourite_food |
                +----+--------+----------------+
                |  1 | Murzik |    Sausages    |
                |  2 | Pushok |      Fish      |
                +----+--------+----------------+

4. SAVE - зберігає нашу базу до файлу.
 - SAVE;

5. EXIT - вихід з програми (За стандартом зберігає базу перед виходом).
 - EXIT;
