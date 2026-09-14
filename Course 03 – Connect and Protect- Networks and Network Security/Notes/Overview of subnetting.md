# 🌐 Visión general de la creación de subredes

La **división en subredes (subnetting)** consiste en dividir una red grande en **redes más pequeñas y organizadas**, llamadas **subredes**.

Cada subred se define mediante una combinación de:

* **Dirección IP**
* **Máscara de subred**
* **Prefijo de red**

Esto permite crear una **"red dentro de otra red"**, mejorando la organización, el rendimiento y la seguridad.

```text id="0v8qj2"
Red principal
│
├── Subred 1 → Usuarios
├── Subred 2 → Servidores
├── Subred 3 → Administración
└── Subred 4 → Invitados
```

Los dispositivos que pertenecen a la misma subred pueden comunicarse directamente dentro de ella, mientras que la comunicación entre subredes normalmente requiere un **router o dispositivo de capa 3**.

---

# 📐 CIDR — Classless Inter-Domain Routing

**CIDR** es un método moderno para representar direcciones IP y sus máscaras de red mediante un **prefijo**.

Ejemplo:

```text id="j8m4u1"
198.51.100.0/24
```

El `/24` indica que **24 bits pertenecen a la parte de red**, dejando 8 bits para hosts.

```text id="7i9vby"
198.51.100.0/24
│────────││
  Red     Host
 24 bits  8 bits
```

Una red `/24` contiene:

```text id="lq6p4z"
198.51.100.0
       ↓
198.51.100.255
```

Es decir, **256 direcciones en total**, aunque en una subred IPv4 tradicional normalmente se reservan la dirección de red y la de broadcast, dejando **254 direcciones utilizables para hosts**.

---

# 🧮 Prefijos CIDR comunes

| CIDR  | Máscara         | Direcciones totales | Hosts utilizables* |
| ----- | --------------- | ------------------: | -----------------: |
| `/24` | 255.255.255.0   |                 256 |                254 |
| `/25` | 255.255.255.128 |                 128 |                126 |
| `/26` | 255.255.255.192 |                  64 |                 62 |
| `/27` | 255.255.255.224 |                  32 |                 30 |
| `/28` | 255.255.255.240 |                  16 |                 14 |
| `/29` | 255.255.255.248 |                   8 |                  6 |
| `/30` | 255.255.255.252 |                   4 |                  2 |

*En una subred IPv4 tradicional donde se reservan dirección de red y broadcast.

---

# 🔄 Direccionamiento con clase vs. CIDR

Antes de CIDR se utilizaba el **direccionamiento classful**, que dividía las direcciones IPv4 en clases como A, B y C.

Este sistema podía desperdiciar grandes cantidades de direcciones.

CIDR introdujo un sistema **sin clases**, permitiendo utilizar prefijos de diferentes tamaños.

```text id="w4y8qz"
Classful
Clase A → grandes redes
Clase B → redes medianas
Clase C → redes pequeñas

          ↓

CIDR
/24 /25 /26 /27 /28 ...
```

Esto permite asignar los recursos de direccionamiento de manera mucho más eficiente.

---

# 🛡️ Ventajas de seguridad del subnetting

La creación de subredes no solo permite organizar las direcciones IP, sino que también puede utilizarse como una **medida de seguridad**.

Permite separar diferentes tipos de dispositivos y controlar la comunicación entre ellos.

### Ejemplo

```text id="m9f7wl"
                 ┌── Subred Usuarios
                 │
Internet → Router ├── Subred Servidores
                 │
                 ├── Subred Administración
                 │
                 └── Subred Invitados
```

Mediante **routers, ACLs y firewalls**, se pueden establecer reglas para controlar qué subredes pueden comunicarse entre sí.

Por ejemplo:

```text id="s7y1xk"
Usuarios   → Servidores      ✅ Permitido
Usuarios   → Administración  ❌ Bloqueado
Invitados  → Servidores      ❌ Bloqueado
Invitados  → Internet        ✅ Permitido
```

Esto ayuda a implementar **segmentación y aislamiento de redes**, reduciendo el impacto potencial de un ataque.

---

# ⚡ Ventajas del subnetting

### Organización

Permite separar dispositivos según su función, departamento o nivel de acceso.

### Rendimiento

Reduce el tamaño de los dominios de red y puede disminuir el tráfico innecesario.

### Eficiencia de direcciones

CIDR permite utilizar rangos de direcciones de manera más eficiente.

### Seguridad

Facilita la creación de zonas aisladas y la aplicación de controles de acceso.

### Escalabilidad

Permite dividir y reorganizar una red a medida que aumenta el número de dispositivos.

---

# 📌 Puntos clave

* **Subnetting** = dividir una red grande en subredes más pequeñas.
* Una subred se define mediante **IP + máscara/prefijo**.
* **CIDR** permite utilizar prefijos flexibles como `/24`, `/26`, `/28`, etc.
* `/24` significa que **24 bits corresponden a la red** y 8 bits a los hosts.
* CIDR reemplazó al antiguo sistema de direccionamiento **classful**.
* El subnetting mejora la **organización, eficiencia y rendimiento** de las redes.
* Las subredes también pueden utilizarse para crear **zonas de seguridad**.
* **Routers, ACLs y firewalls** pueden controlar el tráfico entre diferentes subredes.
* La segmentación ayuda a **limitar el movimiento lateral** de un atacante dentro de una red.
