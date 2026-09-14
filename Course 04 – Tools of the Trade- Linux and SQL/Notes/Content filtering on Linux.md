# Filtrado de contenidos en Linux

El **filtrado de información** en Linux es una habilidad fundamental para los analistas de ciberseguridad, ya que permite localizar rápidamente datos específicos dentro de archivos y directorios utilizando determinados criterios.

## `grep`

El comando `grep` permite buscar una cadena de texto dentro de un archivo y mostrar únicamente las líneas que contienen dicha cadena.

```bash
grep OS updates.txt
grep error time_logs.txt
```

En estos ejemplos, `grep` busca las palabras `OS` y `error` dentro de los archivos indicados.

## Pipe `|`

El operador **pipe (`|`)** permite utilizar la salida de un comando como entrada de otro. Es especialmente útil para combinar comandos y filtrar información.

```bash
ls /home/analyst/reports | grep users
```

En este caso:

1. `ls` lista los archivos y directorios.
2. `|` envía esa salida a `grep`.
3. `grep users` muestra únicamente los elementos que contienen `users` en su nombre.

El pipe puede utilizarse con muchos otros comandos y no está limitado al filtrado.

## `find`

El comando `find` permite buscar archivos y directorios que cumplan determinados criterios, como:

* Nombre.
* Tamaño.
* Fecha de modificación.
* Otros atributos.

La estructura básica es:

```bash
find <directorio> <criterios>
```

Por ejemplo:

```bash
find /home/analyst/projects
```

Busca archivos y directorios a partir de `projects`.

### `-name` e `-iname`

Permiten buscar archivos o directorios según su nombre.

```bash
find /home/analyst/projects -name "*log*"
```

`-name` **distingue entre mayúsculas y minúsculas**, mientras que `-iname` no:

```bash
find /home/analyst/projects -iname "*log*"
```

El comodín `*` representa cero o más caracteres desconocidos. Por ejemplo, `*log*` puede coincidir con nombres como `log.txt`, `system_log.txt` o `LOGS`.

### `-mtime`

Permite buscar archivos o directorios según el tiempo transcurrido desde su última modificación.

```bash
find /home/analyst/projects -mtime -3
```

Busca elementos modificados durante los últimos 3 días.

También se pueden utilizar:

```bash
find /home/analyst/projects -mtime +1
find /home/analyst/projects -mtime -1
```

* `-mtime +1`: modificados hace más de un día.
* `-mtime -1`: modificados hace menos de un día.

Para realizar búsquedas basadas en **minutos**, se puede utilizar `-mmin`.

## Aplicación en ciberseguridad

Estas herramientas son especialmente útiles para un analista de seguridad porque permiten **reducir grandes cantidades de información y encontrar rápidamente datos relevantes**. Por ejemplo, pueden utilizarse para localizar archivos de logs, buscar mensajes de error, identificar archivos modificados recientemente o investigar determinados patrones dentro del sistema.

### Comandos principales

| Comando  | Función                                           |
| -------- | ------------------------------------------------- |
| `grep`   | Busca texto dentro de archivos                    |
| `\|`     | Envía la salida de un comando como entrada a otro |
| `find`   | Busca archivos y directorios según criterios      |
| `-name`  | Busca por nombre, distinguiendo mayúsculas        |
| `-iname` | Busca por nombre sin distinguir mayúsculas        |
| `-mtime` | Busca según fecha de modificación                 |
| `-mmin`  | Busca según minutos desde la modificación         |

**Conclusión:** `grep`, `pipe` y `find` son herramientas esenciales para **navegar, buscar y filtrar información en sistemas Linux**, especialmente durante tareas de análisis e investigación en ciberseguridad.
