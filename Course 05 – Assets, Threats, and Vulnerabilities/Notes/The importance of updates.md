# La importancia de las actualizaciones

## Resumen

Las actualizaciones de software son importantes para la ciberseguridad porque permiten corregir vulnerabilidades que podrían ser aprovechadas por atacantes.

El proceso normalmente comienza con una **Vulnerability Assessment (Evaluación de vulnerabilidades)**, continúa con la identificación y priorización de vulnerabilidades y termina con su **remediación**, que puede incluir la instalación de parches.

## Parches de seguridad

Un **Security Patch (Parche de seguridad)** es una actualización diseñada para corregir vulnerabilidades de seguridad en un sistema operativo, aplicación o producto.

Los parches pueden solucionar vulnerabilidades conocidas y problemas de seguridad asociados a **CVE (Common Vulnerabilities and Exposures)**.

También pueden desarrollarse como respuesta a un **Zero-Day**, que corresponde a una vulnerabilidad desconocida previamente o para la cual todavía no existía una corrección disponible cuando comenzó a ser explotada.

Un proceso básico puede representarse así:

```text
Evaluación de vulnerabilidades
          ↓
Identificación
          ↓
Priorización
          ↓
Parche / actualización
          ↓
Verificación
```

## Estrategias de actualización

### Actualizaciones manuales

Las **Manual Updates (Actualizaciones manuales)** requieren que un usuario o administrador busque, descargue e instale las actualizaciones.

**Ventaja:**

* Mayor control sobre cuándo y dónde se aplican los parches.
* Permite probar una actualización antes de desplegarla ampliamente.

**Desventaja:**

* Las actualizaciones pueden olvidarse o retrasarse.
* Las vulnerabilidades críticas pueden permanecer sin corregir durante demasiado tiempo.

En organizaciones grandes, las herramientas de administración pueden utilizarse para seleccionar qué equipos reciben determinadas actualizaciones.

### Actualizaciones automáticas

Las **Automatic Updates (Actualizaciones automáticas)** permiten que el sistema busque, descargue e instale actualizaciones automáticamente.

**Ventajas:**

* Reduce el trabajo manual.
* Facilita mantener los sistemas actualizados.
* Permite aplicar rápidamente parches de seguridad.

**Desventaja:**

* Una actualización que no haya sido probada correctamente puede provocar problemas de compatibilidad o estabilidad.

Por este motivo, en entornos empresariales puede ser necesario probar primero los parches y después desplegarlos de forma controlada.

## Software End-of-Life

**EOL (End-of-Life)** describe software o productos que han llegado al final de su ciclo de soporte.

Cuando un producto llega a EOL, el fabricante normalmente deja de proporcionar:

* Actualizaciones.
* Parches de seguridad.
* Correcciones de errores.
* Soporte oficial.

Continuar utilizando software EOL aumenta el riesgo porque nuevas vulnerabilidades pueden quedar sin solución.

Esto es especialmente importante en dispositivos **IoT (Internet of Things)**, ya que un dispositivo sin soporte o sin parches puede convertirse en un punto de entrada hacia una red.

## Importancia del parcheo

El **Patch Management (Gestión de parches)** es una parte importante de la gestión de vulnerabilidades.

No basta con identificar una vulnerabilidad: también es necesario determinar su prioridad y aplicar una solución cuando sea posible.

Un ejemplo conocido es **WannaCry (2017)**, un ataque de ransomware que afectó a numerosos sistemas a nivel mundial. El incidente demostró las consecuencias que puede tener mantener sistemas vulnerables sin aplicar parches de seguridad disponibles.

## Puntos clave

* Las actualizaciones permiten corregir vulnerabilidades de seguridad.
* Un **Security Patch** está diseñado para solucionar problemas de seguridad.
* Los parches pueden corregir vulnerabilidades identificadas mediante **CVE**.
* Un **Zero-Day** puede ser explotado antes de que exista una solución disponible.
* Las actualizaciones pueden implementarse manual o automáticamente.
* Las actualizaciones automáticas reducen el riesgo de olvidar parches importantes.
* Las actualizaciones manuales proporcionan mayor control sobre el proceso.
* **EOL (End-of-Life)** significa que un producto ya no recibe soporte oficial.
* El software EOL puede representar un riesgo creciente para una organización.
* **Patch Management** forma parte de la gestión y remediación de vulnerabilidades.
