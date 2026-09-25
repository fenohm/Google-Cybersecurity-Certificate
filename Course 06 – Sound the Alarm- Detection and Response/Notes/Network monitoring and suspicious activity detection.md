## Monitoreo de red y detección de actividad sospechosa

El **monitoreo de red** es una actividad fundamental para los profesionales de seguridad, ya que permite observar el tráfico y las comunicaciones entre dispositivos para identificar actividades anormales o potencialmente maliciosas.

### Línea de base

Una **línea de base (baseline)** representa el comportamiento normal o esperado de una red, sistema o dispositivo. Establecer una línea de base permite comparar la actividad actual con el comportamiento habitual y detectar desviaciones que podrían indicar un incidente de seguridad.

Por ejemplo, un aumento inusual del tráfico durante horarios en los que normalmente existe poca actividad podría requerir una investigación.

### Aspectos que se pueden monitorear

Entre los principales elementos que pueden analizarse se encuentran:

* **Network flow:** información relacionada con el movimiento de las comunicaciones, paquetes, protocolos y puertos.
* **Packet payload:** datos reales transportados dentro de los paquetes. Su análisis puede ayudar a identificar actividades como la exfiltración de información.
* **Temporal patterns:** patrones de tráfico relacionados con horarios y frecuencia de las comunicaciones.
* **IP addresses:** direcciones de origen y destino involucradas en las comunicaciones.
* **Protocols and ports:** combinaciones de protocolos y puertos que pueden revelar comportamientos inusuales.

Un ejemplo de actividad sospechosa es el uso de un protocolo en un puerto diferente al habitual. Este tipo de comportamiento puede utilizarse para establecer comunicaciones de **Command and Control (C2)** entre un sistema comprometido y un atacante.

### Indicadores de compromiso

Los analistas de seguridad también buscan **Indicators of Compromise (IoC)**, que son evidencias que pueden indicar que un sistema o red ha sido comprometido. El análisis de tráfico y registros puede ayudar a identificar estos indicadores y determinar si existe una posible amenaza.

### Herramientas de monitoreo

El monitoreo puede realizarse de forma automatizada o manual mediante diferentes herramientas:

* **IDS:** monitorea la actividad de la red y genera alertas cuando identifica patrones asociados a posibles amenazas.
* **Wireshark:** permite capturar y analizar paquetes de red de forma detallada.
* **tcpdump:** herramienta de línea de comandos utilizada para capturar y analizar tráfico de red.

Estas herramientas permiten examinar las comunicaciones de una red y detectar desviaciones respecto a su comportamiento esperado.

### SOC y NOC

Un **Security Operations Center (SOC)** se enfoca principalmente en la seguridad, monitoreando sistemas y redes para detectar y responder ante amenazas.

Por otro lado, un **Network Operations Center (NOC)** se concentra en el rendimiento, disponibilidad y continuidad de la infraestructura de red.

Comprender el comportamiento normal de una red y utilizar herramientas de monitoreo permite a los analistas detectar desviaciones, identificar posibles compromisos y contribuir a una respuesta más rápida ante incidentes de seguridad.
