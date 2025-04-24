[_Volver Al Capitulo Anterior_](/Módulo_1/2_Distribuciones.md)
---

# Estructura del sistema de archivos Linux

La jerarquía de directorios en Linux sigue el estándar `FHS` (Filesystem Hierarchy Standard), que define la ubicación y propósito de cada carpeta principal.


| **Ruta** | **Descripción Breve** |
| `/` | Raíz del sistema; punto de partida de toda la jerarquía. |
| `/bin` | Comandos esenciales para todos los usuarios (bash, ls…). |
| `/sbin` | Binarios del sistema para administración (ifconfig, fsck). |
| `/usr` | Programa y datos de usuario; contiene subdirectorios `bin`, `lib`, `share`. |
| `/usr/bin` | Aplicaciones de usuario estándar. |
| `/usr/sbin` | Herramientas de administración para usuarios avanzados. |
| `/usr/lib` | Librerías compartidas y módulos de kernel. |
| `/etc` | Archivos de configuración del sistema. |
| `/var` | Datos variables (logs, colas de correo, bases de datos ligeras). |
| `/home` | Directorios personales de usuarios. |
| `/root` | Home del usuario root (administrador). |
| `/tmp` | Archivos temporales; se limpia al reiniciar. |
| `/dev` | Archivos de dispositivo (hardware y pseudo-dispositivos). |
| `/proc` | Sistema de archivos virtual con información del kernel y procesos. |
| `/sys` | Información y control de dispositivos del kernel (sysfs). |
| `/mnt` | Punto de montaje temporal para sistemas de ficheros. |
| `/media` | Puntos de montaje para medios extraíbles (CD, USB). |


Cada uno de estos directorios cumple una función específica para mantener el sistema organizado y facilitar tanto el uso diario como tareas de administración y desarrollo.

---
[_Siguiente Capítulo_](/Módulo_2/Navegación.md)