## Operadores lógicos: AND, OR y NOT

Los operadores lógicos **AND**, **OR** y **NOT** permiten crear filtros más específicos en consultas SQL mediante la combinación o negación de condiciones dentro de la cláusula `WHERE`.

* **AND:** requiere que **todas las condiciones** se cumplan simultáneamente.
* **OR:** permite que se cumpla **una o más condiciones**.
* **NOT:** **niega una condición**, devolviendo los registros que no coinciden con ella.
* También es posible combinar estos operadores para construir filtros más complejos y obtener únicamente la información relevante.

Además, para comprobar que un valor sea diferente de otro, pueden utilizarse los operadores `<>` o `!=`, por ejemplo:

```sql
WHERE country <> 'USA';
```

El uso de estos operadores es especialmente importante en **ciberseguridad**, ya que permite filtrar grandes cantidades de registros y analizar información específica, como intentos de acceso, usuarios, ubicaciones o eventos relacionados con la seguridad.
