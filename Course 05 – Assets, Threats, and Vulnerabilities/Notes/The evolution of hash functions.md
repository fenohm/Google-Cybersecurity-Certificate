# La evolución de las funciones hash

## Resumen

Las **Hash Functions (Funciones hash)** son algoritmos que transforman datos de cualquier tamaño en un valor de longitud fija llamado **Hash** o **Digest**.

Se utilizan principalmente para verificar la **integridad de los datos**, autenticación y mecanismos relacionados con el **no repudio**.

Una característica importante es que un pequeño cambio en los datos originales produce un hash completamente diferente.

### MD5 y las colisiones

Uno de los algoritmos hash más conocidos es **MD5 (Message Digest 5)**, que genera un valor de 128 bits, normalmente representado como una cadena de 32 caracteres hexadecimales.

Con el tiempo, MD5 demostró ser vulnerable debido a las **Hash Collisions (Colisiones de hash)**.

Una colisión ocurre cuando dos entradas diferentes producen exactamente el mismo hash.

Esto representa un problema de seguridad porque un atacante podría intentar crear datos maliciosos que produzcan el mismo hash que información legítima.

Por esta razón, **MD5 ya no debe utilizarse para proteger información sensible o contraseñas**.

### SHA y funciones hash más seguras

Para mejorar la resistencia frente a colisiones surgió la familia **SHA (Secure Hash Algorithm)**.

Entre sus principales variantes se encuentran:

* **SHA-1:** genera un hash de 160 bits. Actualmente no se considera seguro para aplicaciones que requieren resistencia a colisiones.
* **SHA-224:** genera un hash de 224 bits.
* **SHA-256:** genera un hash de 256 bits y es ampliamente utilizado.
* **SHA-384:** genera un hash de 384 bits.
* **SHA-512:** genera un hash de 512 bits.

En general, un tamaño de salida mayor proporciona una mayor resistencia frente a ciertos ataques de fuerza bruta y colisiones, aunque la seguridad también depende del algoritmo utilizado.

## Protección de contraseñas

Las contraseñas **no deberían almacenarse en texto plano** en una base de datos.

En su lugar, se utilizan mecanismos de hashing para almacenar una representación que dificulte recuperar la contraseña original si la base de datos es comprometida.

Sin embargo, utilizar únicamente una función hash rápida no es suficiente para proteger contraseñas.

### Rainbow Tables

Una **Rainbow Table (Tabla rainbow)** contiene valores hash previamente calculados junto con sus posibles valores originales.

Los atacantes pueden utilizarlas para buscar coincidencias entre los hashes robados y contraseñas conocidas o comunes.

Esto es especialmente efectivo contra contraseñas débiles y hashes rápidos como MD5.

### Salting

El **Salting (Uso de salt)** consiste en añadir una cadena aleatoria de datos a una contraseña antes de aplicar el hash.

Por ejemplo:

```text
Contraseña + Salt → Hash
```

Cada contraseña debe utilizar un **Salt** diferente.

Esto hace que dos usuarios con la misma contraseña puedan tener hashes completamente diferentes y dificulta considerablemente el uso de **Rainbow Tables**.

El salt no necesita mantenerse secreto; su objetivo principal es evitar que los atacantes puedan reutilizar fácilmente hashes precalculados.

## Hashing para integridad

Las funciones hash también se utilizan para comprobar la **integridad de archivos**.

Por ejemplo:

1. Se calcula el hash de un archivo original.
2. Se descarga o transfiere el archivo.
3. Se calcula nuevamente el hash.
4. Se comparan ambos valores.
5. Si coinciden, existe una alta probabilidad de que el contenido no haya cambiado.

Esto permite detectar modificaciones accidentales o maliciosas en archivos, programas y documentos.

## Puntos clave

* **Hash Functions** convierten datos en valores de longitud fija.
* El hashing es diferente del cifrado: un hash no está diseñado para ser descifrado.
* **MD5** es un algoritmo antiguo que presenta vulnerabilidades y no debe utilizarse para proteger información sensible.
* Una **Hash Collision** ocurre cuando diferentes entradas producen el mismo hash.
* **SHA-256** y otras variantes modernas ofrecen una mayor resistencia que MD5.
* Las contraseñas no deben almacenarse en texto plano.
* Las **Rainbow Tables** permiten buscar contraseñas a partir de hashes previamente calculados.
* El **Salting** añade datos aleatorios antes de realizar el hash y ayuda a proteger contra Rainbow Tables.
* Los hashes también permiten verificar la **integridad de archivos**.
