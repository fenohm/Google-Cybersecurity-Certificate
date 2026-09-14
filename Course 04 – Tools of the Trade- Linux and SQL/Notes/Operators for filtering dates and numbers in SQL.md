## Operadores para filtrar fechas y números en SQL

En esta sección aprendí a utilizar operadores de comparación en **SQL** para filtrar datos numéricos y valores de fecha y hora mediante la cláusula `WHERE`.

### Conceptos principales

* Los operadores `<`, `>`, `=`, `<=`, `>=` y `<>` permiten comparar valores y obtener únicamente los registros que cumplen una determinada condición.
* Los operadores pueden utilizarse tanto con **números** como con **fechas y horas**, algo especialmente útil en el análisis de registros de seguridad.
* Los operadores pueden ser **exclusivos** o **inclusivos**. Por ejemplo, `>` no incluye el valor utilizado en la comparación, mientras que `>=` sí lo incluye.
* `BETWEEN` permite filtrar registros que se encuentran dentro de un **rango de valores o fechas** y es inclusivo en ambos extremos.

### Aplicación en ciberseguridad

Estos operadores son útiles para analizar información como **intentos de inicio de sesión, cantidad de eventos, volumen de datos, fechas de acceso, registros de actividad y duración de conexiones**.

**Ejemplo:**

```sql
SELECT *
FROM logs
WHERE login_attempts > 5;
```

Esta consulta permite identificar registros donde se realizaron más de 5 intentos de inicio de sesión.

### Aprendizaje

Aprendí a utilizar operadores de comparación y `BETWEEN` para crear filtros más precisos en SQL, facilitando el análisis de datos y la identificación de eventos relevantes dentro de registros de seguridad.
