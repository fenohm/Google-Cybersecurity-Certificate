# El auge de SSO y MFA

## Resumen

La **Authentication (Autenticación)** permite verificar la identidad de un usuario antes de concederle acceso a un sistema o recurso.

Dos tecnologías ampliamente utilizadas para mejorar la autenticación son **SSO (Single Sign-On)** y **MFA (Multi-Factor Authentication)**.

* **SSO:** permite utilizar una única autenticación para acceder a múltiples aplicaciones.
* **MFA:** requiere dos o más factores diferentes para verificar la identidad de un usuario.

Utilizadas en conjunto, permiten mejorar la seguridad y, al mismo tiempo, facilitar la experiencia del usuario.

### SSO

El **Single Sign-On (SSO)** permite que un usuario se autentique una sola vez y pueda acceder posteriormente a diferentes aplicaciones y servicios sin iniciar sesión nuevamente en cada uno.

Sus principales beneficios son:

* Reduce la cantidad de contraseñas que los usuarios deben recordar.
* Disminuye la reutilización de contraseñas.
* Simplifica la administración de cuentas.
* Reduce puntos de autenticación independientes.
* Mejora la experiencia del usuario.

El SSO ayuda a combatir la **Password Fatigue (Fatiga de contraseñas)**, que puede llevar a los usuarios a reutilizar contraseñas en diferentes servicios.

### Cómo funciona el SSO

El SSO normalmente utiliza un **Identity Provider (IdP)** para verificar la identidad del usuario.

Una vez autenticado, el proveedor de identidad puede entregar información o **tokens** que permiten al usuario acceder a diferentes servicios sin volver a introducir sus credenciales.

Algunos protocolos relacionados con SSO son:

* **LDAP (Lightweight Directory Access Protocol):** protocolo utilizado para acceder y administrar información almacenada en servicios de directorio.
* **SAML (Security Assertion Markup Language):** estándar utilizado para intercambiar información de autenticación y autorización, especialmente en aplicaciones empresariales y servicios web.

### Limitaciones del SSO

Aunque SSO mejora la administración de accesos, también concentra el riesgo.

Si un atacante obtiene las credenciales de una cuenta protegida únicamente mediante contraseña, podría acceder a múltiples servicios asociados a esa identidad.

Por esto, **SSO no debería considerarse una protección suficiente por sí sola**.

## MFA

La **Multi-Factor Authentication (MFA)** requiere que el usuario proporcione dos o más factores diferentes para demostrar su identidad.

Los principales factores son:

1. **Something you know:** algo que sabes, como una contraseña o PIN.
2. **Something you have:** algo que tienes, como un dispositivo físico, token o código de autenticación.
3. **Something you are:** algo que eres, como una huella digital o reconocimiento facial.

Por ejemplo, un inicio de sesión podría requerir:

**Contraseña + código de autenticación**

o

**Contraseña + huella digital**

La idea es que comprometer un solo factor no sea suficiente para obtener acceso.

### MFA y seguridad en la nube

La MFA es especialmente importante en entornos **Cloud**, donde los usuarios pueden acceder a los sistemas desde diferentes ubicaciones y dispositivos.

Al exigir múltiples factores, se reduce el riesgo de que una contraseña robada sea suficiente para acceder a información sensible.

## SSO + MFA

SSO y MFA cumplen funciones diferentes y pueden utilizarse conjuntamente:

* **SSO:** simplifica y centraliza la autenticación.
* **MFA:** agrega una capa adicional de seguridad.

Un ejemplo sería:

```text
Usuario
   ↓
SSO / Identity Provider
   ↓
Contraseña + MFA
   ↓
Autenticación exitosa
   ↓
Acceso a múltiples aplicaciones
```

Este enfoque permite mantener una experiencia de acceso sencilla para el usuario mientras se reduce el riesgo asociado a credenciales comprometidas.

## Puntos clave

* **SSO** permite acceder a múltiples servicios utilizando una única autenticación.
* **MFA** requiere dos o más factores para verificar la identidad.
* Los tres factores principales son **Something you know, Something you have y Something you are**.
* **SSO** reduce la reutilización de contraseñas y simplifica la administración.
* **MFA** reduce el impacto de una contraseña robada.
* **LDAP** y **SAML** son tecnologías relacionadas con la autenticación y los servicios de identidad.
* El **Identity Provider (IdP)** desempeña un papel central en muchos sistemas SSO.
* SSO y MFA se complementan y son controles importantes en entornos empresariales y de nube.
