# Evitar los ataques por inyección SQL

## Resumen

La **SQL Injection (Inyección SQL)** es un tipo de ataque que ocurre cuando una aplicación permite introducir entradas maliciosas que terminan siendo interpretadas como parte de una consulta SQL.

Un atacante puede utilizar esta vulnerabilidad para:

* Obtener información confidencial.
* Modificar o eliminar datos.
* Acceder a información sin autorización.
* Comprometer una aplicación vulnerable.

Las vulnerabilidades de inyección SQL son un tema importante dentro de la seguridad de aplicaciones y han aparecido históricamente en el **OWASP Top 10**.

## Consultas SQL

Una **SQL Query (Consulta SQL)** es una solicitud utilizada para recuperar o modificar información almacenada en una base de datos.

Las bases de datos organizan la información en **Tables (Tablas)** y SQL permite realizar operaciones como:

* **SELECT:** recuperar información.
* **INSERT:** agregar información.
* **UPDATE:** modificar información.
* **DELETE:** eliminar información.

Las aplicaciones web pueden utilizar campos de entrada, como formularios de inicio de sesión, buscadores o formularios de comentarios, para obtener información que posteriormente se utiliza en una consulta SQL.

El problema aparece cuando la aplicación no controla correctamente la entrada del usuario y permite que esta sea interpretada como código SQL.

## Categorías de SQL Injection

Existen tres categorías principales:

### In-band SQL Injection

La **In-band SQL Injection** utiliza el mismo canal para realizar el ataque y obtener los resultados.

Por ejemplo:

```text
Entrada vulnerable
       ↓
Aplicación web
       ↓
Base de datos
       ↓
Resultado malicioso
       ↓
Aplicación web
```

Es el tipo de inyección SQL más común.

### Out-of-band SQL Injection

La **Out-of-band SQL Injection** utiliza un canal diferente para ejecutar el ataque y recibir los resultados.

Este método es poco frecuente porque requiere que determinadas características estén habilitadas en el servidor objetivo.

### Inferential SQL Injection

La **Inferential SQL Injection** ocurre cuando el atacante no puede ver directamente los resultados de la consulta.

En su lugar, analiza el **comportamiento del sistema**, como mensajes de error o diferencias en las respuestas, para obtener información sobre la base de datos.

Este tipo también puede conocerse como **Blind SQL Injection**.

## Prevención de SQL Injection

La prevención depende principalmente de controlar correctamente las entradas proporcionadas por los usuarios.

### Prepared Statements

Las **Prepared Statements (Sentencias preparadas)** permiten separar los datos proporcionados por el usuario de la estructura de la consulta SQL.

Esto evita que la entrada del usuario sea interpretada directamente como parte del código SQL.

### Input Sanitization

El **Input Sanitization (Saneamiento de entradas)** consiste en eliminar o modificar elementos de una entrada que podrían ser peligrosos.

### Input Validation

La **Input Validation (Validación de entradas)** comprueba que los datos proporcionados por el usuario cumplen con el formato y las condiciones esperadas.

Por ejemplo, si un campo requiere una dirección de correo electrónico, la aplicación puede comprobar que la entrada tenga un formato válido.

Estas técnicas pueden combinarse con otros controles de seguridad para reducir el riesgo de ataques de inyección.

## Relación con ciberseguridad

La prevención de **SQL Injection** normalmente requiere colaboración entre profesionales de seguridad y desarrolladores.

Un analista de ciberseguridad debe ser capaz de:

1. Identificar entradas potencialmente vulnerables.
2. Comprender cómo una aplicación interactúa con la base de datos.
3. Analizar el riesgo asociado a la vulnerabilidad.
4. Recomendar medidas de mitigación.
5. Verificar que las correcciones sean efectivas.

Esto demuestra la importancia de aplicar **Secure Coding (Programación segura)** durante el desarrollo de aplicaciones.

## Puntos clave

* **SQL Injection** ocurre cuando una aplicación interpreta una entrada maliciosa como parte de una consulta SQL.
* Puede permitir acceder, modificar o eliminar información sin autorización.
* Las tres categorías principales son **In-band, Out-of-band e Inferential SQL Injection**.
* Las entradas de formularios, buscadores y otros campos pueden convertirse en puntos de ataque si no se validan correctamente.
* **Prepared Statements** ayudan a separar los datos de la estructura de las consultas SQL.
* **Input Sanitization** elimina o modifica entradas potencialmente peligrosas.
* **Input Validation** comprueba que las entradas cumplen con el formato esperado.
* La prevención de SQL Injection requiere combinar controles de seguridad y buenas prácticas de desarrollo.
* La colaboración entre **Cybersecurity** y **Software Development** es importante para prevenir vulnerabilidades en aplicaciones web.
