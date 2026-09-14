# 🌐 Protocolos y herramientas de seguridad de red

Los **protocolos de red** son reglas que permiten a los dispositivos comunicarse y determinar cómo deben transmitirse los datos.

Se pueden dividir en tres categorías principales:

1. **Comunicación:** permiten establecer y mantener comunicaciones.
2. **Gestión:** permiten supervisar y solucionar problemas de red.
3. **Seguridad:** protegen los datos mediante mecanismos de cifrado y autenticación.

---

# 📡 Protocolos de red comunes

| Protocolo   | Categoría    | Función                                           |
| ----------- | ------------ | ------------------------------------------------- |
| **TCP**     | Comunicación | Transmisión confiable y orientada a conexión.     |
| **UDP**     | Comunicación | Transmisión rápida sin conexión previa.           |
| **SMTP**    | Comunicación | Envío de correo electrónico.                      |
| **HTTP**    | Comunicación | Comunicación entre navegadores y servidores web.  |
| **DNS**     | Comunicación | Traduce nombres de dominio a direcciones IP.      |
| **ICMP**    | Gestión      | Diagnóstico y notificación de errores de red.     |
| **ARP**     | Comunicación | Relaciona direcciones IP con direcciones MAC.     |
| **IPSec**   | Seguridad    | Protege comunicaciones mediante IP.               |
| **SSL/TLS** | Seguridad    | Cifra comunicaciones y protege datos en tránsito. |

### 🔎 Conceptos importantes

```text
DNS → Nombre de dominio → Dirección IP
ARP → Dirección IP → Dirección MAC
HTTP → Navegador ↔ Servidor web
ICMP → Diagnóstico de red
TCP → Comunicación confiable
UDP → Comunicación rápida
```

---

# 📶 Seguridad Wi-Fi

Los estándares de seguridad inalámbrica han evolucionado para corregir vulnerabilidades:

```text
WEP → WPA → WPA2 → WPA3
```

| Estándar | Seguridad   | Característica                           |
| -------- | ----------- | ---------------------------------------- |
| **WEP**  | ❌ Obsoleto  | Vulnerable y no recomendado.             |
| **WPA**  | ⚠️ Obsoleto | Introdujo TKIP como mejora frente a WEP. |
| **WPA2** | ✅ Alta      | Utiliza AES/CCMP.                        |
| **WPA3** | 🟢 Muy alta | Utiliza SAE y mejoras de seguridad.      |

### WPA2 y WPA3

Ambos pueden utilizarse en dos modalidades:

* **Personal:** recomendado para redes domésticas.
* **Enterprise:** diseñado para organizaciones y permite una gestión individualizada del acceso.

> 🔐 Siempre que sea posible, se debe utilizar el estándar de seguridad inalámbrica más moderno compatible con los dispositivos de la red.

---

# 🧱 Firewalls

Un **firewall** inspecciona y filtra el tráfico de red de acuerdo con reglas de seguridad.

Puede utilizar información como:

* Dirección IP.
* Número de puerto.
* Protocolo.
* Estado de la conexión.
* Aplicación.

## Firewall sin estado

Un firewall **stateless** toma decisiones basándose en reglas predefinidas.

No mantiene información sobre las conexiones anteriores.

```text
Paquete
   ↓
¿Cumple la regla?
   ├── Sí → Permitir
   └── No → Bloquear
```

## Firewall con estado

Un firewall **stateful** mantiene información sobre las conexiones mediante una **tabla de estado**.

Esto permite identificar si un paquete pertenece a una conexión existente.

```text
Cliente → Firewall → Servidor
           │
           └── Tabla de estado
                    ↓
          Identifica la conexión
```

Una ventaja es que puede permitir automáticamente el tráfico de respuesta asociado a una conexión previamente establecida.

---

# 🛡️ NGFW — Next-Generation Firewall

Los **firewalls de nueva generación (NGFW)** proporcionan capacidades más avanzadas que los firewalls tradicionales.

Entre sus características pueden encontrarse:

* **Deep Packet Inspection (DPI)**.
* Prevención y detección de intrusiones.
* Identificación de aplicaciones.
* Filtrado de URL.
* Filtrado DNS.
* Antivirus de red.
* Sandboxing.

A diferencia de un firewall tradicional, que puede tomar decisiones principalmente según **IP y puerto**, un NGFW puede analizar el tráfico a nivel de aplicación.

```text
Firewall tradicional
IP + Puerto → Permitir/Bloquear

        ↓

NGFW
IP + Puerto + Aplicación + Contenido
              ↓
        Permitir/Bloquear
```

---

# 🌐 Servidores Proxy

Un **proxy** actúa como intermediario entre un cliente y otro sistema.

## Forward Proxy

Un **proxy directo** gestiona las solicitudes de clientes internos hacia recursos externos.

```text
Cliente → Forward Proxy → Internet
```

Puede utilizarse para:

* Filtrar sitios web.
* Controlar el acceso a Internet.
* Aplicar políticas de seguridad.
* Bloquear recursos maliciosos.

## Reverse Proxy

Un **reverse proxy** funciona en sentido contrario y gestiona solicitudes provenientes de sistemas externos hacia servicios internos.

```text
Internet → Reverse Proxy → Servidor interno
```

Puede utilizarse como capa de protección y control frente a servicios expuestos a Internet.

---

# 🔐 VPN — Virtual Private Network

Una **VPN** crea una conexión protegida para transportar datos a través de una red pública.

Utiliza **encapsulación** para envolver los datos dentro de una comunicación protegida.

```text
Datos originales
      ↓
Encapsulación
      ↓
Paquete protegido
      ↓
Internet
      ↓
Servidor VPN
      ↓
Datos originales
```

Las VPN pueden utilizarse para:

* Proteger datos en tránsito.
* Conectar usuarios con recursos corporativos.
* Permitir acceso remoto seguro.
* Proteger comunicaciones en redes públicas.
* Ocultar la dirección IP frente a determinados servicios externos.

> ⚠️ Una VPN **no proporciona anonimato absoluto**. El proveedor de VPN puede potencialmente observar determinada actividad, por lo que es importante elegir proveedores confiables y revisar sus políticas de privacidad.

---

# 🌍 SD-WAN

**SD-WAN (Software-Defined Wide Area Network)** es una tecnología que permite gestionar y conectar redes distribuidas mediante software.

Las organizaciones pueden utilizar SD-WAN para conectar:

```text
                 ┌── Sede A
                 │
Usuarios ── SD-WAN ── Sede B
                 │
                 └── Sede C
                       │
                    Cloud
```

Permite conectar usuarios, aplicaciones y diferentes ubicaciones geográficas de forma centralizada y segura.

Las organizaciones pueden combinar **SD-WAN + VPN** para proteger las comunicaciones entre diferentes sedes y recursos corporativos.

---

# 🛡️ Importancia para la ciberseguridad

Un analista de ciberseguridad debe comprender estas tecnologías porque forman parte de las principales **capas de defensa de una red**.

```text
                 SEGURIDAD DE RED
                       │
       ┌───────────────┼───────────────┐
       ↓               ↓               ↓
   Protocolos       Firewall          VPN
       │               │               │
       ↓               ↓               ↓
 Comunicación     Filtrado        Cifrado
       │
       └───────────┐
                   ↓
               Proxy / NGFW
                   │
                   ↓
             Control y análisis
```

## 📌 Puntos clave

* Los **protocolos de red** establecen las reglas para la comunicación.
* **TCP y UDP** son protocolos fundamentales de transporte.
* **DNS** traduce nombres de dominio a IP.
* **ARP** relaciona IP con MAC dentro de una red local.
* **ICMP** se utiliza para diagnóstico y mensajes de error.
* **WPA2 y WPA3** son estándares importantes de seguridad Wi-Fi.
* Los **firewalls stateless** utilizan reglas sin mantener información de conexión.
* Los **firewalls stateful** mantienen una tabla de estado de las conexiones.
* Los **NGFW** pueden inspeccionar aplicaciones y contenido de los paquetes.
* Los **forward proxy** gestionan solicitudes de clientes internos hacia Internet.
* Los **reverse proxy** gestionan solicitudes externas hacia servicios internos.
* Las **VPN** protegen comunicaciones mediante cifrado y encapsulación.
* **SD-WAN** permite conectar y administrar redes distribuidas de forma centralizada.
