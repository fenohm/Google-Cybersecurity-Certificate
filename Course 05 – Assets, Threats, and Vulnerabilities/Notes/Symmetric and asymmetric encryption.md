# Cifrado simétrico y asimétrico

## Resumen

El **Encryption (Cifrado)** es el proceso de transformar datos legibles (**Plaintext**) en información codificada (**Ciphertext**) para evitar que personas no autorizadas puedan acceder a ellos.

Existen dos tipos principales de cifrado:

* **Symmetric Encryption (Cifrado simétrico):** utiliza una única clave secreta para cifrar y descifrar la información.
* **Asymmetric Encryption (Cifrado asimétrico):** utiliza un par de claves, una **Public Key (Clave pública)** y una **Private Key (Clave privada)**.

El cifrado es fundamental para proteger la **Confidentiality** de la información y forma parte de tecnologías como **PKI**, certificados digitales y comunicaciones seguras.

## Cifrado simétrico

El **Symmetric Encryption** utiliza la misma clave para cifrar y descifrar los datos.

Esto significa que el emisor y el receptor necesitan conocer la misma clave secreta.

### Ventajas y desventajas

**Ventaja principal:**

* Es rápido y eficiente para cifrar grandes cantidades de información.

**Desventaja principal:**

* La clave secreta debe compartirse de forma segura entre las partes.

### Algoritmos importantes

* **AES (Advanced Encryption Standard):** uno de los principales algoritmos simétricos utilizados actualmente. Puede utilizar claves de 128, 192 o 256 bits.
* **3DES (Triple DES):** aplica DES tres veces y utiliza claves más largas. Actualmente está siendo reemplazado debido a sus limitaciones y menor eficiencia.

## Cifrado asimétrico

El **Asymmetric Encryption** utiliza dos claves relacionadas matemáticamente:

* **Public Key:** puede compartirse públicamente.
* **Private Key:** debe mantenerse secreta y protegida.

La clave pública y la privada trabajan juntas para proporcionar mecanismos de cifrado, autenticación y firmas digitales.

### Algoritmos importantes

* **RSA (Rivest Shamir Adleman):** uno de los algoritmos asimétricos más conocidos. Utiliza pares de claves y se emplea en diferentes sistemas de seguridad y PKI.
* **DSA (Digital Signature Algorithm):** algoritmo utilizado principalmente para generar y verificar firmas digitales.

El cifrado asimétrico requiere más procesamiento que el simétrico, por lo que normalmente no se utiliza para cifrar grandes cantidades de datos directamente.

## Longitud de las claves

La **Key Length (Longitud de clave)** influye en la resistencia de un sistema criptográfico frente a ataques de fuerza bruta.

Un atacante puede intentar diferentes combinaciones hasta encontrar la clave correcta.

En general:

* Claves más largas → mayor cantidad de combinaciones posibles.
* Claves más cortas → menor seguridad frente a fuerza bruta, aunque pueden ser más rápidas.

Por esto, los sistemas criptográficos deben buscar un equilibrio entre **Security (Seguridad)** y **Performance (Rendimiento)**.

## Uso combinado del cifrado

En aplicaciones reales es común utilizar **cifrado simétrico y asimétrico en conjunto**.

Una forma simplificada de entenderlo es:

1. La criptografía asimétrica permite establecer o proteger una clave de sesión.
2. Una vez establecida la comunicación, se utiliza cifrado simétrico para proteger los datos.
3. El cifrado simétrico permite transmitir grandes cantidades de información de forma eficiente.

Este enfoque permite combinar la seguridad de la criptografía asimétrica con la velocidad del cifrado simétrico.

## PKI y OpenSSL

La **Public Key Infrastructure (PKI)** es un conjunto de tecnologías, procesos y componentes utilizados para gestionar claves públicas, claves privadas y certificados digitales.

**OpenSSL** es una herramienta de código abierto que permite trabajar con diferentes funciones criptográficas, incluyendo la generación y gestión de claves y certificados.

Un concepto importante relacionado con OpenSSL es **Heartbleed**, una vulnerabilidad que afectó a determinadas versiones de OpenSSL y demostró la importancia de mantener el software actualizado y aplicar parches de seguridad.

## Principio de Kerckhoffs

El **Principle of Kerckhoffs (Principio de Kerckhoffs)** establece que la seguridad de un sistema criptográfico no debería depender de mantener secreto el funcionamiento del algoritmo.

En otras palabras:

> Un sistema criptográfico debería seguir siendo seguro aunque el funcionamiento del algoritmo sea conocido.

Lo que debe mantenerse secreto es principalmente la **clave criptográfica**.

Esto se relaciona con una idea fundamental de ciberseguridad:

**Security through obscurity (Seguridad por oscuridad)** no debería utilizarse como mecanismo principal de protección.

## Puntos clave

* **Symmetric Encryption** utiliza una sola clave secreta.
* **Asymmetric Encryption** utiliza una clave pública y una privada.
* **AES** es uno de los principales algoritmos simétricos modernos.
* **RSA** es uno de los algoritmos asimétricos más conocidos.
* Las claves más largas generalmente ofrecen mayor resistencia frente a ataques de fuerza bruta.
* La criptografía simétrica es más rápida, mientras que la asimétrica requiere más procesamiento.
* Ambos tipos de cifrado pueden utilizarse conjuntamente en sistemas reales.
* **PKI** permite gestionar claves públicas, privadas y certificados digitales.
* **OpenSSL** es una herramienta importante para trabajar con criptografía y certificados.
* El **Principio de Kerckhoffs** indica que la seguridad no debe depender de ocultar el funcionamiento del algoritmo.
