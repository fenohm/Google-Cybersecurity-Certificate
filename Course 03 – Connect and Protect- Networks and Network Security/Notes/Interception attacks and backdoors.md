# 🛡️ Ataques de interceptación y puertas traseras

Los ataques de red pueden aprovechar diferentes técnicas para **interceptar comunicaciones, obtener acceso no autorizado o mantener una presencia dentro de un sistema**.

Entre ellos destacan los **ataques de interceptación de red** y los **ataques de puerta trasera (backdoor)**.

---

# 🕵️ Ataques de interceptación de red

Los ataques de interceptación consisten en **capturar el tráfico de red** para obtener información o modificar las comunicaciones.

Los atacantes pueden utilizar herramientas de hardware o software para realizar **packet sniffing**, permitiéndoles inspeccionar los datos que circulan por una red.

```text id="6f6jdn"
Dispositivo A ────────► Dispositivo B
             │
             ▼
        🕵️ Atacante
        Captura tráfico
```

### Posibles acciones del atacante

* Capturar información sensible.
* Inspeccionar paquetes de red.
* Robar credenciales o datos.
* Modificar comunicaciones.
* Insertar contenido malicioso.
* Interrumpir operaciones.

### Ejemplo

Un atacante podría interceptar una transferencia bancaria y modificar los datos para redirigir los fondos hacia una cuenta controlada por él.

---

# 🚪 Ataques de puerta trasera — Backdoor

Una **puerta trasera** es un mecanismo que permite acceder a un sistema **evitando los mecanismos normales de autenticación o control de acceso**.

Las backdoors pueden existir de forma legítima, por ejemplo, para permitir tareas administrativas o solucionar problemas. Sin embargo, también pueden ser creadas o instaladas por atacantes para mantener **acceso persistente** a un sistema comprometido.

```text id="p5z8wx"
Acceso normal
Usuario → Autenticación → Sistema

Backdoor
Atacante ────────────────→ Sistema
              🚪
          Acceso alternativo
```

Una vez obtenida la persistencia, un atacante podría:

* Instalar malware.
* Robar información.
* Modificar configuraciones.
* Realizar ataques DoS.
* Crear nuevos mecanismos de acceso.
* Comprometer otros sistemas.

---

# 💥 DoS — Denial of Service

Un ataque **DoS (Denial of Service)** intenta dejar un sistema o servicio inaccesible mediante una sobrecarga de tráfico o solicitudes.

```text id="0tqzll"
Atacante
  │
  ├──► Solicitudes
  ├──► Solicitudes
  ├──► Solicitudes
  ├──► Solicitudes
  ▼
┌──────────────┐
│   Servidor   │
│   Sobrecarga │
└──────────────┘
      ❌
   Servicio
   inaccesible
```

El resultado puede ser la **interrupción de servicios y operaciones**.

---

# 📊 Impacto de los ataques de red

Un ataque exitoso puede afectar a una organización en diferentes áreas.

## 💰 Impacto financiero

Las organizaciones pueden sufrir:

* Pérdida de ingresos por interrupciones.
* Costos de recuperación.
* Reparación de infraestructura.
* Costos relacionados con ransomware.
* Gastos legales.
* Compensaciones a clientes afectados.

Un ataque que deje servicios críticos fuera de línea puede generar pérdidas importantes, especialmente en organizaciones grandes.

---

## 🏢 Impacto reputacional

Una brecha de seguridad puede provocar una pérdida de confianza por parte de:

* Clientes.
* Empleados.
* Socios comerciales.
* Inversionistas.
* Público general.

Los clientes pueden optar por utilizar servicios de competidores si consideran que una organización no protege adecuadamente sus datos.

---

## 🚨 Impacto en la seguridad pública

Los ataques contra sistemas gubernamentales o infraestructura crítica pueden tener consecuencias que van más allá de las pérdidas económicas.

Ejemplos de objetivos críticos:

```text id="2ex2a6"
⚡ Redes eléctricas
💧 Sistemas de agua
📡 Sistemas de comunicación
🏥 Infraestructura sanitaria
🛡️ Sistemas de defensa
```

Si un atacante compromete infraestructura crítica, un incidente cibernético puede llegar a producir **consecuencias físicas para la población**.

---

# 🧠 Relación con la ciberseguridad

Estos ataques demuestran que la seguridad de una red debe proteger tanto:

```text id="l1x2a8"
        Datos
          │
          ▼
    ┌───────────┐
    │   Red     │
    └───────────┘
       │     │
       ▼     ▼
 Interceptación  Acceso no autorizado
       │              │
       ▼              ▼
 Packet sniffing     Backdoor
       │              │
       └──────┬───────┘
              ▼
          Impacto
```

Por ello, los analistas deben considerar mecanismos como **cifrado, segmentación de red, control de acceso, monitoreo y detección de anomalías**.

## 📌 Puntos clave

* **Packet sniffing** permite capturar e inspeccionar tráfico de red.
* Los ataques de interceptación pueden **robar o modificar información en tránsito**.
* Una **backdoor** proporciona un mecanismo alternativo de acceso a un sistema.
* Los atacantes pueden utilizar backdoors para mantener **persistencia** después de comprometer una organización.
* Un **DoS** busca interrumpir la disponibilidad de un sistema o servicio.
* Los ataques pueden generar impactos **financieros, reputacionales y operacionales**.
* Los ataques contra infraestructura crítica pueden incluso representar riesgos para la **seguridad pública**.
* El cifrado y el monitoreo del tráfico son medidas importantes para reducir los riesgos asociados a la interceptación de comunicaciones.
