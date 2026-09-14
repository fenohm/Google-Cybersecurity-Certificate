# 🐧 Arquitectura de Linux

La arquitectura de Linux está formada por varios componentes que trabajan en conjunto para permitir que el usuario interactúe con el hardware. Comprender esta estructura es importante en ciberseguridad, ya que facilita entender cómo funcionan los sistemas y cómo se gestionan sus recursos.

El flujo general de una tarea en Linux puede representarse como:

Usuario → Aplicaciones → Shell → FHS → Kernel → Hardware

# 🔹 Componentes principales
Usuario: Persona que interactúa con el sistema. Linux es un sistema multiusuario, permitiendo que varios usuarios compartan recursos.
Aplicaciones: Programas destinados a realizar tareas específicas. En Linux pueden instalarse y administrarse mediante gestores de paquetes.
Shell: Interfaz que permite al usuario comunicarse con el sistema mediante comandos de texto. Actúa como intermediario entre el usuario y el kernel.
FHS (Filesystem Hierarchy Standard): Estándar que define cómo se organizan los archivos y directorios dentro de Linux, indicando dónde se almacena cada tipo de información.
Kernel: Núcleo del sistema operativo. Gestiona procesos, memoria y recursos, además de comunicarse con el hardware y las aplicaciones.
Hardware: Componentes físicos de la computadora que permiten ejecutar el sistema.

# 💻 Hardware

El hardware se divide principalmente en:

Periféricos: Dispositivos conectados al computador, como teclado, ratón, monitor e impresora.
Hardware interno: Componentes fundamentales como la CPU, RAM, placa madre y almacenamiento.

La CPU ejecuta las instrucciones de los programas, la RAM almacena temporalmente los datos mientras se están utilizando y el disco duro/SSD almacena archivos y programas de forma permanente.
