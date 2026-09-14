## Tipos de JOIN en SQL

Los **JOIN** permiten combinar información de dos o más tablas utilizando una columna que tienen en común. Dependiendo del tipo de unión, SQL puede devolver únicamente los registros coincidentes o también aquellos que no tienen coincidencia.

* **INNER JOIN:** devuelve únicamente los registros que tienen coincidencias en ambas tablas.
* **LEFT JOIN:** devuelve **todos los registros de la tabla izquierda** y únicamente los registros coincidentes de la tabla derecha.
* **RIGHT JOIN:** devuelve **todos los registros de la tabla derecha** y únicamente los registros coincidentes de la tabla izquierda.
* **FULL OUTER JOIN:** devuelve **todos los registros de ambas tablas**, incluyendo los que no tienen coincidencias.

La estructura básica de una unión utiliza `ON` para indicar las columnas que relacionan ambas tablas:

```sql
SELECT *
FROM employees
INNER JOIN machines
ON employees.device_id = machines.device_id;
```

También es importante especificar el nombre de la tabla junto con la columna cuando esta existe en ambas tablas, utilizando la notación `tabla.columna`.

Los diferentes tipos de **JOIN** son fundamentales para analizar información distribuida en varias tablas, especialmente en tareas de **ciberseguridad**, donde es necesario relacionar datos como empleados, dispositivos, usuarios y eventos.
