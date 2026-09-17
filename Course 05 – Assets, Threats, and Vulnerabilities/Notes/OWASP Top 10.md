# OWASP Top 10

## Resumen

**OWASP (Open Worldwide Application Security Project)** es una organización sin fines de lucro que trabaja para mejorar la seguridad del software. Proporciona recursos, herramientas y documentación utilizados por profesionales de ciberseguridad y desarrollo.

Uno de sus recursos más conocidos es **OWASP Top 10**, una lista de las categorías de vulnerabilidades más importantes y frecuentes en aplicaciones web.

A diferencia de **CVE**, que permite identificar vulnerabilidades específicas en productos y versiones concretas, OWASP Top 10 se enfoca principalmente en **categorías de riesgos de seguridad en aplicaciones web**.

## Principales vulnerabilidades

### 1. Broken Access Control

**Broken Access Control (Control de acceso roto)** ocurre cuando una aplicación no limita correctamente las acciones que puede realizar un usuario.

Puede permitir:

* Acceder a información no autorizada.
* Modificar datos de otros usuarios.
* Eliminar recursos sin permiso.
* Acceder a funciones administrativas.

Está directamente relacionado con principios como **Least Privilege** y **RBAC**.

### 2. Cryptographic Failures

**Cryptographic Failures (Fallos criptográficos)** aparecen cuando los datos sensibles no están protegidos correctamente.

Ejemplos:

* No cifrar información sensible.
* Utilizar algoritmos criptográficos débiles.
* Almacenar contraseñas de forma insegura.
* Utilizar hashes vulnerables como **MD5** para proteger información sensible.

### 3. Injection

**Injection (Inyección)** ocurre cuando una aplicación interpreta datos proporcionados por un usuario como parte de una instrucción o código.

Un ejemplo conocido es **SQL Injection**, donde un atacante manipula una entrada para alterar una consulta SQL.

Las inyecciones pueden permitir:

* Acceder a información.
* Modificar o eliminar datos.
* Ejecutar acciones no autorizadas.

### 4. Insecure Design

**Insecure Design (Diseño inseguro)** ocurre cuando una aplicación no incorpora controles de seguridad adecuados desde su diseño.

No se trata necesariamente de un error puntual de programación, sino de una debilidad en la forma en que fue diseñada la aplicación.

Por esto, la seguridad debe considerarse desde las primeras etapas del desarrollo.

### 5. Security Misconfiguration

**Security Misconfiguration (Desconfiguración de seguridad)** ocurre cuando los sistemas o aplicaciones tienen configuraciones inseguras.

Ejemplos:

* Mantener contraseñas predeterminadas.
* Dejar servicios innecesarios habilitados.
* Utilizar configuraciones por defecto.
* No aplicar correctamente controles de seguridad.

La configuración incorrecta de servidores, aplicaciones o servicios puede crear puntos de entrada para los atacantes.

### 6. Vulnerable and Outdated Components

**Vulnerable and Outdated Components (Componentes vulnerables y obsoletos)** se refiere al uso de bibliotecas, frameworks o componentes que contienen vulnerabilidades conocidas.

Es importante:

* Mantener un inventario de dependencias.
* Actualizar componentes.
* Revisar vulnerabilidades conocidas.
* Utilizar herramientas de **Software Composition Analysis (SCA)**.

Esta categoría se relaciona directamente con la gestión de dependencias estudiada en CI/CD.

### 7. Identification and Authentication Failures

**Identification and Authentication Failures (Fallos de identificación y autenticación)** ocurren cuando una aplicación no verifica correctamente la identidad de los usuarios o gestiona incorrectamente sus sesiones.

Algunos ejemplos son:

* Autenticación débil.
* Gestión insegura de sesiones.
* Falta de controles contra ataques de credenciales.
* Implementaciones incorrectas de autenticación.

El uso de **MFA (Multi-Factor Authentication)** puede ayudar a fortalecer la autenticación.

### 8. Software and Data Integrity Failures

**Software and Data Integrity Failures (Fallos de integridad del software y los datos)** ocurren cuando no se verifica adecuadamente la integridad y autenticidad de software, actualizaciones o datos.

Un riesgo importante es el **Supply Chain Attack (Ataque a la cadena de suministro)**, donde un atacante compromete un componente o proveedor para afectar posteriormente a sus usuarios.

Un ejemplo conocido es el ataque a **SolarWinds en 2020**, donde se distribuyó código malicioso mediante actualizaciones comprometidas.

### 9. Security Logging and Monitoring Failures

**Security Logging and Monitoring Failures (Fallos de registro y monitoreo de seguridad)** aparecen cuando una organización no registra o supervisa adecuadamente los eventos de seguridad.

Los **Logs (registros)** son importantes para:

* Detectar actividades sospechosas.
* Investigar incidentes.
* Identificar intentos de acceso no autorizado.
* Analizar qué ocurrió durante un incidente.

El monitoreo continuo permite detectar problemas y responder más rápidamente.

### 10. Server-Side Request Forgery (SSRF)

**SSRF (Server-Side Request Forgery)** ocurre cuando un atacante consigue manipular una aplicación del servidor para realizar solicitudes hacia otros recursos a los que normalmente no debería tener acceso.

Por ejemplo, una aplicación vulnerable podría ser utilizada para solicitar información desde servicios internos de una organización.

Este tipo de vulnerabilidad puede ser especialmente peligroso cuando el servidor tiene acceso a recursos internos o información sensible.

## OWASP Top 10 y ciberseguridad

El OWASP Top 10 puede utilizarse como referencia durante diferentes etapas de seguridad:

```text
Diseño
  ↓
Desarrollo
  ↓
Pruebas de seguridad
  ↓
Despliegue
  ↓
Monitoreo
```

También puede complementarse con recursos como **CVE**, análisis de dependencias, **SAST**, **DAST** y **SCA**.

Por ejemplo:

* **OWASP Top 10:** identifica categorías de riesgos comunes en aplicaciones web.
* **CVE:** identifica vulnerabilidades específicas conocidas.
* **SAST:** analiza el código fuente.
* **DAST:** analiza aplicaciones en ejecución.
* **SCA:** analiza dependencias y componentes de terceros.

## Puntos clave

* **OWASP** es una organización dedicada a mejorar la seguridad del software.
* **OWASP Top 10** es una referencia fundamental para la seguridad de aplicaciones web.
* Sus categorías incluyen problemas de acceso, criptografía, inyección, configuración, autenticación, dependencias e integridad.
* **Broken Access Control** puede permitir acciones no autorizadas.
* **Injection** puede permitir que entradas maliciosas sean interpretadas como código o instrucciones.
* **Security Misconfiguration** puede generar vulnerabilidades por configuraciones inseguras.
* Los componentes obsoletos pueden contener vulnerabilidades conocidas.
* **SSRF** permite abusar de una aplicación vulnerable para realizar solicitudes desde el servidor.
* Los **logs** y el monitoreo son fundamentales para detectar e investigar incidentes.
* OWASP Top 10 complementa recursos como **CVE**, **SAST, DAST y SCA**.
