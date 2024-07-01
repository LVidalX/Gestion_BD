# Subconsultas SQL
## Realizar 2 ejemplos de la base de datos Events con subconsultas

### Ejemplo 1

```
SELECT c.title, c.speaker
  (SELECT city FROM events
   WHERE city = 'Quito') 
FROM conferences c

```

<img src='\Capturas\ejemplo_1.png'>


### Ejemplo 2

```
SELECT m.name, m.last_name,
  (
  SELECT c.id AS conference
  FROM conferences c
  WHERE id = 3
  )
FROM members m;
```

<img src='\Capturas\ejemplo_2.png'>
