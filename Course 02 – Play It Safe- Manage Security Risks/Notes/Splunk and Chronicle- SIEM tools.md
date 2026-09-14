# Splunk y Chronicle: herramientas SIEM

## Splunk

**Splunk** ofrece soluciones SIEM como **Splunk Enterprise** y **Splunk Cloud**. Estas herramientas permiten recopilar, buscar, supervisar y analizar registros provenientes de múltiples fuentes.

Los datos pueden visualizarse mediante diferentes **paneles de control**, proporcionando a los equipos de seguridad una visión general de las operaciones y ayudándolos a detectar e investigar posibles amenazas.

### Paneles principales de Splunk

#### Panel de postura de seguridad

Está orientado a los **Centros de Operaciones de Seguridad (SOC)**. Muestra eventos y tendencias de seguridad recientes, permitiendo evaluar si las políticas y controles de seguridad están funcionando correctamente.

También puede utilizarse para investigar amenazas en tiempo real, como actividad de red sospechosa asociada a una dirección IP.

#### Panel de resumen ejecutivo

Proporciona una visión general del **estado de seguridad de la organización a lo largo del tiempo**.

Es especialmente útil para presentar información de alto nivel a responsables y partes interesadas, como estadísticas sobre incidentes y tendencias de seguridad.

#### Panel de revisión de incidentes

Permite identificar **patrones sospechosos relacionados con incidentes de seguridad**.

Destaca los elementos de mayor riesgo y proporciona una **cronología visual de los acontecimientos**, ayudando a los analistas a comprender qué ocurrió antes, durante y después de un incidente.

#### Panel de análisis de riesgos

Permite evaluar el riesgo asociado a diferentes objetos, como:

* Usuarios.
* Computadores.
* Direcciones IP.

Ayuda a detectar cambios de comportamiento, por ejemplo, un inicio de sesión fuera del horario habitual o un volumen de tráfico de red anormalmente elevado.

Esta información permite a los analistas **priorizar las acciones de mitigación de riesgos**.

---

# Chronicle

**Chronicle**, actualmente conocido como parte de **Google SecOps**, es una solución SIEM **nativa de la nube** desarrollada por Google.

Permite recopilar, almacenar, analizar y buscar grandes cantidades de registros para identificar posibles amenazas, riesgos y vulnerabilidades.

Los analistas pueden realizar búsquedas utilizando diferentes elementos, como:

* Recursos específicos.
* Nombres de dominio.
* Usuarios.
* Direcciones IP.

Chronicle también proporciona diferentes paneles para supervisar registros, crear filtros y alertas y realizar seguimiento de actividades sospechosas.

## Paneles principales de Chronicle

### Panel de estadísticas empresariales

Muestra alertas recientes e identifica posibles **Indicadores de Compromiso (IOC)**, como nombres de dominio sospechosos.

Los resultados incluyen información como:

* **Puntuación de confianza:** indica la probabilidad de que la actividad represente una amenaza.
* **Nivel de gravedad:** indica la importancia de la amenaza para la organización.

Puede utilizarse para detectar accesos sospechosos a recursos críticos desde ubicaciones o dispositivos poco habituales.

### Panel de ingestión de datos y estado

Permite supervisar la **recepción y procesamiento de los registros** en Chronicle.

Muestra información como:

* Cantidad de registros recibidos.
* Fuentes de los registros.
* Tasas de éxito del procesamiento.

Su objetivo es comprobar que las fuentes de registros estén correctamente configuradas y que los datos lleguen sin errores.

### Panel de coincidencias de IOC

Permite observar las principales amenazas y los **Indicadores de Compromiso (IOC)** detectados.

Los analistas pueden supervisar dominios, direcciones IP y otros indicadores a lo largo del tiempo para identificar tendencias y priorizar las amenazas más importantes.

Por ejemplo, puede utilizarse para investigar actividades relacionadas con una alerta, como un inicio de sesión sospechoso desde una ubicación geográfica inusual.

### Panel principal

Proporciona una **visión general de la actividad de seguridad** de la organización.

Incluye información relacionada con:

* Ingestión de datos.
* Alertas.
* Eventos.
* Tendencias a lo largo del tiempo.

También permite visualizar cronologías de eventos, como un aumento repentino de intentos fallidos de inicio de sesión.

### Panel de detecciones de reglas

Muestra estadísticas relacionadas con las **detecciones e incidentes de seguridad** generados por las reglas de detección.

Los analistas pueden consultar las alertas activadas por una regla específica. Por ejemplo, una regla podría generar una alerta cuando un usuario abre un archivo adjunto malicioso conocido.

Esta información ayuda a identificar incidentes recurrentes y establecer medidas de mitigación.

### Panel general de inicio de sesión de usuarios

Permite analizar el **comportamiento de acceso de los usuarios** dentro de la organización.

Los analistas pueden revisar los eventos de inicio de sesión para detectar comportamientos anómalos, como un mismo usuario iniciando sesión desde diferentes ubicaciones geográficas al mismo tiempo.

Esta información puede utilizarse para detectar y mitigar amenazas relacionadas con cuentas de usuario y aplicaciones.

---

# Comparación general

| Herramienta                   | Característica principal                                                             |
| ----------------------------- | ------------------------------------------------------------------------------------ |
| **Splunk**                    | Recopilación, búsqueda, análisis y visualización de datos mediante múltiples paneles |
| **Chronicle / Google SecOps** | SIEM nativo de la nube orientado al análisis de grandes cantidades de registros      |
| **Splunk Enterprise**         | Solución SIEM orientada a infraestructura empresarial                                |
| **Splunk Cloud**              | Versión de Splunk alojada en la nube                                                 |
| **Chronicle**                 | Análisis de registros, IOC, alertas, detecciones y actividad de usuarios             |

## Conceptos clave

* **SIEM:** sistema que recopila y analiza registros para detectar amenazas.
* **SOC:** Centro de Operaciones de Seguridad encargado de supervisar y responder ante incidentes.
* **IOC:** Indicador de Compromiso, como una IP, dominio o archivo asociado a una posible amenaza.
* **Ingestión de datos:** proceso mediante el cual los registros son recibidos y procesados por el SIEM.
* **Regla de detección:** condición configurada para identificar una actividad potencialmente maliciosa.
* **Panel de control (Dashboard):** interfaz que permite visualizar y analizar información de seguridad.

**Idea principal:** Splunk y Chronicle proporcionan herramientas para **centralizar, visualizar y analizar registros de seguridad**, ayudando a los analistas a detectar amenazas, investigar incidentes, identificar tendencias y priorizar los riesgos de una organización.
