## SIEM – Información de seguridad y gestión de eventos

Un **Security Information and Event Management (SIEM)** es una herramienta que recopila, centraliza y analiza datos de registros (*logs*) provenientes de diferentes sistemas y dispositivos de una organización. Su objetivo es ayudar a los equipos de seguridad a **monitorear, detectar, investigar y responder ante posibles incidentes**.

### Principales ventajas

Las herramientas SIEM permiten:

* **Centralizar datos:** recopilan registros provenientes de fuentes como firewalls, servidores, routers y otros dispositivos.
* **Monitorear y generar alertas:** analizan continuamente los eventos y generan alertas cuando detectan actividades que coinciden con determinadas reglas de seguridad.
* **Almacenar registros:** conservan información histórica que puede utilizarse durante investigaciones y análisis de incidentes.
* **Facilitar las investigaciones:** permiten analizar información de múltiples fuentes desde un lugar centralizado.

### Proceso SIEM

El proceso SIEM puede dividirse en tres etapas principales:

1. **Recopilación y agregación de datos:** el SIEM recopila registros de diferentes fuentes y los centraliza en un mismo lugar. Los registros pueden contener información como marcas de tiempo, direcciones IP, usuarios, procesos y puertos.

2. **Normalización de datos:** los registros provenientes de diferentes sistemas pueden utilizar formatos distintos. La normalización transforma estos datos en un formato estructurado y consistente para facilitar su búsqueda y análisis.

3. **Análisis de datos:** el SIEM aplica reglas y condiciones de detección sobre los registros para identificar actividades sospechosas. Cuando los eventos coinciden con determinadas reglas, se generan alertas para que los analistas puedan investigarlas.

### Conceptos importantes

* **Parsing:** proceso mediante el cual se separa la información de un registro en campos y valores específicos para facilitar su interpretación.
* **Normalización:** transformación de datos provenientes de diferentes fuentes a un formato estándar y estructurado.
* **Correlación:** comparación de múltiples eventos para identificar relaciones o patrones que podrían indicar una amenaza.

Por ejemplo, varios eventos aparentemente independientes, como múltiples intentos fallidos de inicio de sesión desde una misma dirección IP, pueden correlacionarse para identificar un posible ataque.

### Herramientas SIEM

Algunas herramientas SIEM utilizadas en la industria incluyen **Splunk, IBM QRadar, Elastic, Exabeam, Chronicle, LogRhythm y AlienVault OSSIM**.

Comprender el funcionamiento de un SIEM es fundamental para un analista de seguridad, ya que permite trabajar con grandes cantidades de registros, identificar patrones sospechosos y generar información útil para la **detección y respuesta ante incidentes**.
