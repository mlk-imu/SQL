# SQL
Привет!) Здесь о том, как я изучала запросы SQL и работала в MySQL Workbench и Shell в рамках интенсива от "Школы седого тестировщика".

## Оглавление
1. Create
2. Read
3. Update
4. Delete

_____

### Create
CREATE TABLE название таблицы (
название столбца1 INT PRIMARY KEY AUTO_INCREMENT,
название столбца2 тип данных,
название столбца3 тип данных
);

INSERT INTO название таблицы (столбец1, столбец2)
VALUES
 (значение 1.1, значение 1.2)
);

UPDATE таблица SET столбец = "значение" WHERE (и добавить условие, например id = 4, чтобы обойти защиту)
_____

### Read
```SHOW DATABASES;```
>Показать список баз данных

![image](https://github.com/HappyToster/SQL/assets/97261554/350da904-e02c-475d-9c81-3c0da632fe93)

```SHOW TABLES;```
>Показать список таблиц в базе

![image](https://github.com/HappyToster/SQL/assets/97261554/7eb24c5a-d74f-4870-ac65-95ce79dfc945)


```SELECT * FROM lavka.country;```
>Выборка всех данных из таблицы

>![image](https://github.com/HappyToster/SQL/assets/97261554/bb8e0513-88d1-4f98-816b-e2d5ffeaca30)

```SELECT name, id_category FROM online_store.goods;```
>Выборка определенных столбцов из таблицы;
>
>![image](https://github.com/HappyToster/SQL/assets/97261554/e88b256a-b86e-4ef1-bd40-fd9403cc4ae0)

```SELECT * FROM таблица WHERE столбец = "УСЛОВИЕ";```
>

```SELECT СТОЛБЕЦ1 AS НОВЫЙ_СТОЛБЕЦ FROM ТАБЛ;```
>Поменять название столбца при выводе

SELECT СТОЛБЕЦ, СТОЛБЕЦ........ МОЖНО ДОБ ОПЕРАЦИЮ, НАПР УМНОЖЕНИЕ NEW*NEW1 AS RESULT FROM ТАБЛ 

SELECT......FROM ТАБЛ WHERE СТОЛБЕЦ1 < УСЛОВИЕ1 AND СТОБЛЕЦ2 > УСЛОВИЕ2 (ВЫРАЖЕНИЕ)
ТАК МОЖНО ВЫБОРКУ ПО ДАТЕ СДЕЛАТЬ
>

SELECT * FROM ТАБЛ WHERE СТОЛБ BETWEEN 2 AND 3 - ВЫВОДИТ ВКЛЮЧИТЕЛЬНО										
										
SELECT * FROM ТАБЛ WHERE СТОЛБ NOT IN ('ЗНАЧ1', 'ЗНАЧ2'...) - НЕ ТАКОЙ И НЕ ТАКОЙ. ОТСЕКАЕТ ЗНАЧЕНИЯ В СКОБКАХ										
										
SELECT * FROM ТАБЛ WHERE СТОЛБ IN ('ЗНАЧ1', 'ЗНАЧ2'...) - ПОЯВЯТСЯ ТОЛЬКО ЗНАЧ В СКОБКАХ										
										
SELECT * FROM ТАБЛ ORDER BY СТОЛБ ПО КОТ ДЕЛАЕМ УПОР-НИЕ ASC ИЛИ DESC										
										
_____

### Update

UPDATE ТАБЛ SET СТОЛБ = "ЗНАЧ" WHERE ID > 0; ТАК ДЕЛАЕМ, ЧТОБ ОБОЙТИ БЕЗОПАСНЫЙ РЕЖИМ. ИЛИ МОЖНО КОНКРЕТНУЮ СТРОКУ УКАЗАТЬ, НАПР ID = 4										

_____

### Delete
