# Subconsultas
## SQL
## Realizar 2 ejemplos de la base de datos Events con subconsultas

### Ejemplo 1

```
SELECT c.title, c.speaker
  (SELECT city FROM events
   WHERE city = 'Quito') 
FROM conferences c

```

<img src=''>


### Ejemplo 2

```

```

<img src=''>
