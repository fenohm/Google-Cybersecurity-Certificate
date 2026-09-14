## Cláusula WHERE y operadores básicos en SQL

La cláusula `WHERE` permite **filtrar los resultados de una consulta SQL** utilizando condiciones específicas. Es especialmente útil en ciberseguridad para analizar grandes cantidades de registros y encontrar información concreta, como intentos de inicio de sesión, dispositivos o eventos relacionados con un incidente.

### 🔎 WHERE

`WHERE` establece una condición que deben cumplir los registros para ser incluidos en los resultados.

Ejemplo:

```sql
SELECT *
FROM employees
WHERE title = 'IT Staff';
```

En este caso, solo se muestran los empleados cuyo `title` sea exactamente `'IT Staff'`.

El operador `=` se utiliza para comprobar si un valor coincide exactamente con otro.

### 🔤 LIKE

Cuando se necesita buscar información basándose en un **patrón**, se utiliza `LIKE` junto con `WHERE`.

Por ejemplo:

```sql
SELECT *
FROM employees
WHERE title LIKE 'IT%';
```

Esta consulta devuelve los registros cuyo `title` comienza con `IT`, como `IT Staff` o `IT Manager`.

### 🃏 Comodines

Los comodines permiten realizar búsquedas más flexibles:

| Comodín | Función                            | Ejemplo |
| ------- | ---------------------------------- | ------- |
| `%`     | Representa cero o más caracteres   | `'IT%'` |
| `_`     | Representa exactamente un carácter | `'N_'`  |

Ejemplos:

```sql
-- Comienza con "IT"
WHERE title LIKE 'IT%';

-- Termina con "a"
WHERE name LIKE '%a';

-- Contiene "a"
WHERE name LIKE '%a%';

-- Comienza con N y tiene exactamente dos caracteres
WHERE state LIKE 'N_';
```

### 🛡️ Aplicación en ciberseguridad

El filtrado mediante `WHERE` y `LIKE` permite a los analistas **reducir grandes conjuntos de datos y localizar información relevante**. Por ejemplo, pueden utilizarse para buscar usuarios específicos, dispositivos con determinadas características o registros relacionados con un evento de seguridad.

**Idea clave:** `WHERE` permite establecer condiciones para filtrar datos, mientras que `LIKE` permite realizar búsquedas mediante patrones utilizando los comodines `%` y `_`.
