# 🛡️ Aplicaciones de seguridad de red

La **seguridad de red** busca proteger los sistemas mediante múltiples capas de defensa. Este enfoque se conoce como **defensa en profundidad (Defense in Depth)**.

La idea principal es que ninguna herramienta de seguridad es suficiente por sí sola. La combinación de diferentes tecnologías permite detectar, bloquear y analizar amenazas desde distintos puntos de la red.

Las principales herramientas estudiadas son:

* 🔥 **Firewall**
* 🚨 **IDS (Intrusion Detection System)**
* 🛡️ **IPS (Intrusion Prevention System)**
* 📦 **Full Packet Capture**
* 📊 **SIEM (Security Information and Event Management)**

---

# 🔥 Firewall

Un **firewall** controla el tráfico que entra o sale de una red mediante un conjunto de reglas.

Puede permitir o bloquear paquetes basándose en información como:

* Dirección IP.
* Puerto.
* Protocolo.
* Estado de la conexión.
* Contenido del paquete, en el caso de algunos NGFW.

```text
Internet
   │
   ▼
┌─────────────┐
│  Firewall   │
└─────────────┘
   │
   ▼
Red interna
```

Los **NGFW (Next-Generation Firewalls)** pueden realizar una inspección más avanzada, incluyendo el análisis de la carga útil y del tráfico de aplicaciones.

### ⚠️ Limitación

Los firewalls tradicionales pueden depender principalmente de la información disponible en la cabecera del paquete y de las reglas configuradas.

---

# 🚨 IDS — Intrusion Detection System

Un **IDS (Sistema de Detección de Intrusiones)** monitoriza el tráfico y busca indicios de actividad maliciosa.

Puede detectar:

* Firmas de ataques conocidos.
* Patrones sospechosos.
* Anomalías de tráfico.
* Actividades potencialmente maliciosas.

Cuando encuentra algo sospechoso, **genera una alerta para los administradores o analistas**.

```text
Internet
   │
   ▼
┌─────────────┐
│  Firewall   │
└─────────────┘
   │
   ▼
┌─────────────┐
│     IDS     │ ─────► 🚨 Alerta
└─────────────┘
   │
   ▼
Red interna
```

### ⚠️ Limitaciones

* Puede no detectar ataques nuevos o sofisticados.
* Puede generar **falsos positivos**.
* No bloquea directamente el tráfico malicioso.

> 📌 **IDS = Detecta y alerta.**

---

# 🛡️ IPS — Intrusion Prevention System

Un **IPS (Sistema de Prevención de Intrusiones)** también analiza el tráfico en busca de ataques y anomalías, pero además **puede actuar automáticamente para detenerlos**.

Puede:

* Bloquear una dirección de origen.
* Descartar paquetes sospechosos.
* Interrumpir conexiones.
* Generar alertas.
* Detectar firmas de ataques conocidos.
* Identificar determinadas anomalías.

```text
Internet
   │
   ▼
┌─────────────┐
│  Firewall   │
└─────────────┘
   │
   ▼
┌─────────────┐
│     IPS     │
└─────────────┘
   │
   ├────► ❌ Tráfico malicioso bloqueado
   │
   ▼
Red interna
```

### ⚠️ Limitaciones

El IPS normalmente funciona **en línea (inline)**. Si el dispositivo falla, puede interrumpir la comunicación entre Internet y la red interna.

También existe el riesgo de **falsos positivos**, donde tráfico legítimo puede ser bloqueado accidentalmente.

> 📌 **IPS = Detecta, alerta y actúa.**

---

# 🔍 IDS vs IPS

| Característica                        | IDS             | IPS   |
| ------------------------------------- | --------------- | ----- |
| Detecta amenazas                      | ✅               | ✅     |
| Genera alertas                        | ✅               | ✅     |
| Analiza tráfico                       | ✅               | ✅     |
| Bloquea tráfico                       | ❌               | ✅     |
| Puede generar falsos positivos        | ✅               | ✅     |
| Funciona de forma pasiva              | Generalmente    | ❌     |
| Puede interrumpir conexiones si falla | No directamente | ⚠️ Sí |

### 🧠 Regla fácil de recordar

```text
IDS → "¡Encontré algo sospechoso!"
IPS → "¡Encontré algo sospechoso y lo bloqueé!"
```

---

# 📦 Full Packet Capture

Los dispositivos de **captura completa de paquetes** permiten almacenar y analizar grandes cantidades de tráfico de red.

Son especialmente útiles para:

* Investigaciones de seguridad.
* Análisis forense.
* Investigar alertas de IDS.
* Reconstruir comunicaciones.
* Analizar incidentes.

```text
Tráfico de red
      │
      ▼
┌─────────────────┐
│ Packet Capture  │
└─────────────────┘
      │
      ▼
Datos almacenados
      │
      ▼
Análisis / Forense
```

A diferencia de una simple alerta, la captura completa puede proporcionar información detallada sobre lo que ocurrió durante una comunicación.

---

# 📊 SIEM

Un **SIEM (Security Information and Event Management)** es una plataforma que **recopila, centraliza y analiza registros y eventos de seguridad** provenientes de diferentes sistemas.

Puede recibir información desde:

```text
Firewall ──────┐
IDS ───────────┤
IPS ───────────┤
VPN ───────────┼──► SIEM ──► SOC
Proxy ─────────┤
DNS ───────────┤
Servidores ────┘
```

El SIEM proporciona una **vista centralizada de los eventos de seguridad**, permitiendo a los analistas investigar actividades sospechosas desde un único lugar.

### Funciones principales

* 📥 Recopilación de logs.
* 🔎 Análisis de eventos.
* 🚨 Detección de actividad sospechosa.
* 📊 Visualización mediante dashboards.
* 🔗 Correlación de eventos.
* 🕵️ Apoyo a investigaciones de seguridad.

Este concepto suele describirse como **"single pane of glass"**, es decir, un único panel desde el cual los analistas pueden observar múltiples fuentes de información.

### Ejemplos

* **Google Chronicle**
* **Splunk Enterprise**
* **Splunk Cloud**

> 📌 Un SIEM **no reemplaza al analista**. Proporciona información que debe ser interpretada para determinar si un evento representa realmente una amenaza y cómo responder.

---

# 🏗️ Defensa en profundidad

Una organización puede combinar todas estas herramientas para crear diferentes capas de protección.

```text
                  INTERNET
                     │
                     ▼
              ┌─────────────┐
              │  Firewall   │
              └─────────────┘
                     │
                     ▼
              ┌─────────────┐
              │     IDS     │
              └─────────────┘
                     │
                     ▼
              ┌─────────────┐
              │     IPS     │
              └─────────────┘
                     │
                     ▼
                RED INTERNA
                     │
          ┌──────────┴──────────┐
          ▼                     ▼
   Packet Capture              SIEM
          │                     │
          └──────────┬──────────┘
                     ▼
                    SOC
```

Cada capa tiene una función diferente:

```text
Firewall       → Controlar tráfico
IDS            → Detectar y alertar
IPS            → Detectar y bloquear
Packet Capture → Registrar e investigar
SIEM           → Centralizar y correlacionar
SOC            → Analizar y responder
```

---

# 💰 Costes y gestión

Implementar múltiples capas de seguridad también implica costes.

Una organización debe considerar:

* 💵 Coste de adquisición.
* ⚙️ Instalación y configuración.
* 🔧 Mantenimiento.
* 👨‍💻 Personal especializado.
* 📊 Infraestructura para almacenar logs.
* 🚨 Monitorización continua.

Por esta razón, los responsables de seguridad deben determinar el **nivel adecuado de protección según el riesgo y los recursos disponibles**.

---

# 📌 Comparación general

| Herramienta        | Función principal               | ¿Bloquea amenazas? |
| ------------------ | ------------------------------- | -----------------: |
| **Firewall**       | Filtrar tráfico mediante reglas |                  ✅ |
| **IDS**            | Detectar y alertar              |                  ❌ |
| **IPS**            | Detectar y prevenir             |                  ✅ |
| **Packet Capture** | Registrar y analizar tráfico    |                  ❌ |
| **SIEM**           | Centralizar y analizar eventos  |                  ❌ |

---

# 🧠 Puntos clave

* La **defensa en profundidad** utiliza múltiples capas de seguridad para proteger una red.
* Un **firewall** controla el tráfico mediante reglas.
* Un **IDS** detecta actividad sospechosa y genera alertas.
* Un **IPS** detecta amenazas y puede bloquearlas automáticamente.
* La **captura completa de paquetes** permite realizar análisis detallados e investigaciones forenses.
* Un **SIEM** centraliza logs y eventos provenientes de diferentes dispositivos y sistemas.
* El **SOC** utiliza estas herramientas para monitorizar, investigar y responder ante incidentes.
* Ninguna herramienta sustituye completamente al analista de seguridad.
* La implementación de estas tecnologías debe equilibrar **riesgo, nivel de protección y costes**.

### 🔑 Concepto fundamental

> **La seguridad efectiva no depende de una única herramienta, sino de la combinación de múltiples capas de protección, detección, prevención, monitorización y análisis.**
