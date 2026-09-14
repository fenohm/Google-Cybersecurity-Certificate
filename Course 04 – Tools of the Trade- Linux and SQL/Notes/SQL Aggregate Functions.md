## Funciones de agregación en SQL

Las **funciones de agregación** permiten realizar cálculos sobre múltiples registros y devolver un único resultado, facilitando el análisis y resumen de grandes cantidades de datos.

Las principales funciones estudiadas fueron:

* **COUNT:** cuenta la cantidad de registros, ignorando los valores `NULL`.
* **AVG:** calcula el promedio de los valores numéricos de una columna.
* **SUM:** calcula la suma de los valores numéricos de una columna.

Estas funciones se utilizan dentro de `SELECT` y pueden combinarse con filtros mediante `WHERE` para obtener resultados más específicos.

Ejemplo:

```sql
SELECT COUNT(firstname)
FROM customers
WHERE country = 'USA';
```

Las funciones de agregación son especialmente útiles para **analizar y resumir información**, permitiendo identificar cantidades, promedios y totales relevantes para el trabajo de un analista de ciberseguridad.

### Aprendizaje continuo

SQL es un lenguaje amplio que cuenta con muchas funciones y herramientas adicionales. Continuar practicando mediante diferentes bases de datos y problemas reales permite desarrollar la capacidad de identificar qué información se necesita y construir consultas para obtenerla.

El **aprendizaje continuo y la práctica** son fundamentales para ampliar el uso de SQL en tareas de análisis de datos y ciberseguridad.
