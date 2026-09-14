# 🌐 Visión general de los protocolos de red

Los **protocolos de red** son un conjunto de reglas que permiten que dos o más dispositivos se comuniquen correctamente. Definen cómo se estructuran, transmiten, reciben y procesan los datos dentro de una red.

Para un analista de ciberseguridad es fundamental comprender estos protocolos, ya que algunos pueden presentar **vulnerabilidades que son aprovechadas por actores maliciosos**. Por ejemplo, un ataque puede aprovechar DNS para redirigir a los usuarios desde un sitio legítimo hacia uno malicioso.

## 📡 Categorías de protocolos

Los protocolos de red pueden clasificarse principalmente en:

1. **Protocolos de comunicación**
2. **Protocolos de gestión**
3. **Protocolos de seguridad**

---

## 1. 📤 Protocolos de comunicación

Controlan el intercambio de información entre dispositivos y determinan cómo se transmiten los datos.

| Protocolo | Función                                                             | Puerto | Capa TCP/IP |
| --------- | ------------------------------------------------------------------- | -----: | ----------- |
| **TCP**   | Comunicación orientada a conexión y transmisión confiable de datos. |      — | Transporte  |
| **UDP**   | Transmisión rápida sin establecer conexión previa.                  |      — | Transporte  |
| **HTTP**  | Comunicación entre clientes y servidores web.                       |     80 | Aplicación  |
| **DNS**   | Traduce nombres de dominio a direcciones IP.                        |     53 | Aplicación  |

### TCP — Transmission Control Protocol

TCP establece una conexión antes de transmitir datos y garantiza una comunicación confiable.

Utiliza el **three-way handshake**:

```text
Cliente → SYN
Servidor → SYN/ACK
Cliente → ACK
```

Una vez completado el proceso, se establece la conexión TCP.

### UDP — User Datagram Protocol

UDP no establece una conexión antes de transmitir datos. Es menos confiable que TCP, pero ofrece menor latencia y mayor velocidad.

Un ejemplo de uso es la realización de consultas **DNS**.

### HTTP — Hypertext Transfer Protocol

HTTP permite la comunicación entre navegadores web y servidores.

* Puerto: **80**
* Capa: **Aplicación**
* No cifra la información transmitida.
* Actualmente suele ser reemplazado por HTTPS.

### DNS — Domain Name System

DNS traduce nombres de dominio, como:

```text
google.com
```

en direcciones IP:

```text
142.250.x.x
```

Normalmente utiliza **UDP/53**, aunque puede utilizar TCP cuando la respuesta es demasiado grande.

---

## 2. ⚙️ Protocolos de gestión

Se utilizan para **supervisar, administrar y diagnosticar** dispositivos y actividades dentro de una red.

| Protocolo | Función                                                    | Capa TCP/IP |
| --------- | ---------------------------------------------------------- | ----------- |
| **SNMP**  | Supervisar y administrar dispositivos de red.              | Aplicación  |
| **ICMP**  | Informar errores y diagnosticar problemas de conectividad. | Internet    |

### SNMP — Simple Network Management Protocol

SNMP permite monitorizar y administrar dispositivos de red.

Puede utilizarse para:

* Obtener información de dispositivos.
* Supervisar el uso de ancho de banda.
* Consultar el estado de equipos.
* Modificar determinadas configuraciones.

### ICMP — Internet Control Message Protocol

ICMP permite que los dispositivos informen sobre **errores o problemas relacionados con la transmisión de datos**.

Una de sus aplicaciones más conocidas es:

```bash
ping 8.8.8.8
```

El comando `ping` utiliza ICMP para comprobar conectividad y medir la latencia entre dispositivos.

---

## 3. 🔐 Protocolos de seguridad

Estos protocolos proporcionan mecanismos para proteger la información durante su transmisión, principalmente mediante **cifrado**.

| Protocolo | Función                           | Puerto | Capa TCP/IP |
| --------- | --------------------------------- | -----: | ----------- |
| **HTTPS** | Comunicación web cifrada.         |    443 | Aplicación  |
| **SFTP**  | Transferencia segura de archivos. |     22 | Aplicación  |

### HTTPS — Hypertext Transfer Protocol Secure

HTTPS es la versión segura de HTTP.

Utiliza **TLS** para proteger la comunicación entre el cliente y el servidor.

* Puerto: **443**
* Capa: **Aplicación**
* Protege los datos en tránsito frente a interceptaciones.

### SFTP — SSH File Transfer Protocol

SFTP permite transferir archivos de forma segura utilizando **SSH**.

* Normalmente utiliza **TCP/22**.
* Proporciona cifrado durante la transferencia.
* Puede utilizarse para subir y descargar archivos de sistemas remotos.

---

## 🛡️ Importancia para la ciberseguridad

Comprender los protocolos de red permite a un analista de ciberseguridad:

* Identificar tráfico normal y sospechoso.
* Detectar protocolos inseguros.
* Comprender posibles vectores de ataque.
* Analizar tráfico de red.
* Diagnosticar problemas de conectividad.
* Implementar medidas de protección.
* Reconocer servicios mediante sus puertos y protocolos.

> ⚠️ **Importante:** El cifrado de protocolos como HTTPS o SFTP protege el contenido de la comunicación, pero **no oculta necesariamente las direcciones IP de origen y destino**. Un atacante que intercepte el tráfico puede seguir obteniendo cierta información sobre la comunicación.

## 📌 Puntos clave

* Los protocolos son las **reglas que permiten la comunicación entre dispositivos**.
* **TCP** prioriza confiabilidad y **UDP** prioriza velocidad.
* **DNS** traduce nombres de dominio en direcciones IP.
* **HTTP** utiliza el puerto 80 y no cifra la comunicación.
* **HTTPS** utiliza el puerto 443 y protege la comunicación mediante TLS.
* **SNMP** permite administrar y monitorizar dispositivos.
* **ICMP** permite diagnosticar problemas de conectividad.
* **SFTP** permite transferir archivos de forma segura mediante SSH.
* Conocer estos protocolos es fundamental para **analizar tráfico, identificar vulnerabilidades y detectar posibles ataques**.
