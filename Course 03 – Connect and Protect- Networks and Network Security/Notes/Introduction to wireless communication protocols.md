# 📡 Introducción a los protocolos de comunicación inalámbrica

**Wi-Fi** es el nombre utilizado para un conjunto de estándares que permiten la comunicación en **redes LAN inalámbricas (WLAN)**. Estos estándares pertenecen a la familia **IEEE 802.11**, desarrollada por el **IEEE (Institute of Electrical and Electronics Engineers)**.

Los protocolos de seguridad Wi-Fi han evolucionado con el objetivo de corregir vulnerabilidades y mejorar la protección de las comunicaciones inalámbricas.

## 🔐 Evolución de la seguridad Wi-Fi

```text
WEP → WPA → WPA2 → WPA3
```

Cada generación ha incorporado mejoras para solucionar las debilidades de la anterior.

---

## 1. ⚠️ WEP — Wired Equivalent Privacy

WEP fue desarrollado en **1999** y fue uno de los primeros estándares de seguridad inalámbrica.

Su objetivo era proporcionar a las redes Wi-Fi un nivel de privacidad similar al de las redes cableadas.

Actualmente **WEP se considera inseguro y obsoleto** porque su cifrado puede ser vulnerado mediante diferentes técnicas.

### Características

* Primer estándar de seguridad Wi-Fi ampliamente utilizado.
* Diseñado para proteger redes inalámbricas.
* Presenta vulnerabilidades graves.
* Puede ser atacado y descifrado relativamente fácilmente.
* **No debe utilizarse en redes modernas.**

---

## 2. 🔒 WPA — Wi-Fi Protected Access

WPA apareció en **2003** como una solución temporal para reemplazar WEP y permitir compatibilidad con hardware antiguo.

Una de sus principales mejoras fue **TKIP (Temporal Key Integrity Protocol)**.

También incorporó mecanismos para comprobar la integridad de los mensajes y detectar modificaciones o retransmisiones maliciosas.

### Vulnerabilidad KRACK

WPA puede verse afectado por **KRACK (Key Reinstallation Attack)**, un ataque que aprovecha el proceso de handshake para manipular la reinstalación de claves de cifrado.

Debido a sus vulnerabilidades, WPA fue posteriormente reemplazado por WPA2.

---

# 3. 🛡️ WPA2 — Wi-Fi Protected Access 2

WPA2 fue introducido en **2004** y mejoró considerablemente la seguridad de WPA.

Una de sus principales características fue la utilización de **AES (Advanced Encryption Standard)** junto con **CCMP**, proporcionando confidencialidad, autenticación e integridad de los mensajes.

### Características

* Utiliza **AES**.
* Utiliza **CCMP**.
* Mayor seguridad que WEP y WPA.
* Se convirtió en el estándar de seguridad Wi-Fi predominante.
* También puede verse afectado por ataques KRACK.

---

## 🏠 WPA2 Personal

Está diseñado principalmente para **redes domésticas**.

Utiliza una contraseña compartida que debe configurarse en los dispositivos que necesitan acceder a la red.

```text
Router Wi-Fi
     │
     ├── Contraseña compartida
     │
     ├── PC
     ├── Smartphone
     └── Notebook
```

### Ventajas

* Fácil de configurar.
* Adecuado para redes domésticas.
* No requiere una infraestructura de autenticación empresarial.

### Desventaja

La misma contraseña se comparte entre los usuarios/dispositivos, lo que dificulta administrar individualmente los permisos.

---

## 🏢 WPA2 Enterprise

Está diseñado para **organizaciones y redes empresariales**.

Permite una administración centralizada y un control individual del acceso de los usuarios.

### Ventajas

* Autenticación individual.
* Control centralizado.
* Permite revocar el acceso de usuarios.
* Mayor seguridad para organizaciones.
* Los usuarios no necesitan conocer directamente las claves de cifrado de la red.

Su implementación es más compleja que WPA2 Personal, pero resulta mucho más adecuada para entornos empresariales.

---

# 4. 🔐 WPA3 — Wi-Fi Protected Access 3

WPA3 fue introducido en **2018** como la evolución de WPA2.

Su objetivo es solucionar vulnerabilidades conocidas y proporcionar mecanismos de autenticación y cifrado más robustos.

### Principales mejoras

#### 🔑 SAE — Simultaneous Authentication of Equals

WPA3 utiliza **SAE** para el proceso de autenticación y establecimiento de claves.

Esto mejora la protección frente a ataques que intentan capturar tráfico inalámbrico y posteriormente descifrarlo.

#### 🛡️ Protección frente a KRACK

WPA3 incorpora mejoras destinadas a evitar los ataques de reinstalación de claves asociados al handshake de WPA2.

#### 🔐 Cifrado más fuerte

* WPA3 utiliza cifrado de **128 bits** en sus implementaciones habituales.
* **WPA3-Enterprise** puede utilizar un nivel de seguridad equivalente a **192 bits**.

---

# 📊 Comparación de protocolos Wi-Fi

| Protocolo |  Año | Seguridad        | Tecnología principal  | Estado                |
| --------- | ---: | ---------------- | --------------------- | --------------------- |
| **WEP**   | 1999 | ❌ Muy baja       | Cifrado WEP           | Obsoleto              |
| **WPA**   | 2003 | ⚠️ Mejor que WEP | TKIP                  | Obsoleto              |
| **WPA2**  | 2004 | ✅ Alta           | AES + CCMP            | Ampliamente utilizado |
| **WPA3**  | 2018 | 🟢 Muy alta      | SAE + cifrado moderno | Recomendado           |

### Evolución

```text
WEP
 │
 │ Vulnerabilidades graves
 ▼
WPA
 │
 │ Problemas como KRACK
 ▼
WPA2
 │
 │ Mejor seguridad, pero vulnerable a KRACK
 ▼
WPA3
 │
 ├── SAE
 ├── Mejor protección de autenticación
 └── Cifrado más robusto
```

---

# 🛡️ Importancia para la ciberseguridad

Como analista de ciberseguridad, es importante conocer la evolución de la seguridad inalámbrica para:

* Identificar protocolos Wi-Fi inseguros.
* Detectar redes que utilizan estándares obsoletos.
* Recomendar configuraciones de seguridad adecuadas.
* Comprender ataques contra redes inalámbricas.
* Diferenciar **WPA2 Personal** de **WPA2 Enterprise**.
* Comprender las mejoras introducidas por WPA3.
* Evaluar el nivel de seguridad de una WLAN.

## 📌 Puntos clave

* **Wi-Fi** se basa en los estándares **IEEE 802.11**.
* **WEP** está obsoleto y no debe utilizarse.
* **WPA** fue una solución temporal para reemplazar WEP.
* **WPA2** introdujo **AES y CCMP**, mejorando significativamente la seguridad.
* **WPA2 Personal** está orientado a redes domésticas.
* **WPA2 Enterprise** proporciona autenticación y administración centralizada.
* **WPA3** mejora la seguridad mediante **SAE** y mecanismos de cifrado más robustos.
* Como regla general, se debe utilizar **el estándar de seguridad más moderno compatible con los dispositivos de la red**.
