## Consulta de una base de datos SQL

Las consultas SQL permiten **extraer, organizar y analizar información almacenada en bases de datos**. En el curso se utiliza la base de datos de ejemplo **Chinook**, que contiene diferentes tablas como `employees`, `customers` e `invoices`.

### 🗄️ Consultas básicas

Las dos palabras clave fundamentales son:

* `SELECT`: indica qué columnas se desean obtener.
* `FROM`: indica desde qué tabla se obtendrán los datos.

Ejemplo:

```sql
SELECT customerid, city
FROM customers;
```

Para seleccionar todas las columnas de una tabla se utiliza `*`:

```sql
SELECT *
FROM customers;
```

El punto y coma `;` indica el final de la consulta.

### 🔢 ORDER BY

La cláusula `ORDER BY` permite **ordenar los resultados** según una o más columnas.

Por defecto, los resultados se ordenan de forma **ascendente (`ASC`)**:

```sql
SELECT customerid, city, country
FROM customers
ORDER BY city;
```

También es posible utilizar `DESC` para ordenar de forma **descendente**:

```sql
SELECT customerid, city, country
FROM customers
ORDER BY city DESC;
```

* Datos numéricos: de menor a mayor con `ASC` y de mayor a menor con `DESC`.
* Datos de texto: orden alfabético de A-Z con `ASC` y de Z-A con `DESC`.

### 📊 Ordenar por varias columnas

`ORDER BY` también permite utilizar varias columnas. SQL ordenará primero por la primera columna y, cuando existan valores iguales, utilizará la siguiente columna como criterio secundario.

Ejemplo:

```sql
SELECT customerid, city, country
FROM customers
ORDER BY country, city;
```

En este caso, los registros se organizan primero por `country` y posteriormente por `city` dentro de cada país.

### 💡 Aplicación en ciberseguridad

Las consultas SQL son fundamentales para un analista de ciberseguridad, ya que permiten **extraer información específica, organizar grandes cantidades de datos y analizar registros almacenados en bases de datos**.

**Idea clave:** `SELECT` determina qué datos obtener, `FROM` indica de qué tabla y `ORDER BY` permite organizar los resultados. Estas instrucciones constituyen la base para desarrollar consultas SQL más avanzadas.
