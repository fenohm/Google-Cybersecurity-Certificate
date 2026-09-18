# Ataques de fuerza bruta

## Resumen

Los **Brute Force Attacks (Ataques de fuerza bruta)** son técnicas utilizadas para obtener acceso no autorizado mediante intentos repetidos de adivinar credenciales u otra información protegida.

Las contraseñas son un control de seguridad importante, pero pueden ser vulnerables cuando son débiles, reutilizadas o están expuestas en filtraciones de datos.

## Tipos de ataques

Existen diferentes formas de realizar ataques de fuerza bruta:

* **Simple Brute Force:** prueba diferentes combinaciones de nombres de usuario y contraseñas hasta encontrar una válida.
* **Dictionary Attack:** utiliza listas de contraseñas o credenciales comunes para intentar acceder a una cuenta.
* **Reverse Brute Force:** comienza con una contraseña conocida y la prueba contra múltiples cuentas o sistemas.
* **Credential Stuffing:** utiliza credenciales obtenidas de filtraciones anteriores para intentar acceder a cuentas en otros servicios.
* **Pass the Hash:** utiliza credenciales o hashes obtenidos previamente para intentar autenticarse sin conocer necesariamente la contraseña original.
* **Exhaustive Key Search:** intenta diferentes claves posibles para descifrar información protegida mediante cifrado.

## Herramientas

Existen herramientas que pueden automatizar diferentes tipos de pruebas relacionadas con credenciales y autenticación:

* **Aircrack-ng:** utilizado para analizar y probar la seguridad de redes Wi-Fi.
* **Hashcat:** herramienta utilizada principalmente para recuperar o probar contraseñas a partir de hashes.
* **John the Ripper:** herramienta para evaluar la seguridad de contraseñas.
* **Ophcrack:** herramienta orientada a la recuperación de contraseñas mediante tablas precomputadas.
* **THC Hydra:** herramienta utilizada para realizar pruebas automatizadas contra distintos servicios de autenticación.

Estas herramientas pueden ser utilizadas por profesionales de seguridad para evaluar sistemas propios o autorizados.

## Medidas de prevención

Las organizaciones pueden utilizar diferentes controles para reducir el riesgo de ataques de fuerza bruta:

### Hashing y Salting

**Hashing** transforma una contraseña en un valor que no debería permitir recuperar directamente la contraseña original.

**Salting** consiste en añadir datos aleatorios a una contraseña antes de realizar el proceso de hashing. Esto dificulta ataques como los **Dictionary Attacks** y reduce la utilidad de tablas precomputadas.

### Multi-Factor Authentication

**Multi-Factor Authentication (MFA)** requiere dos o más factores para verificar la identidad de un usuario.

Por ejemplo:

```text
Contraseña + Código de autenticación
```

Aunque un atacante consiga la contraseña, todavía necesitaría superar el segundo factor.

### CAPTCHA

**CAPTCHA** es un mecanismo de desafío-respuesta diseñado para diferenciar entre usuarios humanos y sistemas automatizados.

Puede ayudar a dificultar los intentos automatizados de autenticación.

### Password Policies

Las **Password Policies (Políticas de contraseñas)** establecen reglas para mejorar la seguridad de las credenciales.

Pueden incluir:

* Longitud mínima.
* Restricciones sobre contraseñas comunes.
* Bloqueo o limitación de intentos.
* Requisitos de autenticación adicionales.
* Reglas para evitar la reutilización de contraseñas.

Una política adecuada debe buscar que las credenciales sean difíciles de comprometer sin generar requisitos innecesariamente difíciles para los usuarios.

## Puntos clave

* Los **Brute Force Attacks** intentan obtener acceso mediante múltiples intentos.
* Los principales métodos incluyen **Simple Brute Force, Dictionary Attack, Reverse Brute Force** y **Credential Stuffing**.
* Herramientas como **Hashcat, John the Ripper y THC Hydra** pueden utilizarse para evaluar la seguridad de sistemas y credenciales.
* **Hashing + Salting** ayudan a proteger las contraseñas almacenadas.
* **MFA** agrega una capa adicional de protección incluso cuando una contraseña es comprometida.
* **CAPTCHA** puede dificultar los ataques automatizados.
* Las políticas de contraseñas ayudan a establecer prácticas de autenticación consistentes.
* Estas herramientas y técnicas deben utilizarse únicamente sobre sistemas propios o con autorización.
