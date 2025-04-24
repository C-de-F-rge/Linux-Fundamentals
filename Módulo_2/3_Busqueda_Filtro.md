[_Volver Al Capitulo Anterior_](/Módulo_2/2_Manipulación.md)
---
# 🔍 Búsqueda y filtrado en Linux

## 📁 find — Búsqueda recursiva en tiempo real

### Descripción: 
Busca archivos y directorios en tiempo real, permitiendo filtrar por nombre, tipo, tamaño, fecha, permisos, entre otros.
### Sintaxis:
```bash
find [ruta] [condiciones] [acciones]
```
### Ejemplos:
```bash
# Buscar archivos llamados "config.json" en todo el sistema
find / -name "config.json"

# Buscar archivos modificados en los últimos 7 días
find /var/www -type f -mtime -7

# Buscar archivos mayores de 100 MB
find . -type f -size +100M

# Buscar archivos y cambiar sus permisos
find . -type f -name "*.sh" -exec chmod +x {} \;
```
---
## 🧾 grep — Filtrado de texto por patrones

### Descripción:
Busca líneas que coincidan con un patrón en archivos o en la salida de otros comandos
### Sintaxis:
```bash
grep [opciones] "patrón" [archivo]
```
### Ejemplos:
```bash
# Buscar la palabra "error" en un archivo de log
grep "error" /var/log/syslog

# Búsqueda sin distinguir mayúsculas/minúsculas
grep -i "warning" app.log

# Mostrar líneas que no contienen el patrón
grep -v "DEBUG" app.log

# Buscar recursivamente en archivos .php
grep -r "mysqli_connect" .

# Contar coincidencias
grep -c "timeout" server.log
```

---
## ⚡ locate — Búsqueda rápida basada en base de datos

### Descripción:
Busca archivos utilizando una base de datos indexada, lo que permite obtener resultados rápidamente.
### Sintaxis:
```bash
locate [opciones] "nombre_archivo"
```
### Ejemplos:
```bash
# Buscar todos los archivos que contienen "nginx"
locate nginx

# Buscar archivos .conf
locate "*.conf"

# Actualizar la base de datos (requiere permisos de superusuario)
sudo updatedb
```
---
## 📌 which — Ubicación de ejecutables en el PATH

### Descripción:
Muestra la ruta completa del ejecutable de un comando, según las rutas definidas en la variable de entorno PATH.
### Sintaxis:
```bash
which [comando]
```
### Ejemplos:
```bash
# Ver la ruta de Python
which python3

# Ver la ruta de Docker
which docker
```
---
[_Siguiente Capítulo_](/Módulo_2/4_Permisos&Usuario.md)