[_Volver Al Capitulo Anterior_](/Módulo_1/3_Estructura.md)
---

# Navegación en el sistema de archivos (`cd`, `ls`, `pwd`, etc.)

## cd (change directory)
**Descripción:** Cambia el directorio de trabajo actual al que indiques. Por defecto, sin argumentos, te lleva al home del usuario. 

### Sintaxis:
```bash
cd [ruta_del_directorio]
```


### Ejemplos:
```bash
# Ir al directorio /var/log
cd /var/log

# Volver al directorio home
cd

# Subir un nivel (al padre)
cd ..

# Ir al directorio anterior
cd -
```
---
## ls (list)
**Descripción:** Lista archivos y carpetas en el directorio indicado (por defecto, el actual). Soporta múltiples opciones para ver detalles, ocultos, ordenar, etc. 

### Sintaxis:
```bash
ls [opciones] [ruta]
```
### Ejemplos:
```bash
# Listado simple
ls

# Listado detallado (permisos, dueño, tamaño, fecha)
ls -l

# Incluir archivos ocultos (comienzan con .)
ls -a

# Listado detallado y en formato legible (KB/MB)
ls -lh

# Listar por fecha de modificación, el más reciente primero
ls -lt
```
---
## pwd (print working directory)
**Descripción:** Muestra la ruta completa del directorio de trabajo actual, desde la raíz (/). Es útil para orientarte en la jerarquía de carpetas.

### Sintaxis:
```bash
pwd
```
### Ejemplos:
```bash
$ pwd
/home/yoi/proyecto
```
---
## pushd
**Descripción:** guarda tu directorio actual en una pila y cambia al directorio indicado

### Sintaxis:
```bash
pushd [ruta]
```
### Ejemplos:
```bash
# Estoy en /home/yoi
pushd /var/log
# Ahora estoy en /var/log y /home/yoi queda en la pila
```
---
## 🌳 tree (vista en forma de árbol)
**Descripción:** muestra recursivamente el contenido de directorios en un formato jerárquico indentado

### Sintaxis:
```bash
tree [opciones] [ruta]
```
### Ejemplos:
```bash
# Árbol completo del directorio actual
tree

# Sólo un nivel de profundidad
tree -L 1

# Incluir archivos ocultos
tree -a
```
---
## 🔍 find (búsqueda avanzada de archivos)
**Descripción:** 

### Sintaxis:
```bash
find [ruta] [condiciones] [acciones]
```
### Ejemplos:
```bash
# Buscar por nombre en el directorio actual
find . -name "archivo.txt"

# Buscar (insensible a mayúsculas)
find /home/yoi -iname "*log*"

# Buscar archivos mayores de 10MB
find /var -size +10M

# Ejecutar comando sobre cada resultado
find . -type f -name "*.sh" -exec chmod +x {} \;
```
---
[_Siguiente Capítulo_](/Módulo_2/2_Manipulación.md)