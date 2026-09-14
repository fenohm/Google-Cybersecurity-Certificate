# 🌐 Traducción de direcciones y protocolos de red

En una red, los dispositivos utilizan **direcciones IP y MAC** para identificarse y comunicarse. Además, existen distintos protocolos encargados de asignar direcciones, traducirlas, establecer conexiones remotas y gestionar el correo electrónico.

## 🔄 NAT — Network Address Translation

**NAT** permite que varios dispositivos de una red privada compartan una única **dirección IP pública** para comunicarse con Internet.

El router reemplaza la IP privada de origen por su IP pública al enviar tráfico a Internet y realiza el proceso inverso cuando recibe las respuestas.

### IP privadas

Son utilizadas dentro de redes locales y **no son únicas en Internet**.

Rangos privados:

```text
10.0.0.0     – 10.255.255.255
172.16.0.0  – 172.31.255.255
192.168.0.0  – 192.168.255.255
```

### IP públicas

Son direcciones **únicas globalmente** utilizadas para identificar redes o dispositivos en Internet. Generalmente son asignadas por un **ISP**.

> 💡 NAT permite conservar direcciones IPv4 públicas al permitir que múltiples dispositivos privados compartan una misma IP pública.

---

## 📡 DHCP — Dynamic Host Configuration Protocol

DHCP es un protocolo de gestión que configura automáticamente los dispositivos de una red.

Puede proporcionar:

* Dirección IP.
* Máscara de subred.
* Puerta de enlace predeterminada.
* Dirección del servidor DNS.

### Puertos

| Componente    | Puerto     |
| ------------- | ---------- |
| Servidor DHCP | **UDP 67** |
| Cliente DHCP  | **UDP 68** |

---

## 🔎 ARP — Address Resolution Protocol

ARP permite encontrar la **dirección MAC asociada a una dirección IP** dentro de una red local.

Ejemplo:

```text
IP: 192.168.1.10
        ↓ ARP
MAC: AA:BB:CC:DD:EE:FF
```

Los dispositivos mantienen esta información en una **caché ARP**.

* Opera principalmente en la capa de acceso a la red.
* **No utiliza puertos**, ya que los números de puerto pertenecen a protocolos de capas superiores.

---

## 💻 Telnet

Telnet permite conectarse y administrar un sistema remoto mediante línea de comandos.

Sin embargo, transmite la información **en texto claro**, por lo que no es adecuado para conexiones seguras.

* **Puerto:** TCP 23
* **Capa:** Aplicación
* **Problema:** No cifra la comunicación.
* **Alternativa segura:** SSH.

---

## 🔐 SSH — Secure Shell

SSH permite establecer conexiones remotas **seguras y cifradas**.

Se utiliza frecuentemente para administrar servidores y dispositivos de red.

* **Puerto:** TCP 22
* **Capa:** Aplicación
* Proporciona autenticación segura.
* Cifra la comunicación.
* Es la alternativa recomendada frente a Telnet.

---

# 📧 Protocolos de correo electrónico

## 📥 POP3 — Post Office Protocol

POP3 permite **descargar correos electrónicos desde un servidor hacia un dispositivo local**.

Una característica importante es que los mensajes pueden almacenarse localmente y, dependiendo de la configuración, eliminarse del servidor.

| Tipo             |          Puerto |
| ---------------- | --------------: |
| POP3 sin cifrado | TCP/UDP **110** |
| POP3 con SSL/TLS | TCP/UDP **995** |

### POP3 vs. múltiples dispositivos

POP3 no está diseñado principalmente para mantener los mensajes sincronizados entre varios dispositivos, ya que el correo puede descargarse y almacenarse localmente.

---

## 📥 IMAP — Internet Message Access Protocol

IMAP también permite acceder al correo entrante, pero mantiene los mensajes **almacenados en el servidor**.

Esto permite:

* Acceder al correo desde varios dispositivos.
* Mantener los mensajes sincronizados.
* Leer parcialmente los mensajes mientras se descargan.

| Tipo             |      Puerto |
| ---------------- | ----------: |
| IMAP sin cifrado | TCP **143** |
| IMAP con TLS     | TCP **993** |

### POP3 vs. IMAP

```text
POP3 → Descarga principalmente el correo al dispositivo
IMAP → Mantiene el correo sincronizado con el servidor
```

---

## 📤 SMTP — Simple Mail Transfer Protocol

SMTP se utiliza para **enviar y transmitir correos electrónicos** desde el remitente hasta el servidor o destinatario correspondiente.

También trabaja junto con DNS para localizar los servidores de correo del dominio de destino.

| Tipo         |          Puerto |
| ------------ | --------------: |
| SMTP         |  TCP/UDP **25** |
| SMTP con TLS | TCP/UDP **587** |

El puerto **25** se utiliza habitualmente para la transferencia entre servidores de correo y puede ser objeto de restricciones para reducir el spam.

---

# 🧱 Protocolos y puertos

Los **puertos** permiten que los dispositivos determinen qué servicio debe procesar la información recibida.

Los firewalls pueden utilizar los puertos para **permitir o bloquear tráfico**.

Ejemplo:

```text
Firewall
   │
   ├── TCP 22  → SSH       ✅ Permitir
   ├── TCP 23  → Telnet    ❌ Bloquear
   └── TCP 443 → HTTPS     ✅ Permitir
```

Por esto, conocer protocolos y puertos es fundamental para un analista de ciberseguridad.

---

# 📋 Tabla de referencia

| Protocolo      | Función                                   | Puerto(s) |
| -------------- | ----------------------------------------- | --------- |
| **NAT**        | Traducción de IP privada ↔ pública        | —         |
| **DHCP**       | Asignación automática de configuración IP | UDP 67/68 |
| **ARP**        | IP → dirección MAC                        | —         |
| **Telnet**     | Administración remota sin cifrado         | TCP 23    |
| **SSH**        | Administración remota segura              | TCP 22    |
| **POP3**       | Recepción/descarga de correo              | TCP 110   |
| **POP3S**      | POP3 cifrado                              | TCP 995   |
| **IMAP**       | Correo sincronizado con servidor          | TCP 143   |
| **IMAPS**      | IMAP cifrado                              | TCP 993   |
| **SMTP**       | Envío de correo                           | TCP 25    |
| **SMTP + TLS** | Envío de correo cifrado                   | TCP 587   |

## 🛡️ Importancia para la ciberseguridad

Como analista de ciberseguridad, conocer estos protocolos permite:

* Identificar servicios activos en una red.
* Analizar tráfico de red.
* Configurar reglas de firewall.
* Detectar protocolos inseguros.
* Identificar posibles vectores de ataque.
* Comprender conexiones entre dispositivos.
* Realizar troubleshooting de red.
* Reconocer rápidamente servicios mediante sus puertos.

### 🧠 Conceptos clave

```text
NAT    → IP privada ↔ IP pública
DHCP   → Asigna configuración IP automáticamente
ARP    → IP → MAC
Telnet → Administración remota sin cifrado
SSH    → Administración remota segura
POP3   → Descarga correo
IMAP   → Sincroniza correo con el servidor
SMTP   → Envía correo
```

> **Punto clave:** Un analista no solo debe memorizar los puertos, sino comprender **qué función cumple cada protocolo, en qué capa opera y qué implicaciones de seguridad tiene**.
