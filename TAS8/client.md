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

```

## Inserción de datos 

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

## SELECT
### Select_1
```
SELECT * FROM product
WHERE category = 'Gaming' OR category = 'Audio';
```
### Select_2

```
SELECT * FROM product
WHERE price > 100 AND price < 500 AND country_of_origin = 'Japan';
```

### Select_3

```
SELECT * FROM product
WHERE price > 1000 AND (country_of_origin = 'Japan' OR country_of_origin 'USA');
```
