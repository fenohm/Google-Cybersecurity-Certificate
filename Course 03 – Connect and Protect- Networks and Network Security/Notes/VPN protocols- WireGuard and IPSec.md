# 🔐 Protocolos VPN: WireGuard e IPSec

Una **VPN (Virtual Private Network)** es una tecnología de seguridad que permite crear una conexión protegida a través de una red pública, como Internet.

Una VPN crea un **túnel virtual** entre dispositivos o redes, permitiendo proteger los datos en tránsito mediante **cifrado** y ocultando la dirección IP pública del cliente frente a los destinos a los que se conecta.

```text id="vpn-tunnel"
Dispositivo
    │
    │ Datos cifrados
    ▼
┌───────────┐
│    VPN    │
│  Túnel    │
└───────────┘
    │
    ▼
Servidor VPN / Internet
```

El **protocolo VPN** determina las reglas utilizadas para crear, mantener y proteger este túnel.

---

# 🌐 Tipos de VPN

Existen dos tipos principales de conexiones VPN:

## 💻 VPN de acceso remoto

Una **VPN de acceso remoto** conecta un dispositivo individual con un servidor o red VPN mediante Internet.

Es utilizada, por ejemplo, cuando un usuario necesita acceder de forma segura a recursos de una organización desde otra ubicación.

```text id="remote-vpn"
Usuario remoto
      │
      │ 🔐 Túnel cifrado
      ▼
    Internet
      │
      ▼
Servidor VPN
      │
      ▼
Red corporativa
```

### Características

* Conecta un **cliente individual** a una red o servidor VPN.
* Cifra los datos enviados y recibidos.
* Es común en el trabajo remoto.
* Generalmente es más sencilla de implementar que una VPN de sitio a sitio.

---

## 🏢 VPN de sitio a sitio

Una **VPN de sitio a sitio (Site-to-Site)** conecta dos o más redes completas mediante un túnel seguro.

Es utilizada principalmente por organizaciones con oficinas o sedes ubicadas en diferentes lugares.

```text id="site-to-site-vpn"
┌──────────────┐                 ┌──────────────┐
│  Oficina A   │                 │  Oficina B   │
│              │                 │              │
│ Red 10.0.0.0 │                 │ Red 192.168.1│
└──────┬───────┘                 └──────┬───────┘
       │                                │
       └──────── 🔐 VPN 🔐 ─────────────┘
                    Internet
```

### Características

* Conecta **redes completas**.
* Muy utilizada en entornos empresariales.
* Permite extender una red hacia otras ubicaciones.
* Suele utilizar protocolos como **IPSec**.
* Puede ser más compleja de configurar y administrar.

---

# ⚡ WireGuard

**WireGuard** es un protocolo VPN moderno diseñado para proporcionar **simplicidad, alto rendimiento y criptografía moderna**.

Puede utilizarse tanto para:

* VPN de acceso remoto.
* Conexiones cliente-servidor.
* VPN de sitio a sitio.

### Características principales

* 🚀 Alto rendimiento y baja sobrecarga.
* 🔐 Utiliza criptografía moderna.
* ⚙️ Diseño simple y relativamente fácil de configurar.
* 📦 Base de código más pequeña que muchas alternativas tradicionales.
* 🌍 Es de código abierto.
* 💻 Compatible con diferentes sistemas operativos.

WireGuard puede ser una buena opción cuando se necesita una conexión rápida, por ejemplo:

```text id="wireguard-use"
📺 Streaming
📁 Transferencia de archivos grandes
💻 Acceso remoto
🏢 Conexiones entre redes
```

---

# 🛡️ IPSec — Internet Protocol Security

**IPSec** es un conjunto de protocolos y estándares utilizados para proteger las comunicaciones a nivel IP.

Permite proporcionar principalmente:

* **Cifrado** de los datos.
* **Autenticación** de los extremos.
* **Integridad** de los paquetes.
* Protección de comunicaciones mediante túneles VPN.

IPSec es ampliamente utilizado y cuenta con una gran compatibilidad debido a su larga trayectoria y adopción.

```text id="ipsec-flow"
Red A
  │
  ▼
Gateway IPSec
  ║
  ║ 🔐 Túnel cifrado
  ║
  ▼
Gateway IPSec
  │
  ▼
Red B
```

### Características

* 🔒 Amplia adopción en entornos empresariales.
* 🌐 Compatible con numerosos sistemas y dispositivos.
* 🏢 Muy utilizado para VPN de sitio a sitio.
* 🧩 Ofrece múltiples opciones de configuración.
* ⚙️ Generalmente es más complejo de implementar que WireGuard.

---

# ⚖️ WireGuard vs. IPSec

| Característica          | WireGuard         | IPSec                              |
| ----------------------- | ----------------- | ---------------------------------- |
| Antigüedad              | Más reciente      | Más establecido                    |
| Configuración           | Más simple        | Más compleja                       |
| Rendimiento             | Generalmente alto | Depende de la implementación       |
| Código                  | Más reducido      | Más complejo                       |
| Código abierto          | Sí                | Existen múltiples implementaciones |
| Compatibilidad heredada | Puede ser menor   | Muy amplia                         |
| VPN sitio a sitio       | Sí                | Sí, muy utilizado                  |
| Acceso remoto           | Sí                | Sí                                 |
| Uso empresarial         | En crecimiento    | Muy consolidado                    |

## 🔄 Comparación rápida

```text id="comparison-vpn"
WireGuard
   │
   ├── Moderno
   ├── Simple
   ├── Alto rendimiento
   └── Criptografía moderna

IPSec
   │
   ├── Amplia compatibilidad
   ├── Muy utilizado
   ├── Maduro y consolidado
   └── Mayor complejidad
```

---

# 🎯 ¿Cuál utilizar?

La elección depende de factores como:

* Requisitos de seguridad.
* Infraestructura existente.
* Compatibilidad con dispositivos.
* Rendimiento necesario.
* Facilidad de administración.
* Tipo de conexión VPN.

```text id="choice-vpn"
¿Necesitas simplicidad y alto rendimiento?
            │
            ▼
        WireGuard

¿Necesitas amplia compatibilidad e integración
con infraestructura empresarial existente?
            │
            ▼
          IPSec
```

---

# 🛡️ Importancia para la ciberseguridad

Las VPN permiten establecer conexiones protegidas incluso cuando los datos deben viajar a través de redes no confiables.

Como analista de ciberseguridad, es importante comprender:

* La diferencia entre una **VPN de acceso remoto** y una **VPN de sitio a sitio**.
* Cómo funciona un **túnel VPN**.
* La importancia del **cifrado de datos en tránsito**.
* Las diferencias entre protocolos VPN.
* Las ventajas y limitaciones de **WireGuard e IPSec**.
* La importancia de la autenticación y configuración segura de los puntos finales.

## 📌 Puntos clave

* Una **VPN** crea una conexión protegida a través de una red pública.
* Los protocolos VPN determinan cómo se establece y protege el túnel.
* Una **VPN de acceso remoto** conecta un usuario individual con una red o servidor.
* Una **VPN de sitio a sitio** conecta redes completas.
* **WireGuard** es un protocolo moderno, simple y orientado al alto rendimiento.
* **IPSec** es una tecnología ampliamente adoptada y común en infraestructuras empresariales.
* IPSec suele utilizarse frecuentemente en conexiones **Site-to-Site**.
* La elección entre WireGuard e IPSec depende de la compatibilidad, rendimiento, infraestructura y necesidades de seguridad.
