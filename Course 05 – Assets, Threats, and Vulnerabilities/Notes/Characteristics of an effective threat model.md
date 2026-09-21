# Características de un modelo de amenaza eficaz

## Resumen

El **Threat Modeling (Modelado de amenazas)** es un proceso utilizado para identificar los recursos de un sistema, sus vulnerabilidades y las posibles amenazas a las que están expuestos.

Su objetivo es **identificar riesgos de forma proactiva** y determinar qué controles de seguridad pueden utilizarse para reducirlos.

Aunque tradicionalmente se ha utilizado mucho durante el desarrollo de aplicaciones, también puede aplicarse a sistemas, procesos y entornos empresariales.

## Importancia de la seguridad de aplicaciones

Las aplicaciones web y móviles manejan grandes cantidades de información y permiten conectar a usuarios con organizaciones y servicios.

Una vulnerabilidad en una aplicación puede tener consecuencias importantes. Un ejemplo conocido es **Log4Shell (CVE-2021-44228)**, una vulnerabilidad crítica relacionada con una biblioteca de registro de Java que podía permitir **Remote Code Execution (RCE)**.

Por esto, la seguridad debe considerarse durante todo el **Software Development Life Cycle (SDLC)** y no solamente después de que una aplicación haya sido desarrollada.

## Proceso de Threat Modeling

Un ejercicio de **Threat Modeling** puede realizarse mediante un ciclo de varias etapas:

1. **Define Scope:** definir el alcance del análisis.
2. **Identify Threats:** identificar posibles amenazas.
3. **Characterize Environment:** analizar el entorno y cómo funciona el sistema.
4. **Analyze Threats:** estudiar las amenazas y sus posibles impactos.
5. **Mitigate Risks:** implementar controles para reducir los riesgos.
6. **Evaluate Results:** revisar los resultados y determinar si las medidas fueron adecuadas.

Idealmente, este proceso debe realizarse durante diferentes etapas del desarrollo de una aplicación.

## Frameworks de Threat Modeling

Existen diferentes frameworks y metodologías que pueden utilizarse según las necesidades de una organización.

### STRIDE

**STRIDE** es un framework desarrollado por Microsoft que permite identificar seis categorías principales de amenazas:

| Letra | Amenaza                | Concepto                  |
| ----- | ---------------------- | ------------------------- |
| **S** | Spoofing               | Suplantación de identidad |
| **T** | Tampering              | Manipulación de datos     |
| **R** | Repudiation            | Repudio de acciones       |
| **I** | Information Disclosure | Revelación de información |
| **D** | Denial of Service      | Denegación de servicio    |
| **E** | Elevation of Privilege | Elevación de privilegios  |

STRIDE es especialmente útil para analizar cómo una aplicación podría ser atacada y qué controles pueden implementarse para reducir esos riesgos.

### PASTA

**PASTA (Process for Attack Simulation and Threat Analysis)** es un enfoque de Threat Modeling centrado en el riesgo.

Busca analizar posibles escenarios de ataque y relacionarlos con los riesgos del negocio y de la aplicación.

Su proceso utiliza diferentes etapas y puede incorporar información proveniente de evaluaciones de vulnerabilidades y otros análisis de seguridad.

### Trike

**Trike** es una metodología y herramienta de código abierto enfocada en la seguridad.

Se concentra principalmente en aspectos como:

* Permisos.
* Casos de uso.
* Privilegios.
* Controles de seguridad.

### VAST

**VAST (Visual, Agile and Simple Threat Modeling)** es un framework orientado a hacer el Threat Modeling más visual, ágil y escalable.

Puede utilizarse junto con plataformas automatizadas para facilitar el análisis en organizaciones con muchos sistemas y aplicaciones.

## Participación en Threat Modeling

El Threat Modeling normalmente requiere colaboración entre diferentes áreas, especialmente cuando se analiza una aplicación.

Un analista de ciberseguridad puede aportar una **Attack Mindset (Mentalidad de atacante)** y ayudar a formular preguntas como:

* ¿Qué estamos protegiendo?
* ¿Qué podría salir mal?
* ¿Cómo podría aprovecharlo un atacante?
* ¿Qué controles existen actualmente?
* ¿Qué riesgos todavía no han sido abordados?
* ¿Las medidas implementadas son suficientes?

También pueden utilizarse herramientas como **Data Flow Diagrams (DFD)** y **Attack Trees** para representar cómo circula la información y cómo podría desarrollarse un ataque.

## Relación con DevSecOps

El Threat Modeling es especialmente importante dentro de **DevSecOps**, donde la seguridad se integra con el desarrollo y las operaciones.

En lugar de esperar hasta que una aplicación esté terminada para buscar vulnerabilidades, la seguridad se considera durante las diferentes etapas del desarrollo.

Esto permite detectar problemas antes de que lleguen a producción y reducir el costo y el impacto de corregir vulnerabilidades posteriormente.

## Puntos clave

* **Threat Modeling** permite identificar amenazas, vulnerabilidades y riesgos de forma proactiva.
* Debe incorporarse durante el **SDLC** y no únicamente después del desarrollo.
* El proceso puede incluir definir el alcance, identificar amenazas, analizar riesgos, mitigarlos y evaluar los resultados.
* **STRIDE** clasifica amenazas en seis categorías: Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service y Elevation of Privilege.
* **PASTA** utiliza un enfoque centrado en el riesgo y la simulación de ataques.
* **Trike** se enfoca en permisos, privilegios y controles de seguridad.
* **VAST** busca hacer el Threat Modeling más visual, ágil y escalable.
* El análisis de amenazas requiere colaboración entre diferentes áreas.
* Utilizar una **Attack Mindset** ayuda a identificar cómo podría intentar atacar un sistema una persona maliciosa.
* **Threat Modeling + DevSecOps** permite incorporar la seguridad desde las primeras etapas del desarrollo.
