# Seguridad CI/CD

## Resumen

Las canalizaciones **CI/CD (Continuous Integration / Continuous Delivery / Continuous Deployment)** automatizan gran parte del proceso de desarrollo y publicación de software. Aunque mejoran la velocidad y eficiencia, también pueden convertirse en un punto de entrada para ataques si no se protegen correctamente.

Por esto, la seguridad debe integrarse directamente en el proceso de desarrollo mediante un enfoque **DevSecOps**.

## CI/CD

### Integración continua (CI)

La **Continuous Integration (CI)** consiste en integrar frecuentemente los cambios de código de distintos desarrolladores en un repositorio central.

Cada cambio puede activar automáticamente:

* Compilación del software.
* Ejecución de pruebas.
* Análisis de seguridad.
* Detección temprana de errores y vulnerabilidades.

### Entrega continua (Continuous Delivery)

La **Continuous Delivery** mantiene el software preparado para ser publicado. Después de superar las pruebas automatizadas, normalmente existe una aprobación manual antes de llegar a producción.

### Despliegue continuo (Continuous Deployment)

La **Continuous Deployment** automatiza completamente el proceso. Si el código supera todas las comprobaciones, se despliega automáticamente en producción sin intervención manual.

## Vulnerabilidades comunes en CI/CD

Una canalización CI/CD puede presentar diferentes riesgos:

* **Insecure Dependencies:** dependencias de terceros que contienen vulnerabilidades conocidas (**CVE**).
* **Misconfigured Permissions:** permisos excesivos que permiten modificar código o configuraciones críticas.
* **Missing Security Testing:** ausencia de pruebas de seguridad automatizadas.
* **Exposed Secrets:** claves API, contraseñas o tokens almacenados directamente en el código.
* **Insecure Build Environments:** servidores o entornos de compilación vulnerables que pueden ser comprometidos.

## Seguridad integrada en CI/CD

Una estrategia segura utiliza diferentes controles durante el proceso de desarrollo:

* **SAST (Static Application Security Testing):** analiza el código fuente para detectar vulnerabilidades sin ejecutar la aplicación.
* **DAST (Dynamic Application Security Testing):** analiza una aplicación mientras está funcionando.
* **SCA (Software Composition Analysis):** identifica vulnerabilidades y riesgos en dependencias y componentes de terceros.
* **RBAC (Role-Based Access Control):** asigna permisos según el rol del usuario.
* **MFA (Multi-Factor Authentication):** añade factores adicionales para proteger las cuentas.
* **Secrets Management:** utiliza herramientas especializadas para almacenar y administrar información sensible.

También es importante mantener actualizadas las dependencias y utilizar soluciones como **Dependabot**, **Snyk**, **HashiCorp Vault** o **AWS Secrets Manager** cuando corresponda.

## DevSecOps y defensa en profundidad

**DevSecOps** integra la seguridad durante todo el ciclo de desarrollo, en lugar de dejarla únicamente para el final.

Una canalización segura aplica el principio de **Defense in Depth (Defensa en profundidad)** utilizando múltiples controles:

```text
Código
  ↓
SAST
  ↓
SCA / Dependencias
  ↓
Pruebas
  ↓
DAST
  ↓
Validaciones de seguridad
  ↓
Despliegue
```

Esto permite detectar y corregir vulnerabilidades lo antes posible, reduciendo el riesgo y el costo de solucionarlas posteriormente.

## Puntos clave

* **CI/CD** automatiza la integración, entrega y despliegue de software.
* Una canalización insegura puede convertirse en un punto de entrada para ataques.
* Las dependencias vulnerables pueden introducir **CVE** en las aplicaciones.
* **SAST, DAST y SCA** permiten automatizar diferentes tipos de controles de seguridad.
* **RBAC** y **MFA** ayudan a proteger el acceso a las herramientas CI/CD.
* Los secretos nunca deberían almacenarse directamente en el código.
* Los entornos de compilación también deben protegerse.
* **DevSecOps** integra la seguridad desde las primeras etapas del desarrollo.
* La **Defense in Depth** utiliza múltiples capas de seguridad para reducir el riesgo.
