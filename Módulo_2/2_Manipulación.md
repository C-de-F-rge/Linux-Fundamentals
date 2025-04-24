[_Volver Al Capitulo Anterior_](/Módulo_2/1_Navegación.md)
---
# Manipulación de archivos y directorios (`cp`, `mv`, `rm`, `mkdir`, `touch`)

## 📋 cp (copy)
Copia archivos o directorios de una ubicación a otra.

### Sintaxis:
```bash
cp [opciones] <origen> <destino>

```

### Opciones comunes:
| **Opción** | **Descripción** |
| `-r` | copia directorios de forma recursiva. |
| `-v` | muestra los archivos a medida que se copian (“verbose”). |
| `-b` | crea una copia de seguridad de archivos existentes. |

### Ejemplos:
```bash
# Copiar archivo.txt a backup.txt
cp archivo.txt backup.txt

# Copiar todo el directorio src/ a dest/ recursivamente
cp -r src/ dest/

# Copiar con detalles y copia de seguridad .bak
cp -v -b -S .bak config.cfg /respaldos/
```
---
## 🚚 mv (move/rename)
Mueve o renombra archivos y directorios.

### Sintaxis:
```bash
mv [opciones] <origen> <destino>
```

### Opciones comunes:
| **Opción** | **Descripción** |
| `-i` | pide confirmación antes de sobrescribir. |
| `-v` | muestra los archivos procesados. |
### Ejemplos:
```bash
# Renombrar archivo
mv viejo.txt nuevo.txt

# Mover varios archivos a carpeta backups/
mv *.log backups/  

# Mover con confirmación
mv -i datos.csv /mnt/storage/
```
---
## ❌ rm (remove)
Elimina archivos o directorios. ¡Cuidado! no hay papelera.

### Sintaxis:
```bash
rm [opciones] <archivo_o_directorio>
```

### Opciones comunes:
| **Opción** | **Descripción** |
| `-r` | elimina directorios y su contenido recursivamente. |
| `-f` | fuerza la eliminación sin preguntar.  |
| `-i` | pide confirmación antes de cada eliminación.  |
### Ejemplos:
```bash
# Eliminar un archivo
rm temp.txt

# Eliminar un directorio y todo su contenido
rm -r old_project/

# Eliminar todos los .log pidiendo confirmación
rm -i *.log
```
---
## 📁 mkdir (make directory)
Crea uno o varios directorios nuevos.

### Sintaxis:
```bash
mkdir [opciones] <directorio1> [directorio2 ...]
```

### Opciones comunes:
| **Opción** | **Descripción** |
| `-p` | rea padres necesarios sin error si ya existen. |
| `-m <modo>` | asigna permisos al crear.  |
### Ejemplos:
```bash
# Crear un directorio
mkdir proyectos

# Crear estructura de subdirectorios
mkdir -p proyectos/2025/abril

# Crear varios a la vez
mkdir docs logs backups
```
---
## 🕓 touch
Crea archivos vacíos o actualiza timestamps de existentes.

### Sintaxis:
```bash
touch [opciones] <archivo1> [archivo2 ...]
```

### Opciones comunes:
| **Opción** | **Descripción** |
| `-c` | no crea archivo si no existe. |
| `-a/-m` | cambia solo access o modification time.  |
### Ejemplos:
```bash
# Crear un archivo vacío
touch nuevo.txt

# Crear múltiples archivos
touch a.txt b.txt c.txt

# Actualizar timestamp sin crear
touch -c existente.log
```
---
[_Siguiente Capítulo_](/Módulo_2/3_Busqueda_Filtro.md)