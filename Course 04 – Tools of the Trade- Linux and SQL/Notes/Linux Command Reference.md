# 🐧 Referencia de comandos Linux

Guía de comandos fundamentales de Linux estudiados en el **Google Cybersecurity Certificate**.

---

## 📁 Navegar por el sistema de archivos

| Comando  | Descripción                                                                                                                 |
| -------- | --------------------------------------------------------------------------------------------------------------------------- |
| `cd`     | Permite desplazarse entre directorios.                                                                                      |
| `cd ..`  | Permite subir un nivel desde el directorio actual.                                                                          |
| `ls`     | Muestra los archivos y directorios de una ubicación.                                                                        |
| `ls -a`  | Muestra también los archivos ocultos.                                                                                       |
| `ls -l`  | Muestra los archivos y directorios junto con información como permisos, propietario, grupo, tamaño y fecha de modificación. |
| `ls -la` | Combina la información detallada de `ls -l` con la visualización de archivos ocultos.                                       |
| `pwd`    | Muestra la ruta del directorio de trabajo actual.                                                                           |
| `whoami` | Muestra el nombre del usuario que está actualmente conectado.                                                               |

---

## 📄 Leer archivos

| Comando   | Descripción                                                                           |
| --------- | ------------------------------------------------------------------------------------- |
| `cat`     | Muestra directamente el contenido de un archivo.                                      |
| `head`    | Muestra las primeras 10 líneas de un archivo por defecto.                             |
| `head -n` | Permite especificar cuántas líneas iniciales se desean mostrar.                       |
| `less`    | Permite visualizar el contenido de un archivo página por página y desplazarse por él. |
| `tail`    | Muestra las últimas 10 líneas de un archivo por defecto.                              |
| `tail -n` | Permite especificar cuántas líneas finales se desean mostrar.                         |

---

## 🗂️ Administrar el sistema de archivos

| Comando | Descripción                                                                                                    |
| ------- | -------------------------------------------------------------------------------------------------------------- |
| `cp`    | Copia un archivo o directorio a una nueva ubicación sin eliminar el original.                                  |
| `mkdir` | Crea un nuevo directorio.                                                                                      |
| `mv`    | Mueve un archivo o directorio a otra ubicación. También puede utilizarse para cambiar el nombre de un archivo. |
| `nano`  | Abre o crea archivos utilizando el editor de texto Nano desde la terminal.                                     |
| `rm`    | Elimina un archivo.                                                                                            |
| `rmdir` | Elimina un directorio, siempre que esté vacío.                                                                 |
| `touch` | Crea un archivo nuevo.                                                                                         |

### Diferencia entre `rm` y `rmdir`

* `rm` → elimina **archivos**.
* `rmdir` → elimina **directorios vacíos**.

---

## 🔎 Filtrar contenido

| Comando       | Descripción                                                                                                     |                                                                                                                        |
| ------------- | --------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `find`        | Busca archivos y directorios que cumplan determinados criterios.                                                |                                                                                                                        |
| `find -name`  | Busca archivos o directorios cuyo nombre coincida con un patrón específico, respetando mayúsculas y minúsculas. |                                                                                                                        |
| `find -iname` | Busca archivos o directorios por nombre sin distinguir entre mayúsculas y minúsculas.                           |                                                                                                                        |
| `find -mtime` | Busca archivos o directorios según el tiempo transcurrido desde su última modificación, expresado en días.      |                                                                                                                        |
| `find -mmin`  | Busca archivos o directorios según el tiempo transcurrido desde su última modificación, expresado en minutos.   |                                                                                                                        |
| `grep`        | Busca una cadena específica dentro de un archivo y muestra las líneas donde aparece.                            |                                                                                                                        |
| `(piping)`    | Envía la salida de un comando como entrada para otro comando, permitiendo combinar comandos para procesar información. |

**Ejemplo:**

```bash
ls /home/analyst/reports | grep users
```

Este comando busca dentro de la salida de `ls` los archivos o directorios que contienen `users` en su nombre.

---

## 👤 Gestionar usuarios y permisos

| Comando    | Descripción                                                                                                            |
| ---------- | ---------------------------------------------------------------------------------------------------------------------- |
| `chmod`    | Modifica los permisos de archivos y directorios.                                                                       |
| `chown`    | Cambia el propietario de un archivo o directorio. Se utiliza normalmente con `sudo`.                                   |
| `groupdel` | Elimina un grupo del sistema. Se utiliza con `sudo`.                                                                   |
| `sudo`     | Concede temporalmente privilegios elevados a usuarios autorizados para ejecutar determinados comandos administrativos. |
| `useradd`  | Crea un nuevo usuario en el sistema. Se utiliza con `sudo`.                                                            |
| `userdel`  | Elimina un usuario del sistema. Se utiliza con `sudo`.                                                                 |
| `usermod`  | Modifica una cuenta de usuario existente. Se utiliza con `sudo`.                                                       |

### Opciones importantes

| Opción | Comando               | Descripción                                                                                                     |
| ------ | --------------------- | --------------------------------------------------------------------------------------------------------------- |
| `-g`   | `useradd` / `usermod` | Establece o modifica el grupo primario del usuario.                                                             |
| `-G`   | `useradd` / `usermod` | Asigna grupos suplementarios al usuario.                                                                        |
| `-a`   | `usermod`             | Añade el usuario a un grupo sin eliminar los grupos suplementarios existentes cuando se utiliza junto con `-G`. |
| `-d`   | `usermod`             | Cambia el directorio personal del usuario.                                                                      |
| `-l`   | `usermod`             | Cambia el nombre de inicio de sesión del usuario.                                                               |
| `-L`   | `usermod`             | Bloquea una cuenta para impedir que el usuario inicie sesión.                                                   |
| `-r`   | `userdel`             | Elimina al usuario y también los archivos de su directorio personal.                                            |

### Ejemplos

```bash
sudo useradd fgarcia
```

Crea el usuario `fgarcia`.

```bash
sudo useradd -g security fgarcia
```

Crea `fgarcia` y establece `security` como su grupo primario.

```bash
sudo useradd -G finance,admin fgarcia
```

Crea `fgarcia` y lo añade a los grupos suplementarios `finance` y `admin`.

```bash
sudo usermod -a -G marketing fgarcia
```

Añade `fgarcia` al grupo `marketing` sin eliminar sus grupos suplementarios existentes.

```bash
sudo usermod -L fgarcia
```

Bloquea la cuenta de `fgarcia` para impedir su inicio de sesión.

```bash
sudo userdel fgarcia
```

Elimina al usuario `fgarcia`.

```bash
sudo userdel -r fgarcia
```

Elimina al usuario `fgarcia` y los archivos de su directorio personal.

```bash
sudo chown fgarcia access.txt
```

Cambia el propietario del archivo `access.txt` a `fgarcia`.

```bash
sudo chown :security access.txt
```

Cambia el grupo propietario de `access.txt` a `security`.

---

## 🔐 Gestión de permisos con `chmod`

`chmod` permite modificar los permisos de **lectura (`r`)**, **escritura (`w`)** y **ejecución (`x`)** para:

* `u` → usuario propietario.
* `g` → grupo.
* `o` → otros usuarios.

### Ejemplos

```bash
chmod u+rwx,g+rwx,o+rwx login_sessions.txt
```

Añade permisos de lectura, escritura y ejecución al usuario, grupo y otros usuarios.

```bash
chmod g-rw bonuses.txt
```

Elimina los permisos de lectura y escritura del grupo.

```bash
chmod u=r,g=r,o=r login_sessions.txt
```

Establece únicamente el permiso de lectura para el usuario, grupo y otros.

---

## 🆘 Obtener ayuda en Linux

| Comando      | Descripción                                                                                      |
| ------------ | ------------------------------------------------------------------------------------------------ |
| `apropos`    | Busca en las descripciones de las páginas de manual comandos relacionados con una palabra clave. |
| `apropos -a` | Busca páginas de manual que contengan todas las palabras clave especificadas.                    |
| `man`        | Muestra información detallada sobre un comando mediante su página de manual.                     |
| `whatis`     | Muestra una descripción breve de un comando en una sola línea.                                   |

### Ejemplos

```bash
apropos password
```

Busca páginas de manual relacionadas con `password`.

```bash
apropos -a graph editor
```

Busca páginas de manual que contengan tanto `graph` como `editor`.

```bash
man chown
```

Muestra información detallada sobre el funcionamiento y las opciones de `chown`.

```bash
whatis nano
```

Muestra una descripción breve del comando `nano`.

---

## 🎯 Aplicación en ciberseguridad

Estos comandos proporcionan herramientas fundamentales para trabajar con Linux en tareas de **administración de sistemas, gestión de usuarios, permisos, búsqueda de archivos y análisis de información**.

El dominio de estos comandos permite a un analista de ciberseguridad desenvolverse de forma más eficiente en entornos Linux y aplicar correctamente conceptos como **privilegios, permisos, usuarios, grupos y control de acceso**.
