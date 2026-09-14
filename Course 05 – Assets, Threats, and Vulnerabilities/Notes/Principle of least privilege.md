# Principio de privilegio mínimo

## Resumen

El **Principle of Least Privilege (PoLP)** es un principio de seguridad que establece que cada usuario debe recibir **solamente el nivel mínimo de acceso y autorización necesario para realizar sus tareas**.

Su objetivo principal es reducir el riesgo de accesos no autorizados, modificaciones accidentales o abuso de privilegios, ayudando a proteger la **Confidentiality, Integrity and Availability (CIA Triad)** de la información.

### Cómo reduce el riesgo

Aplicar el mínimo privilegio permite:

* Limitar el acceso a información sensible.
* Reducir la posibilidad de modificación o pérdida accidental de datos.
* Disminuir el impacto de una cuenta comprometida.
* Facilitar la supervisión y administración de los sistemas.

El principio debe aplicarse a todos los recursos que maneje una organización, asignando permisos según las necesidades reales de cada usuario.

### Tipos de cuentas

Antes de aplicar el mínimo privilegio es necesario identificar quién necesita acceso y qué nivel de autorización requiere.

Algunos tipos comunes de cuentas son:

* **Guest Account:** Cuenta para usuarios externos que necesitan acceso limitado.
* **User Account:** Cuenta asignada a empleados según sus funciones.
* **Service Account:** Cuenta utilizada por aplicaciones o servicios para interactuar con otros sistemas.
* **Privileged Account:** Cuenta con permisos elevados, normalmente utilizada para tareas administrativas.

Cada cuenta debería tener solamente los permisos necesarios para cumplir su función.

### Least Privilege y Separation of Duties

El **Least Privilege** está relacionado con **Separation of Duties (SoD)** o separación de funciones.

La separación de funciones consiste en distribuir tareas y responsabilidades entre diferentes usuarios para evitar que una sola persona tenga control absoluto sobre funciones críticas.

Ambos principios ayudan a reducir el riesgo de abuso de privilegios y accesos no autorizados.

### Auditoría de privilegios

Asignar correctamente los permisos no es suficiente. Los accesos deben revisarse periódicamente porque los usuarios pueden acumular permisos que ya no necesitan.

Este problema se conoce como **Privilege Creep (acumulación de privilegios)**.

Existen tres auditorías comunes:

* **Usage Audit:** Revisa qué recursos utiliza cada cuenta y qué acciones realiza.
* **Privilege Audit:** Comprueba si los permisos de un usuario corresponden con sus funciones actuales.
* **Account Change Audit:** Revisa cambios realizados en las cuentas, como modificaciones de contraseñas o permisos.

Estas auditorías permiten identificar permisos innecesarios y revocarlos cuando ya no son requeridos.

## Puntos clave

* **Least Privilege** significa otorgar únicamente los permisos necesarios para realizar una tarea.
* Es un control fundamental para reducir el riesgo de accesos no autorizados.
* Existen diferentes tipos de cuentas, como **Guest, User, Service y Privileged Accounts**.
* Los permisos deben revisarse periódicamente para evitar **Privilege Creep**.
* **Separation of Duties** complementa el mínimo privilegio al distribuir responsabilidades críticas.
* La auditoría de cuentas permite detectar permisos innecesarios y actividades sospechosas.
* El mínimo privilegio ayuda a proteger la **Confidentiality, Integrity and Availability (CIA Triad)**.
