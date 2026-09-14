# Comandos de permisos en Linux

Los **permisos de Linux** permiten controlar quién puede leer, modificar o ejecutar archivos y directorios. Para un analista de ciberseguridad, comprender y administrar estos permisos es fundamental para proteger la información y aplicar el **principio de privilegio mínimo**.

## Permisos en Linux

Los permisos se representan mediante una cadena de **10 caracteres**, por ejemplo:

```text
-rwxrwxrwx
```

El primer carácter indica el tipo de elemento:

* `d` → directorio.
* `-` → archivo regular.

Los siguientes nueve caracteres representan los permisos de:

* **Usuario (`u`)** → propietario del archivo.
* **Grupo (`g`)** → grupo al que pertenece el propietario.
* **Otros (`o`)** → todos los demás usuarios.

Cada grupo puede tener tres permisos:

| Permiso     | Símbolo | Función                                               |
| ----------- | ------- | ----------------------------------------------------- |
| Lectura     | `r`     | Permite leer el contenido                             |
| Escritura   | `w`     | Permite modificar el contenido                        |
| Ejecución   | `x`     | Permite ejecutar un archivo o acceder a un directorio |
| Sin permiso | `-`     | No se concede ese permiso                             |

Por ejemplo:

```text
-rwxr-xr--
```

Se puede interpretar como:

* Usuario: `rwx` → lectura, escritura y ejecución.
* Grupo: `r-x` → lectura y ejecución.
* Otros: `r--` → solamente lectura.

---

## Comando `ls`

El comando `ls` permite visualizar archivos y directorios. Con determinadas opciones también permite analizar sus permisos.

### `ls -a`

Muestra todos los archivos, incluyendo los **archivos ocultos**, que normalmente comienzan con `.`.

```bash
ls -a
```

### `ls -l`

Muestra información detallada, incluyendo:

* Permisos.
* Propietario.
* Grupo.
* Tamaño.
* Fecha de modificación.
* Nombre del archivo o directorio.

```bash
ls -l
```

### `ls -la`

Combina ambas opciones y muestra información detallada de todos los archivos, incluidos los ocultos.

```bash
ls -la
```

---

## Modificación de permisos con `chmod`

El comando `chmod` permite **cambiar los permisos** de archivos y directorios.

Su estructura básica es:

```bash
chmod <permisos> <archivo>
```

### Añadir permisos

El operador `+` agrega permisos.

```bash
chmod u+rwx,g+rwx,o+rwx login_sessions.txt
```

En este caso se agregan permisos de lectura, escritura y ejecución al usuario, grupo y otros.

### Eliminar permisos

El operador `-` elimina permisos.

```bash
chmod u-rwx,g-rwx,o-rwx login_sessions.txt
```

### Asignar permisos

El operador `=` establece exactamente los permisos especificados.

```bash
chmod u=r,g=r,o=r login_sessions.txt
```

Esto elimina cualquier permiso adicional que existiera y deja únicamente el permiso de lectura para usuario, grupo y otros.

---

## Sintaxis de `chmod`

| Símbolo | Significado                 |
| ------- | --------------------------- |
| `u`     | Usuario/propietario         |
| `g`     | Grupo                       |
| `o`     | Otros usuarios              |
| `+`     | Añadir permisos             |
| `-`     | Eliminar permisos           |
| `=`     | Establecer permisos exactos |
| `r`     | Lectura                     |
| `w`     | Escritura                   |
| `x`     | Ejecución                   |

Cuando se modifican diferentes tipos de propietarios, se utilizan comas:

```bash
chmod u+rw,g+r,o-r archivo.txt
```

---

## Principio de privilegio mínimo

El **principio de privilegio mínimo (PoLP)** establece que cada usuario debe disponer únicamente de los permisos necesarios para realizar sus funciones.

Conceder permisos innecesarios puede aumentar el riesgo de:

* Acceso no autorizado.
* Modificación de información.
* Eliminación de archivos.
* Exposición de información confidencial.
* Compromiso del sistema.

### Ejemplo práctico

Supongamos que un archivo confidencial llamado `bonuses.txt` tiene los siguientes permisos:

```text
-rw-rw----
```

El propietario tiene lectura y escritura, pero el grupo también tiene estos permisos.

Si únicamente el propietario necesita acceder al archivo, se pueden eliminar los permisos del grupo:

```bash
chmod g-rw bonuses.txt
```

Después del cambio, el archivo quedaría:

```text
-rw-------
```

De esta manera, se reduce el acceso al mínimo necesario.

---

## Aplicación en ciberseguridad

El análisis y configuración correcta de permisos es una tarea importante para un analista de seguridad. Los comandos `ls -l`, `ls -la` y `chmod` permiten **auditar y modificar los permisos**, ayudando a proteger archivos sensibles y reducir accesos innecesarios.

### Comandos principales

| Comando       | Función                                          |
| ------------- | ------------------------------------------------ |
| `ls -a`       | Muestra archivos ocultos                         |
| `ls -l`       | Muestra permisos e información detallada         |
| `ls -la`      | Muestra información detallada incluyendo ocultos |
| `chmod`       | Modifica permisos                                |
| `chmod u+...` | Añade permisos al usuario                        |
| `chmod g-...` | Elimina permisos del grupo                       |
| `chmod o=...` | Establece permisos para otros                    |

**Conclusión:** comprender los permisos de Linux y utilizar correctamente `chmod` permite controlar el acceso a archivos y directorios, aplicar el **principio de privilegio mínimo** y reducir posibles riesgos de seguridad.
