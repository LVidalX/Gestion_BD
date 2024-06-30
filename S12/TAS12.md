# Tarea Autonoma - Semana 12

## Sentencia 1
### Crear una vista que muestre la lista de productos comprados por los clientes con las siguientes columnas: 
Base de datos: Invoice || 
nombre_cliente | fecha_compra | nombre_producto | cantidad

```
CREATE VIEW client_view AS
SELECT c.full_name, i.create_at, p.description, d.quantity
FROM client c 
JOIN invoice i
ON i.id = c.id
JOIN product p 
ON p.id = c.id
JOIN detail d
ON d.id = c.id;

```

## Sentencia 2
### Crear una vista donde se muestre la lista de miembros registrados a las conferencias.
Base de datos: Event ||
nombre_conferencia | codigo_registro | nombre_miembro 

```

```

