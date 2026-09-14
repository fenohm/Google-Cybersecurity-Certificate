# Operaciones en la capa de red

## 📌 Resumen

La **capa de red** se encarga del direccionamiento y la entrega de paquetes desde un dispositivo de origen hasta un dispositivo de destino. Los **routers** utilizan las direcciones IP incluidas en los encabezados de los paquetes para determinar hacia qué red deben reenviarlos.

Cada paquete IP contiene información importante para el enrutamiento, como:

- Dirección IP de origen.
- Dirección IP de destino.
- Tamaño del paquete.
- Protocolo utilizado para transportar los datos.
- Información relacionada con la fragmentación y el tiempo de vida del paquete.

Los paquetes utilizados con **TCP** suelen denominarse paquetes IP, mientras que los utilizados con **UDP** también pueden denominarse datagramas.

## 📦 Formato de un paquete IPv4

Un paquete IPv4 está compuesto por dos partes principales:

1. **Encabezado:** contiene la información necesaria para el direccionamiento y enrutamiento.
2. **Datos:** contiene la información que se está transmitiendo, como contenido web o correos electrónicos.

El encabezado IPv4 tiene un tamaño de entre **20 y 60 bytes**, mientras que el tamaño máximo de un paquete IPv4 completo es de **65.535 bytes**.

### Campos del encabezado IPv4

El encabezado IPv4 contiene **13 campos principales**:

- **Versión (VER):** indica qué versión del protocolo IP se está utilizando.
- **Longitud del encabezado (IHL/HLEN):** indica el tamaño del encabezado y dónde comienzan los datos.
- **Tipo de servicio (ToS):** proporciona información utilizada para determinar la prioridad y calidad del servicio.
- **Longitud total:** indica el tamaño completo del paquete, incluyendo encabezado y datos.
- **Identificación:** identifica los fragmentos pertenecientes a un mismo paquete original.
- **Banderas (Flags):** proporcionan información relacionada con la fragmentación del paquete.
- **Desplazamiento de fragmentación:** indica la posición que ocupa un fragmento dentro del paquete original.
- **TTL (Time To Live):** limita la cantidad de routers por los que puede pasar un paquete. Disminuye en cada router y, cuando llega a cero, el paquete es descartado.
- **Protocolo:** indica qué protocolo se utiliza para transportar los datos del paquete, como TCP o UDP.
- **Suma de comprobación del encabezado:** permite detectar errores o corrupción en el encabezado.
- **Dirección IP de origen:** identifica el dispositivo que envió el paquete.
- **Dirección IP de destino:** identifica el dispositivo o red a la que se dirige el paquete.
- **Opciones:** permite incluir funcionalidades adicionales en el paquete.

## ⏱️ TTL (Time To Live)

El **TTL** evita que los paquetes circulen indefinidamente por la red.

Cada vez que un paquete atraviesa un router, su valor TTL disminuye en **1**. Cuando alcanza **0**, el router descarta el paquete y puede enviar al origen un mensaje **ICMP Time Exceeded**.

Este mecanismo también es importante para herramientas de diagnóstico y para comprender cómo funciona el enrutamiento.

## 🌐 IPv4 vs. IPv6

**IPv6** fue desarrollado principalmente para solucionar el problema del agotamiento de direcciones IPv4 y mejorar determinados aspectos del funcionamiento de las redes.

| Característica | IPv4 | IPv6 |
|---|---|---|
| Tamaño de dirección | 32 bits (4 bytes) | 128 bits (16 bytes) |
| Formato | Decimal | Hexadecimal |
| Separador | `.` | `:` |
| Cantidad de direcciones | ~4.300 millones | ~340 undecillones |
| Ejemplo | `198.51.100.0` | `2002:0db8::ff21:0023:1234` |
| Encabezado | Más complejo | Más simplificado |
| Fragmentación | Incluye campos de fragmentación en el encabezado | Maneja la fragmentación de forma diferente |
| Campo destacado | TTL | Flow Label |

### 📍 Direcciones IPv4

Las direcciones IPv4 están formadas por **4 números decimales**, separados por puntos. Cada número puede tener un valor entre **0 y 255**.

Ejemplo:

`198.51.100.0`

IPv4 utiliza **32 bits**, lo que permite aproximadamente **4.300 millones de direcciones**.

### 📍 Direcciones IPv6

Las direcciones IPv6 utilizan **128 bits** y están formadas por grupos de números hexadecimales separados por dos puntos.

Ejemplo completo:

`2002:0db8:0000:0000:0000:ff21:0023:1234`

Los grupos consecutivos compuestos únicamente por ceros pueden abreviarse utilizando `::`.

Ejemplo:

`2002:0db8::ff21:0023:1234`

## 🔐 IPv6 y seguridad

IPv6 introduce mejoras relacionadas con el direccionamiento y el enrutamiento. Al disponer de un espacio de direcciones mucho mayor, reduce la necesidad de utilizar mecanismos como NAT para conservar direcciones IPv4.

También evita determinados problemas asociados con direcciones privadas duplicadas en redes IPv4.

Sin embargo, utilizar IPv6 no significa que una red sea automáticamente segura. Los dispositivos y controles de seguridad deben configurarse correctamente para proteger tanto el tráfico IPv4 como IPv6.

## 🛡️ Importancia para la ciberseguridad

El análisis de los campos de un paquete IP permite obtener información relevante para evaluar la seguridad de una comunicación.

Al analizar un paquete, un profesional de ciberseguridad puede determinar:

- **De dónde proviene** el paquete.
- **Hacia dónde se dirige**.
- **Qué protocolo** está utilizando.
- Si presenta indicios de fragmentación.
- Cuántos saltos puede realizar mediante el **TTL**.
- Si el encabezado presenta posibles errores o corrupción.

Comprender la estructura de los paquetes IP es fundamental para realizar **análisis de tráfico, detección de anomalías, troubleshooting e investigación de incidentes de seguridad**.

## 🎯 Puntos clave

> - La **capa de red** se encarga del direccionamiento y enrutamiento de paquetes.
> - Los **routers** utilizan las direcciones IP de destino para determinar hacia dónde enviar los paquetes.
> - Un paquete IPv4 contiene un **encabezado y una sección de datos**.
> - El encabezado IPv4 contiene información como IP de origen, IP de destino, TTL y protocolo.
> - El **TTL** evita que los paquetes circulen indefinidamente por la red.
> - IPv4 utiliza direcciones de **32 bits**, mientras que IPv6 utiliza direcciones de **128 bits**.
> - IPv6 proporciona un espacio de direccionamiento mucho mayor que IPv4.
> - IPv6 utiliza un encabezado más simplificado e incorpora el campo **Flow Label**.
> - Analizar los campos de un paquete IP permite obtener información importante para la **seguridad y el análisis de tráfico de red**.
