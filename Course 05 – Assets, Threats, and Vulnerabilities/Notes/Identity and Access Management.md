# Gestión de identidad y acceso (IAM)

## Resumen

La **Identity and Access Management (IAM)** es un conjunto de procesos y tecnologías utilizados para gestionar las identidades digitales y controlar el acceso a los recursos de una organización.

Su objetivo puede resumirse como:

> El usuario adecuado debe tener acceso a los recursos adecuados, en el momento adecuado y por las razones adecuadas.

IAM se relaciona directamente con dos principios fundamentales:

* **Principle of Least Privilege:** cada usuario recibe únicamente los permisos necesarios para realizar sus tareas.
* **Separation of Duties (SoD):** las responsabilidades importantes se dividen entre diferentes personas para evitar que una sola persona tenga demasiado control.

## IAM y AAA

**IAM** y **AAA (Authentication, Authorization and Accounting)** son modelos utilizados para gestionar el acceso a los recursos.

Ambos permiten:

* **Authentication:** verificar quién es el usuario.
* **Authorization:** determinar qué recursos puede utilizar.
* **Accounting:** registrar y supervisar las actividades realizadas.

Un usuario puede ser una persona, un dispositivo o incluso una aplicación.

### Autenticación

La **Authentication (Autenticación)** verifica que el usuario realmente sea quien afirma ser.

Los principales factores de autenticación son:

* **Something you know:** algo que sabes, como una contraseña.
* **Something you have:** algo que tienes, como un dispositivo o token.
* **Something you are:** algo que eres, como una huella digital.

También pueden utilizarse tecnologías como **SSO** y **MFA** para mejorar el proceso de autenticación.

## User Provisioning

El **User Provisioning (Aprovisionamiento de usuarios)** consiste en crear y configurar la identidad digital de un usuario y asignarle los permisos correspondientes.

Por ejemplo, cuando un empleado ingresa a una empresa, puede recibir:

* Una cuenta de usuario.
* Acceso a determinadas aplicaciones.
* Permisos según su función.
* Acceso a recursos específicos.

El proceso contrario es el **Deprovisioning (Desaprovisionamiento)**, que consiste en eliminar o retirar los permisos de un usuario cuando ya no necesita acceso.

Esto es especialmente importante cuando un empleado abandona una organización.

## Modelos de control de acceso

Una vez autenticado un usuario, es necesario determinar qué recursos puede utilizar.

Los tres modelos principales estudiados son:

### MAC

El **Mandatory Access Control (MAC)** es un modelo de control de acceso estricto en el que los permisos son determinados por una autoridad central.

Los usuarios no pueden modificar libremente los permisos.

Es común en entornos donde existe una alta necesidad de control, como organizaciones militares o gubernamentales.

### DAC

El **Discretionary Access Control (DAC)** permite que el propietario de un recurso determine quién puede acceder a él y qué permisos tendrá.

Por ejemplo, el propietario de una carpeta puede decidir si otro usuario tendrá permisos de:

* Lectura.
* Edición.
* Comentario.

### RBAC

El **Role-Based Access Control (RBAC)** asigna permisos según el rol o función que desempeña una persona dentro de una organización.

Por ejemplo:

```text
Usuario → Rol → Permisos

Analista de seguridad → Security Analyst → SIEM / Logs
Administrador → Administrator → Sistemas / Configuración
RR.HH. → HR → Recursos humanos
```

RBAC permite administrar los permisos de forma más organizada y facilita la aplicación del **Principle of Least Privilege**.

## Tecnologías de control de acceso

Una solución IAM normalmente combina diferentes componentes para gestionar las identidades y los permisos.

Puede incluir:

* Directorio de usuarios.
* Herramientas para administrar identidades.
* Sistemas de autenticación.
* Sistemas de autorización.
* Registro y auditoría de actividades.

Estas tecnologías permiten automatizar la administración de accesos y reducir errores humanos.

## Puntos clave

* **IAM** permite gestionar identidades digitales y controlar el acceso a los recursos.
* **AAA** y **IAM** son modelos utilizados para administrar el acceso de los usuarios.
* **Authentication** verifica la identidad.
* **Authorization** determina qué puede hacer el usuario.
* **Accounting** registra las actividades realizadas.
* **Provisioning** crea y configura cuentas y permisos.
* **Deprovisioning** elimina los accesos cuando ya no son necesarios.
* **MAC** utiliza políticas de acceso estrictas y centralizadas.
* **DAC** permite al propietario del recurso decidir los permisos.
* **RBAC** asigna permisos según el rol del usuario.
* **Least Privilege** limita los permisos al mínimo necesario.
* **Separation of Duties** divide responsabilidades para evitar abusos de privilegios.
