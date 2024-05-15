# Examen_bases_de_datos


**Consultas sobre una tabla**

1. Devuelve un listado con el código de oficina y la ciudad donde hay oficinas.

```mysql
SELECT oficina.id_oficina, c.nombre as Ciudad
FROM oficina_direccion as oficina 
RIGHT JOIN direccion as d ON d.id_ciudad = oficina.id_direccion 
INNER JOIN ciudad as c ON c.id_ciudad = d.id_ciudad
WHERE oficina.id_oficina IS NOT NULL;

+------------+-----------+
| id_oficina | Ciudad    |
+------------+-----------+
|          1 | Madrid    |
|          2 | Barcelona |
|          3 | París     |
|          4 | Milán     |
|          5 | Múnich    |
+------------+-----------+
5 rows in set (0.00 sec)
   ```
