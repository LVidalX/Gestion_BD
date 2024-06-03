# Tarea en clase semana 8
## Funcion count
## Creación de la tabla

```
CREATE TABLE IF NOT EXISTS client (
      id SERIAL,
      nui VARCHAR(10) NOT NULL,
      full_name VARCHAR(100) NOT NULL,
      phone VARCHAR(10),
      type_of_client VARCHAR(50) DEFAULT 'BASIC',
      city VARCHAR(50),
      credit_limit DECIMAL(7,2) 
);


CREATE TABLE product (
      id SERIAL PRIMARY KEY,
      description VARCHAR(255),
      price DECIMAL(10, 2),
      category VARCHAR(50),
      country_of_origin VARCHAR(50),
      year_of_production INT 
);

```

## Inserción de datos 
### Tabla Client
```
INSERT INTO client(id, nui, full_name, phone, type_of_client, city, credit_limit)
       VALUES(1001, '235764892', 'Ana García Pérez', '1943835670', 'Particular', 'Cuenca', 5000),
             (1002, '589327641', 'John Smith', '2494381931', 'Corporativo', 'Quito', 50000),
             (1003, '741962583', 'María González', '2914831483', 'Particular', 'Guayaquil', 7500),
             (1004, '862543198', 'David Johnson', '1943835670', 'Corporativo', 'Ambato', 75000),
             (1005, '437896213', 'Sofia Martínez', '7658301833', 'Particular', 'Cuenca', 10000),
             (1006, '915324876', 'Michael Brown', '8540139451', 'Corporativo', 'Guayaquil', 60000),
             (1007, '369785241', 'Laura López', '9485145730', 'Particular', 'Quito', 8000),
             (1008, '584239671', 'Daniel Jackson', '4593814306', 'Corporativo', 'Ambato', 70000),
             (1009, '752963147', 'Andrea Fernández', '6914841493', 'Particular', 'Cuenca', 6000),
             (1010, '631487952', 'Mark Taylor', '2885330197', 'Corporativo', 'Quito', 55000);
```

### Tabla Product

```
INSERT INTO product (id, description, price, category, country_of_origin, year_of_production)
         VALUES (1001, 'Women’s Dress', 59.99, 'Clothing', 'France', 2021),
                (1002, 'Kids’ T-shirt', 19.99, 'Clothing', 'Bangladesh', 2022),
                (1003, 'Running Shoes', 79.99, 'Clothing', 'Vietnam', 2023),
                (1004, 'Jeans', 49.99, 'Clothing', 'Mexico', 2021),
                (1005, 'Leather Boots', 129.99, 'Clothing', 'Italy', 2022),
                (1006, 'Winter Coat', 199.99, 'Clothing', 'Canada', 2023),
                (1007, 'Summer Hat', 14.99, 'Clothing', 'China', 2021),
                (1008, 'Sneakers', 69.99, 'Clothing', 'USA', 2022),
                (1009, 'Scarf', 24.99, 'Clothing', 'India', 2021),
                (1010, 'Wooden Dining Table', 599.99, 'Furniture', 'Germany', 2022),
                (1011, 'Office Chair', 199.99, 'Furniture', 'USA', 2021),
                (1012, 'Sofa Set', 899.99, 'Furniture', 'Italy', 2023),
                (1013, 'Bookshelf', 149.99, 'Furniture', 'Sweden', 2022),
                (1014, 'Bed Frame', 399.99, 'Furniture', 'China', 2021),
                (1015, 'Wardrobe', 799.99, 'Furniture', 'Germany', 2023);
 
```


## Consulta de Datos

### Mostrar el total de nombres.
Para mostrar todos los nombres usamos la funcion COUNT() pasandole como parametro el campo, en este campo *full_name*

```
SELECT COUNT (full_name) AS total_names
FROM client;
```

<img src="">


### Count City

```
SELECT COUNT (DISCTINCT city) AS total_cities
FROM client;

```

### Count Phone

```
SELECT COUNT (phone)
FROM client;
```

### Count Phone and names

```
SELECT COUNT (phone, names)
FROM client;
```

### Count Cities with Distinct

```
SELECT COUNT (DISTINCT City)
FROM client;
```


## WHERE
### Multiples criterios AND, OR, BETWEEN.



# TA_S8

## CONSULTAS


## SELECT
### Select_1
```
SELECT COUNT(*) AS numero_de_productos
FROM product
WHERE category = 'Clothing';

```
<img src='\capturas\Select_1.png'>

### Select_2

```
SELECT COUNT(*) AS numero_de_clientes
FROM client
WHERE city = 'Italy';

```
<img src='\capturas\Select_2.png'>

### Select_3

```
SELECT COUNT(*) AS numero_de_productos
FROM product
WHERE price BETWEEN 50 AND 150;

```

<img src='\capturas\Select_3.png'>

### Select_4

```
SELECT * FROM client
WHERE city = 'Ambato' AND type_of_client = 'Corporativo';

```

<img src='\capturas\Select_4.png'>

### Select_5

```
SELECT * FROM product
WHERE category = 'nombre_de_la_categoria' AND price > valor_especifico;

```

<img src='\capturas\Select_5.png'>

### Select_6

```
SELECT * FROM product
WHERE year_of_production = 2021 AND country_of_origin = 'USA';

```
<img src='\capturas\Select_6.png'>

### Select_7

```
SELECT *
FROM client
WHERE fullname LIKE 'J%';

```

<img src='\capturas\Select_7.png'>

### Select_8

```
SELECT *
FROM client
WHERE city LIKE '%a%';

```

<img src='\capturas\Select_8.png'>





