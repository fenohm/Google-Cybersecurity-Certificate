# 🕵️ Analizadores de protocolos de red y tcpdump

Un **analizador de protocolos de red** es una herramienta utilizada para **capturar, inspeccionar y analizar el tráfico de una red**.

También se les conoce como:

* **Packet sniffer**
* **Packet analyzer**
* **Network protocol analyzer**

Estas herramientas son fundamentales para monitorizar redes, solucionar problemas e identificar actividades sospechosas.

### 🔧 Ejemplos de analizadores

* SolarWinds NetFlow Traffic Analyzer
* ManageEngine OpManager
* Azure Network Watcher
* **Wireshark**
* **tcpdump**

---

# 🐧 tcpdump

**tcpdump** es un analizador de protocolos de red basado en línea de comandos.

Características principales:

* 💻 Funciona desde la terminal.
* 🪶 Es ligero y consume pocos recursos.
* 🐧 Está disponible en Linux/Unix.
* 🍎 También puede utilizarse en macOS.
* 📦 Utiliza la biblioteca **libpcap**.
* 🔎 Permite capturar y analizar paquetes de red.

tcpdump muestra información relevante de los paquetes directamente en la terminal.

```text id="7vqfbr"
Paquete
   │
   ├── Timestamp
   ├── IP origen
   ├── Puerto origen
   ├── IP destino
   └── Puerto destino
```

---

# 📊 Interpretación de una captura tcpdump

Una captura de paquetes puede proporcionar información importante sobre las comunicaciones de una red.

| Información           | Descripción                                    |
| --------------------- | ---------------------------------------------- |
| **Timestamp**         | Momento en que se capturó el paquete.          |
| **IP de origen**      | Dispositivo que envió el paquete.              |
| **Puerto de origen**  | Puerto desde donde se originó la comunicación. |
| **IP de destino**     | Dispositivo que recibe el paquete.             |
| **Puerto de destino** | Servicio al que se dirige el paquete.          |

### Ejemplo conceptual

```text id="v9k2sd"
12:30:15.123456
192.168.1.10:52341 → 192.168.1.1:53
```

Interpretación:

```text
Timestamp    → 12:30:15.123456
IP origen    → 192.168.1.10
Puerto origen → 52341
IP destino   → 192.168.1.1
Puerto destino → 53 (DNS)
```

> 💡 Por defecto, tcpdump puede intentar resolver direcciones IP en nombres de host y números de puerto en nombres de servicios conocidos.

---

# 🛠️ Usos de tcpdump

Los analizadores de protocolos pueden utilizarse para:

### 📈 Establecer una línea base

Permiten conocer cuáles son los **patrones normales de tráfico** de una red.

### 🔎 Detectar tráfico malicioso

El análisis de paquetes puede ayudar a identificar:

* Tráfico anómalo.
* Comunicaciones sospechosas.
* Escaneos de red.
* Intentos de ataque.
* Posibles ataques DoS.

### 🚨 Generar alertas

Los datos obtenidos pueden utilizarse para crear mecanismos que notifiquen a los administradores cuando se detectan comportamientos sospechosos.

### 📡 Detectar dispositivos no autorizados

También pueden ayudar a identificar:

* Puntos de acceso inalámbricos no autorizados.
* Tráfico inesperado.
* Servicios desconocidos.
* Comunicaciones no permitidas.

### 🔧 Solucionar problemas

tcpdump también es útil para **diagnosticar problemas de conectividad y rendimiento**.

---

# ⚠️ Uso malicioso

Los analizadores de protocolos también pueden ser utilizados por atacantes.

Un atacante que consiga acceso a una red podría capturar paquetes para obtener información sensible, especialmente si la comunicación **no está cifrada**.

```text id="h8y5xc"
Red
 │
 ├── Usuario → Servidor
 │       │
 │       └────► 🕵️ Atacante
 │                 │
 │                 ▼
 │            Packet Sniffing
 │                 │
 │                 ▼
 │          Información capturada
```

La información potencialmente expuesta puede incluir:

* Nombres de usuario.
* Contraseñas.
* Direcciones IP.
* Puertos.
* Información de servicios.
* Datos transmitidos sin cifrado.

Por este motivo, los protocolos seguros como **HTTPS, SSH y TLS** son importantes para proteger la información en tránsito.

---

# 💻 Comandos básicos de tcpdump

Algunos comandos útiles para familiarizarse con tcpdump:

```bash id="0h0a4m"
sudo tcpdump
```

Captura el tráfico de la interfaz seleccionada.

```bash id="5c1xqk"
sudo tcpdump -i eth0
```

Captura tráfico de una interfaz específica.

```bash id="8p2y1d"
sudo tcpdump -i any
```

Captura tráfico de todas las interfaces disponibles, cuando el sistema lo permite.

```bash id="c4w6nm"
sudo tcpdump -n
```

Evita la resolución de nombres, mostrando directamente las direcciones IP y puertos numéricos.

```bash id="z6m3jr"
sudo tcpdump -c 20
```

Captura únicamente 20 paquetes.

> 🔐 En un entorno de laboratorio, estas opciones son especialmente útiles para aprender a reconocer patrones normales y anómalos de tráfico.

---

# 🛡️ Importancia para la ciberseguridad

Como analista de ciberseguridad, comprender los analizadores de protocolos permite **observar lo que realmente está ocurriendo dentro de una red**.

```text id="8d2v3f"
Capturar
    ↓
Analizar
    ↓
Identificar patrones
    ↓
Detectar anomalías
    ↓
Investigar amenazas
```

Estas herramientas pueden ser utilizadas tanto para **defensa y diagnóstico** como para actividades maliciosas, por lo que es importante comprender sus capacidades y los riesgos asociados.

## 📌 Puntos clave

* Un **packet analyzer** captura e inspecciona tráfico de red.
* **tcpdump** es un analizador ligero basado en línea de comandos.
* Utiliza **libpcap** para la captura de paquetes.
* Está ampliamente disponible en sistemas **Linux/Unix y macOS**.
* Una captura tcpdump puede mostrar **timestamp, IPs y puertos de origen y destino**.
* Es útil para **troubleshooting, establecer líneas base y detectar tráfico sospechoso**.
* Los atacantes también pueden utilizar packet sniffers para capturar información sensible.
* El **cifrado del tráfico** reduce el riesgo de que la información capturada pueda ser utilizada por un atacante.
* Para un analista, tcpdump es una herramienta fundamental para comprender y analizar el **tráfico real de una red**.
