1. Выберите из таблицы orders 3 самых дешевых заказа за всё время.
Данные нужно отсортировать в порядке убывания цены.

SELECT * FROM orders WHERE STATUS != 'cancelled' ORDER BY sum ASC LIMIT 3;

![image](https://github.com/user-attachments/assets/29246b5e-c5f4-43c8-9a56-a65ec95df6e4)

2. Выберите из таблицы orders 2 самых дорогих заказов за всё время.
Данные нужно отсортировать в порядке убывания цены.
   
SELECT * FROM orders WHERE STATUS != 'cancelled' ORDER BY sum DESC LIMIT 2;

![image](https://github.com/user-attachments/assets/45cce39c-5d47-429e-aeca-617bd82b0161)

3. Добавьте в таблицу orders данные о новом заказе стоимостью 8000 рублей. В заказе 4 товара (products).

INSERT INTO orders (id, sum, products) VALUES (6, 8000, 4); 
SELECT * FROM orders;

![image](https://github.com/user-attachments/assets/4aadbec3-c3ac-4017-9dbf-8ba538b17b3a)

4. Добавьте в таблицу products новый товар — «VR-очки», стоимостью 70000 рублей в количестве (count) 2 штук.
   
INSERT INTO products (id, name, count, price) VALUES (7, 'VR-очки', 2, 70000); 
SELECT * FROM products;

![image](https://github.com/user-attachments/assets/20836d91-dc22-41e4-b2ac-9dc206ee1355)

5. В таблицу products внесли данные с ошибкой, вместо "PS5" в наименовании написали IMAC. Исправьте ошибку.
   
UPDATE products SET name = 'PS5' WHERE name = 'IMAC'; SELECT * FROM products;

![image](https://github.com/user-attachments/assets/79694ffd-8302-4264-9d41-9bb4af46ff54)
