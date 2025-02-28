1. Выберите из таблицы orders 3 самых дешевых заказа за всё время.

SELECT * FROM orders WHERE STATUS != 'cancelled' ORDER BY sum ASC LIMIT 3;

![image](https://github.com/user-attachments/assets/13430d6a-cc92-4ff5-920f-80e1c90f07aa)

2. Выберите из таблицы orders 2 самых дорогих заказов за всё время.
   
SELECT * FROM orders WHERE STATUS != 'cancelled' ORDER BY sum DESC LIMIT 2;

![image](https://github.com/user-attachments/assets/36c6e429-7f5d-459a-8b9f-c6a2dc96ee46)

3. Добавьте в таблицу orders данные о новом заказе стоимостью 8000 рублей. В заказе 4 товара (products).

INSERT INTO orders (id, sum, products) VALUES (6, 8000, 4); 
SELECT * FROM orders;

![image](https://github.com/user-attachments/assets/3c7b93e7-68cb-4447-9fff-42a7c301238d)

4. Добавьте в таблицу products новый товар — «VR-очки», стоимостью 70000 рублей в количестве (count) 2 штук.
   
INSERT INTO products (id, name, count, price) VALUES (7, 'VR-очки', 2, 70000); 
SELECT * FROM products;

![image](https://github.com/user-attachments/assets/c8931ad8-7652-462c-8ad6-4b28f11f85d9)

5. В таблицу products внесли данные с ошибкой, вместо "PS5" в наименовании написали IMAC. Исправьте ошибку.
   
UPDATE products SET name = 'PS5' WHERE name = 'IMAC'; SELECT * FROM products;

![image](https://github.com/user-attachments/assets/9f3d1a1c-c12b-4019-915a-89b322f3d1e6)

