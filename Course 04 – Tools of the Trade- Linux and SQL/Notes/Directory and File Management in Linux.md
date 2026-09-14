# Gestión de directorios y archivos en Linux

La gestión de archivos y directorios es una habilidad fundamental para los analistas de ciberseguridad. Linux proporciona distintos comandos para **crear, eliminar, mover, copiar y modificar archivos y directorios** directamente desde el shell.

## Gestión de directorios

### `mkdir`

El comando `mkdir` permite crear nuevos directorios.

```bash
mkdir network
mkdir /home/analyst/logs/network
```

Puede utilizarse tanto con **rutas relativas** como con **rutas absolutas**.

Para comprobar que el directorio fue creado correctamente:

```bash
ls
```

### `rmdir`

Permite eliminar directorios **vacíos**.

```bash
rmdir network
```

`rmdir` no puede eliminar un directorio que contenga archivos o subdirectorios.

---

## Gestión de archivos

### `touch`

Crea un archivo vacío.

```bash
touch permissions.txt
```

### `rm`

Elimina archivos del sistema.

```bash
rm permissions.txt
```

> ⚠️ `rm` debe utilizarse con cuidado, ya que los archivos eliminados pueden ser difíciles de recuperar.

### `mv`

Permite **mover o renombrar** archivos y directorios.

Para mover un archivo:

```bash
mv permissions.txt /home/analyst/logs
```

Para cambiar su nombre:

```bash
mv permissions.txt perm.txt
```

Al mover un archivo, este deja de existir en su ubicación original.

### `cp`

Copia archivos o directorios sin eliminar el original.

```bash
cp permissions.txt /home/analyst/logs
```

### Diferencia entre `mv` y `cp`

| Comando | Función                                           |
| ------- | ------------------------------------------------- |
| `mv`    | Mueve o renombra archivos/directorios             |
| `cp`    | Copia archivos/directorios y mantiene el original |

---

## Editor de texto `nano`

`nano` es un editor de texto que funciona directamente desde la terminal y está disponible en muchas distribuciones Linux.

Para abrir un archivo existente:

```bash
nano permissions.txt
```

También permite crear un archivo nuevo:

```bash
nano authorized_users.txt
```

### Atajos importantes

| Atajo      | Función         |
| ---------- | --------------- |
| `Ctrl + O` | Guardar archivo |
| `Ctrl + X` | Salir de nano   |

A diferencia de algunos editores, `nano` no guarda automáticamente los cambios, por lo que es importante guardar el archivo antes de salir.

Otros editores de texto de terminal populares son **Vim** y **Emacs**.

---

## Redirección de salida

Linux permite redirigir la salida de un comando hacia un archivo utilizando los operadores `>` y `>>`.

### `>`

Redirige la salida y **sobrescribe** el contenido existente del archivo.

```bash
echo "time" > permissions.txt
```

Si el archivo no existe, se crea automáticamente.

> ⚠️ `>` debe utilizarse con cuidado, ya que sobrescribe el contenido anterior.

### `>>`

Redirige la salida y **añade** el contenido al final del archivo sin eliminar lo que ya existe.

```bash
echo "last updated date" >> permissions.txt
```

Si el archivo no existe, también se crea automáticamente.

### Diferencia entre `>` y `>>`

| Operador | Función                                           |
| -------- | ------------------------------------------------- |
| `>`      | Sobrescribe el archivo                            |
| `>>`     | Añade contenido al final                          |
| `\|`     | Envía la salida de un comando como entrada a otro |

---

## Comandos principales

| Comando | Función                                      |
| ------- | -------------------------------------------- |
| `mkdir` | Crea directorios                             |
| `rmdir` | Elimina directorios vacíos                   |
| `touch` | Crea archivos vacíos                         |
| `rm`    | Elimina archivos                             |
| `mv`    | Mueve o renombra archivos/directorios        |
| `cp`    | Copia archivos/directorios                   |
| `nano`  | Editor de texto desde la terminal            |
| `echo`  | Muestra o genera texto                       |
| `>`     | Sobrescribe/redirige salida a un archivo     |
| `>>`    | Añade/redirige salida al final de un archivo |

## Aplicación en ciberseguridad

Estos comandos son fundamentales para la administración y análisis de sistemas Linux. Un analista de seguridad puede utilizarlos para **organizar archivos de logs, crear estructuras de directorios, realizar copias, mover evidencias, modificar archivos de configuración y almacenar información obtenida durante una investigación**.

**Conclusión:** conocer la gestión de archivos y directorios mediante la terminal permite trabajar de forma más eficiente con sistemas Linux y constituye una base importante para tareas de **administración, análisis e investigación en ciberseguridad**.
