## Uso responsable de `sudo` y gestión de usuarios en Linux

En este contenido aprendí a utilizar de forma segura `sudo` para ejecutar comandos con **privilegios elevados**, evitando trabajar directamente con la cuenta `root`. Esto permite aplicar el principio de **mínimo privilegio**, reduciendo los riesgos asociados a accesos administrativos.

También reforcé conceptos de **autenticación y autorización** y aprendí a gestionar usuarios, grupos y permisos mediante comandos de Linux:

* `sudo`: ejecución temporal de comandos con privilegios elevados.
* `useradd`: creación de nuevos usuarios y asignación de grupos.
* `usermod`: modificación de cuentas, grupos, directorios y bloqueo de usuarios.
* `userdel`: eliminación de cuentas de usuario, con precaución al utilizar `-r`.
* `chown`: modificación del propietario de archivos y directorios.

Un aspecto importante es utilizar `sudo` únicamente cuando sea necesario y revisar cuidadosamente los comandos antes de ejecutarlos, especialmente cuando provienen de fuentes externas.

### Conceptos clave

* **Autenticación:** proceso de verificar la identidad de un usuario.
* **Autorización:** proceso de determinar qué recursos puede utilizar un usuario.
* **Privilegios elevados:** permisos que permiten realizar acciones administrativas sobre el sistema.
* **Principio de mínimo privilegio:** otorgar únicamente los permisos necesarios para realizar una tarea.
