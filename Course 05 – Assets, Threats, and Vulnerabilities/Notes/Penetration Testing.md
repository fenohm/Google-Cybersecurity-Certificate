# Pruebas de penetración

## Resumen

Una **Penetration Test (Prueba de penetración o Pen Test)** es un ataque simulado y autorizado que busca identificar vulnerabilidades en sistemas, redes, aplicaciones y procesos.

A diferencia de una **Vulnerability Assessment**, que principalmente identifica vulnerabilidades, un Pen Test intenta **explotar esas vulnerabilidades de forma controlada** para determinar qué consecuencias podría tener un ataque real.

Por ejemplo, un equipo de seguridad podría intentar explotar una vulnerabilidad en una aplicación bancaria para comprobar si permitiría acceder a información de clientes o realizar acciones no autorizadas.

## Vulnerability Assessment vs. Pen Test

La principal diferencia es:

| Vulnerability Assessment            | Penetration Test                       |
| ----------------------------------- | -------------------------------------- |
| Identifica vulnerabilidades         | Intenta explotarlas                    |
| Busca debilidades conocidas         | Simula un ataque real                  |
| Ayuda a priorizar vulnerabilidades  | Determina el impacto potencial         |
| Puede realizarse mediante escáneres | Requiere análisis y técnicas de ataque |

Ambos procesos pueden complementarse dentro de una estrategia de seguridad.

## Red Team, Blue Team y Purple Team

### Red Team

El **Red Team** simula a un atacante para identificar vulnerabilidades y comprobar hasta dónde podría llegar un ataque.

### Blue Team

El **Blue Team** se concentra en la defensa, detección y **Incident Response (Respuesta a incidentes)**.

Busca comprobar si los controles de seguridad pueden detectar y responder ante ataques.

### Purple Team

El **Purple Team** combina el trabajo de Red Team y Blue Team de manera colaborativa.

El objetivo es utilizar los resultados de los ataques simulados para mejorar las capacidades defensivas.

## Estrategias de Pen Testing

La cantidad de información entregada al pentester determina el tipo de prueba.

### White Box

En una **White Box Test (Prueba de caja blanca)**, el pentester dispone de bastante información sobre el sistema.

Puede recibir información como:

* Arquitectura de red.
* Código o documentación.
* Flujo de datos.
* Información sobre sistemas internos.

### Black Box

En una **Black Box Test (Prueba de caja negra)**, el pentester tiene poca o ninguna información interna.

La prueba intenta representar la perspectiva de un atacante externo.

### Gray Box

En una **Gray Box Test (Prueba de caja gris)**, el pentester recibe información o acceso limitado.

Representa situaciones en las que un atacante puede disponer de cierto conocimiento interno.

```text
Información disponible

White Box  → ██████████  Alta
Gray Box   → █████░░░░░  Parcial
Black Box  → ░░░░░░░░░░  Mínima
```

## Habilidades necesarias

El Pen Testing combina conocimientos de diferentes áreas de ciberseguridad:

* **Network Security:** seguridad de redes.
* **Application Security:** seguridad de aplicaciones.
* **Linux:** administración y análisis de sistemas Linux.
* **Vulnerability Analysis:** identificación y análisis de vulnerabilidades.
* **Threat Modeling:** identificación de posibles amenazas.
* **Python y Bash:** automatización y creación de herramientas.
* **Detection and Response:** detección y respuesta ante incidentes.
* **Communication:** capacidad para documentar y comunicar los resultados.

Por eso, aprender programación y sistemas operativos puede ser muy útil para avanzar posteriormente hacia pentesting.

## Bug Bounty

Los **Bug Bounty Programs (Programas de recompensas por errores)** permiten que investigadores de seguridad encuentren y reporten vulnerabilidades de productos o servicios a cambio de posibles recompensas.

Son una forma de practicar investigación de seguridad dentro de programas autorizados y definidos por las organizaciones.

Es importante respetar siempre el **scope (alcance)** y las reglas establecidas por cada programa.

## Puntos clave

* Un **Penetration Test** es un ataque simulado, autorizado y controlado.
* Una **Vulnerability Assessment** identifica vulnerabilidades, mientras que un Pen Test busca comprobar su impacto mediante explotación controlada.
* **Red Team** simula ataques.
* **Blue Team** se concentra en defensa y respuesta.
* **Purple Team** combina ambos enfoques de forma colaborativa.
* **White Box** proporciona mucha información al pentester.
* **Black Box** proporciona poca o ninguna información interna.
* **Gray Box** proporciona información limitada.
* El Pen Testing requiere conocimientos de redes, sistemas, aplicaciones, vulnerabilidades y programación.
* Los **Bug Bounty Programs** permiten investigar vulnerabilidades dentro de programas autorizados.
* Toda prueba de penetración debe realizarse con autorización y dentro del alcance definido.
