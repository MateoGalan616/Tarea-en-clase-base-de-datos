### Creacion de la tabla 
'''
CREATE TABLE product (
    id INT PRIMARY KEY,
    description VARCHAR(255),
    price DECIMAL(10, 2),
    category VARCHAR(50),
    country_of_origin VARCHAR(100),
    year_of_production INT
);

'''
### insercion de datos 
'''
INSERT INTO product (id, description, price, category, country_of_origin, year_of_production) VALUES
(1, 'Smartphone con pantalla de 6.5 pulgadas', 299.99, 'Electronics', 'China', 2022),
(2, 'Cafetera de espresso automática', 149.95, 'Home Appliances', 'Italy', 2021),
(3, 'Bicicleta de montaña', 499.50, 'Outdoor', 'USA', 2020),
(4, 'Cámara fotográfica digital', 249.99, 'Photography', 'Japan', 2023),
(5, 'Reloj inteligente con monitor de frecuencia cardíaca', 199.99, 'Wearables', 'South Korea', 2023),
(6, 'Zapatillas deportivas para correr', 89.95, 'Footwear', 'Germany', 2022),
(7, 'Aspiradora robot', 179.99, 'Home Appliances', 'China', 2021),
(8, 'Televisor 4K de 55 pulgadas', 599.99, 'Electronics', 'Mexico', 2023),
(9, 'Cocina de gas con 5 quemadores', 699.00, 'Kitchen Appliances', 'USA', 2020),
(10, 'Parlante inalámbrico Bluetooth', 59.99, 'Audio', 'France', 2022),
(11, 'Camiseta de algodón orgánico', 25.00, 'Apparel', 'India', 2021),
(12, 'Tablet de 10 pulgadas', 329.99, 'Electronics', 'China', 2023),
(13, 'Mochila de senderismo 50L', 75.50, 'Outdoor', 'Canada', 2022),
(14, 'Gafas de sol polarizadas', 39.95, 'Accessories', 'Italy', 2021),
(15, 'Impresora multifuncional', 159.99, 'Office Supplies', 'Japan', 2022),
(16, 'Juego de ollas de acero inoxidable', 99.95, 'Kitchen Appliances', 'Brazil', 2020),
(17, 'Monitor de computadora 27 pulgadas', 279.99, 'Electronics', 'South Korea', 2023),
(18, 'Trotadora eléctrica', 399.00, 'Fitness', 'USA', 2021),
(19, 'Cámara de seguridad para exteriores', 119.99, 'Home Security', 'China', 2022),
(20, 'Auriculares con cancelación de ruido', 199.99, 'Audio', 'Germany', 2023);
'''

# Contar el número de productos de una categoría específica:
SELECT COUNT(*) FROM product WHERE category = 'NombreDeLaCategoría';


# Contar el número de clientes en una ciudad específica:
SELECT COUNT(*) AS customer_count
FROM client
WHERE city = 'San Francisco';



# Contar el número de productos cuyo precio está dentro de un rango específico
SELECT COUNT(*) AS product_count
FROM product
WHERE price BETWEEN 100.00 AND 200.00;


# Seleccionar clientes que viven en una ciudad específica y tienen un tipo de cliente específico
SELECT *
FROM client
WHERE city = 'San Francisco' AND type_of_client = 'Premium';


# Seleccionar productos que pertenecen a una categoría específica y cuyo precio está por encima de un valor específico
SELECT *
FROM product
WHERE category = 'Home Appliances' AND price > 150.00;


# Seleccionar productos que fueron producidos en un año específico y en un país de origen específico
SELECT *
FROM product
WHERE year_of_production = 2022 AND country_of_origin = 'China';


# Seleccionar clientes cuyo nombre completo comience con 'J'
SELECT *
FROM client
WHERE fullname LIKE 'J%';


#  Seleccionar clientes cuya ciudad contenga la letra 'a'
SELECT *
FROM client
WHERE city LIKE '%a%';
