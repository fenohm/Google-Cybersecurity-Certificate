# SQL Reference Guide

**Google Cybersecurity Certificate**

## 1. Consultar una base de datos

Las palabras clave principales para recuperar información son:

* `SELECT`: indica qué columnas devolver.

  ```sql
  SELECT employee_id
  FROM employees;
  ```

  `SELECT *` devuelve todas las columnas.

* `FROM`: indica la tabla que se consultará.

  ```sql
  FROM employees
  ```

* `ORDER BY`: ordena los resultados según una o más columnas.

  ```sql
  ORDER BY department ASC;
  ORDER BY city DESC;
  ORDER BY country, city;
  ```

---

## 2. Filtrar consultas

`WHERE` permite establecer condiciones para obtener únicamente los registros relevantes.

### Operadores de comparación

| Operador | Función           |
| -------- | ----------------- |
| `=`      | Igual a           |
| `>`      | Mayor que         |
| `>=`     | Mayor o igual que |
| `<`      | Menor que         |
| `<=`     | Menor o igual que |
| `<>`     | Diferente de      |
| `!=`     | Diferente de      |

Ejemplo:

```sql
WHERE birthdate >= '1965-06-30';
```

### Operadores lógicos

* `AND`: ambas condiciones deben cumplirse.
* `OR`: se debe cumplir una o ambas condiciones.
* `NOT`: niega una condición.

```sql
WHERE country = 'Canada' OR country = 'USA';
```

### BETWEEN

Permite filtrar valores dentro de un rango de números o fechas.

```sql
WHERE hiredate BETWEEN '2002-01-01' AND '2003-01-01';
```

### LIKE y comodines

`LIKE` permite buscar patrones dentro de una columna.

* `%`: representa cualquier cantidad de caracteres.
* `_`: representa exactamente un carácter.

```sql
WHERE title LIKE 'IT%';
WHERE state LIKE 'N_';
```

---

## 3. Unir tablas

Los `JOIN` permiten combinar información de diferentes tablas mediante una columna relacionada.

### INNER JOIN

Devuelve únicamente los registros que coinciden en ambas tablas.

```sql
SELECT *
FROM employees
INNER JOIN machines
ON employees.device_id = machines.device_id;
```

### LEFT JOIN

Devuelve todos los registros de la tabla izquierda y las coincidencias de la tabla derecha.

```sql
SELECT *
FROM employees
LEFT JOIN machines
ON employees.device_id = machines.device_id;
```

### RIGHT JOIN

Devuelve todos los registros de la tabla derecha y las coincidencias de la tabla izquierda.

```sql
SELECT *
FROM employees
RIGHT JOIN machines
ON employees.device_id = machines.device_id;
```

### FULL OUTER JOIN

Devuelve todos los registros de ambas tablas, tengan o no coincidencia.

```sql
SELECT *
FROM employees
FULL OUTER JOIN machines
ON employees.device_id = machines.device_id;
```

---

## 4. Realizar cálculos

Las **funciones de agregación** permiten realizar cálculos sobre múltiples registros.

* `COUNT()`: cuenta registros.
* `AVG()`: calcula el promedio.
* `SUM()`: calcula la suma.

Ejemplos:

```sql
SELECT COUNT(firstname)
FROM customers;
```

```sql
SELECT AVG(height)
FROM employees;
```

```sql
SELECT SUM(cost)
FROM products;
```

## Aplicación en ciberseguridad

Estas herramientas permiten consultar, filtrar, relacionar y analizar grandes cantidades de información almacenada en bases de datos. En un contexto de **ciberseguridad**, SQL puede utilizarse para investigar eventos, analizar usuarios, dispositivos, intentos de acceso y otros registros relevantes.

### Conceptos fundamentales aprendidos

`SELECT` → consultar datos
`WHERE` → filtrar datos
`ORDER BY` → ordenar resultados
`AND / OR / NOT` → combinar condiciones
`LIKE / % / _` → buscar patrones
`BETWEEN` → filtrar rangos
`JOIN` → relacionar tablas
`COUNT / AVG / SUM` → realizar cálculos
