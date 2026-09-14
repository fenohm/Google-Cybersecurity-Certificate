# El Modelo OSI

## 📌 Resumen

El **Modelo OSI (Open Systems Interconnection)** es un modelo conceptual estandarizado que describe cómo los dispositivos se comunican y transmiten datos a través de una red. Está compuesto por **7 capas**, lo que permite comprender con mayor detalle los procesos que ocurren durante una comunicación de red.

El modelo OSI es una representación más detallada que el **Modelo TCP/IP**, que utiliza 4 capas. Ambos modelos son utilizados por profesionales de redes y ciberseguridad para comprender la comunicación, solucionar problemas e identificar posibles amenazas.

## 🌐 Las 7 capas del Modelo OSI

### 7. Capa de aplicación

Es la capa más cercana al usuario y contiene los protocolos que permiten a las aplicaciones acceder a los servicios de red.

Ejemplos:

- **HTTP/HTTPS:** comunicación entre navegadores y servidores web.
- **SMTP:** envío de correos electrónicos.
- **DNS:** traducción de nombres de dominio a direcciones IP.

### 6. Capa de presentación

Se encarga de preparar los datos para que puedan ser interpretados correctamente por las aplicaciones del sistema receptor.

Funciones principales:

- **Encriptación:** protege los datos durante la comunicación.
- **Compresión:** reduce el tamaño de los datos.
- **Traducción y formato:** adapta los datos a formatos que puedan ser interpretados por diferentes sistemas.

Un ejemplo relacionado con esta capa es **SSL**, utilizado como parte de las comunicaciones HTTPS.

### 5. Capa de sesión

Se encarga de establecer, mantener y finalizar las sesiones de comunicación entre dispositivos.

También puede encargarse de:

- Autenticación.
- Reconexión.
- Establecimiento de puntos de control.
- Recuperación de una transmisión después de una interrupción.

Los puntos de control permiten continuar una transmisión desde el último punto registrado en caso de que la conexión se interrumpa.

### 4. Capa de transporte

Se encarga de la entrega de datos entre dispositivos y del control de la transferencia.

Una de sus funciones principales es la **segmentación**, que consiste en dividir grandes cantidades de datos en segmentos más pequeños para facilitar su transmisión.

También controla:

- Velocidad de transferencia.
- Flujo de datos.
- Entrega de información.
- Reensamblaje de los segmentos en el destino.

Protocolos principales:

- **TCP:** proporciona una transmisión confiable y orientada a conexión.
- **UDP:** proporciona una transmisión rápida sin establecer una conexión.

### 3. Capa de red

Se encarga de determinar cómo los datos llegan desde una red de origen hasta una red de destino.

Los paquetes contienen **direcciones IP**, que permiten a los routers determinar hacia dónde deben ser enviados.

Funciones principales:

- Direccionamiento IP.
- Enrutamiento de paquetes.
- Comunicación entre diferentes redes.

### 2. Capa de enlace de datos

Se encarga de organizar el envío y recepción de datos dentro de una misma red.

En esta capa funcionan componentes como:

- **Switches** de una red local.
- **Tarjetas de interfaz de red (NIC)**.

Algunos protocolos relacionados con esta capa son:

- **NCP:** Network Control Protocol.
- **HDLC:** High-Level Data Link Control.
- **SDLC:** Synchronous Data Link Control.

### 1. Capa física

Es la capa encargada de la transmisión física de los datos. Incluye todos los componentes de hardware utilizados para transportar la información.

Ejemplos:

- Cables Ethernet.
- Cables coaxiales.
- Módems.
- Hubs.
- Cableado de red.

Los datos deben convertirse en señales representadas mediante **bits (0 y 1)** para poder transmitirse físicamente a través de los medios de comunicación.

## 🔄 Modelo OSI vs. Modelo TCP/IP

El Modelo OSI y el Modelo TCP/IP permiten comprender cómo se produce la comunicación entre dispositivos de una red.

| Modelo | Capas |
|---|---:|
| **OSI** | 7 |
| **TCP/IP** | 4 |

El **Modelo TCP/IP** combina varias funciones que en OSI están separadas:

| Modelo OSI | Modelo TCP/IP |
|---|---|
| Capa 7: Aplicación | Capa de aplicación |
| Capa 6: Presentación | Capa de aplicación |
| Capa 5: Sesión | Capa de aplicación |
| Capa 4: Transporte | Capa de transporte |
| Capa 3: Red | Capa de Internet |
| Capa 2: Enlace de datos | Capa de acceso a la red |
| Capa 1: Física | Capa de acceso a la red |

## 🔐 Importancia para la ciberseguridad

El Modelo OSI permite analizar una red de manera estructurada y determinar **en qué capa puede estar ocurriendo un problema, vulnerabilidad o ataque**.

Comprender sus capas ayuda a:

- Analizar problemas de conectividad.
- Identificar protocolos de red.
- Comprender el funcionamiento de dispositivos de red.
- Analizar el tráfico de red.
- Identificar posibles puntos de ataque.
- Comunicar de forma más precisa dónde ocurre un incidente de seguridad.

## 🎯 Puntos clave

> - El **Modelo OSI tiene 7 capas**.
> - Las capas OSI van desde la **capa física (1)** hasta la **capa de aplicación (7)**.
> - La **capa 1** se relaciona con el hardware y los medios físicos.
> - La **capa 2** gestiona la comunicación dentro de una red local.
> - La **capa 3** utiliza direcciones IP y se encarga del enrutamiento.
> - La **capa 4** controla la entrega y segmentación de los datos mediante TCP o UDP.
> - Las **capas 5, 6 y 7** gestionan sesiones, presentación de datos y servicios utilizados por las aplicaciones.
> - El Modelo TCP/IP simplifica varias de las funciones del Modelo OSI en sus 4 capas.
> - Conocer el Modelo OSI es fundamental para **analizar redes, solucionar problemas y detectar amenazas de seguridad**.
