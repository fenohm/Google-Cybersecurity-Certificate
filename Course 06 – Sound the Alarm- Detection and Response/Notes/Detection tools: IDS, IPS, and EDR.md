## Herramientas de detección: IDS, IPS y EDR

Las herramientas de detección permiten a las organizaciones monitorear sus redes y sistemas para identificar actividades sospechosas o maliciosas. Entre las principales herramientas se encuentran **IDS, IPS y EDR**, cada una con diferentes capacidades de detección y respuesta.

### IDS – Intrusion Detection System

Un **IDS** monitorea la actividad de una red o sistema para detectar posibles amenazas y generar alertas. Su función principal es **detectar y registrar**, pero no detener automáticamente la actividad maliciosa.

Algunas herramientas IDS son **Snort, Suricata, Zeek y Sagan**.

### IPS – Intrusion Prevention System

Un **IPS** también monitorea la actividad en busca de amenazas, pero a diferencia del IDS, puede **tomar acciones para prevenir o detener** una actividad maliciosa. Por ejemplo, puede bloquear determinado tráfico mediante reglas de seguridad.

Herramientas como **Snort, Suricata y Sagan** pueden utilizarse tanto como IDS como IPS.

### EDR – Endpoint Detection and Response

Un **EDR** se instala en los dispositivos finales de una organización, como computadores, teléfonos o tablets. Monitorea, registra y analiza la actividad de estos dispositivos para detectar comportamientos sospechosos.

A diferencia de IDS e IPS, las herramientas EDR realizan **análisis de comportamiento** y pueden utilizar automatización para responder ante determinadas amenazas. Por ejemplo, pueden bloquear automáticamente la ejecución de un proceso sospechoso.

### Tipos de resultados de detección

Al analizar las alertas de seguridad es importante distinguir entre cuatro resultados:

* **True Positive:** se detecta correctamente una actividad maliciosa.
* **True Negative:** no existe actividad maliciosa y no se genera una alerta.
* **False Positive:** se genera una alerta por una actividad que en realidad no es maliciosa.
* **False Negative:** existe una actividad maliciosa, pero la herramienta no logra detectarla.

Los **false positives** pueden consumir tiempo y recursos del equipo de seguridad al investigar alertas legítimas, mientras que los **false negatives** son especialmente relevantes porque una amenaza puede pasar desapercibida.

### Comparación

| Herramienta | Detecta | Previene | Análisis de comportamiento |
| ----------- | ------- | -------- | -------------------------- |
| **IDS**     | Sí      | No       | No                         |
| **IPS**     | Sí      | Sí       | No                         |
| **EDR**     | Sí      | Sí       | Sí                         |

Comprender las diferencias entre IDS, IPS y EDR permite interpretar correctamente las alertas de seguridad y conocer qué tipo de respuesta puede proporcionar cada herramienta. Estas tecnologías forman parte de las herramientas utilizadas por los equipos de seguridad para **detectar, analizar y responder ante amenazas**.
