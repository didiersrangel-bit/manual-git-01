# Guía Rápida de Comandos Básicos de Git y GitHub

Esta guía contiene los comandos esenciales para controlar tus versiones con Git y subir tus proyectos a GitHub.

---

## 1. Configuración Inicial
Configura tu identidad en tu computadora. Esto solo se hace la primera vez.

```bash
# Configura tu nombre de usuario global
git config --global user.name "Tu Nombre o Usuario"

# Configura tu correo electrónico (usa el mismo de GitHub)
git config --global user.email "tu-correo@ejemplo.com"

# Verifica la configuración guardada
git config --list
```

---

## 2. Iniciar y Clonar Proyectos
Comandos para crear un repositorio local o traer uno existente desde GitHub.

```bash
# Inicializa un repositorio Git local en la carpeta actual
git init

# Descarga un proyecto existente desde GitHub a tu computadora
git clone https://github.com
```

---

## 3. El Flujo de Trabajo Básico (Guardar Cambios)
Estos son los comandos que usarás en el día a día para registrar tus avances.

```bash
# Muestra el estado actual de tus archivos (modificados, nuevos, listos para guardar)
git status

# Agrega un archivo específico al área de preparación (Staging Area)
git add nombre-del-archivo.txt

# Agrega TODOS los archivos nuevos y modificados de golpe
git add .

# Guarda tus cambios de forma definitiva en el historial local con un mensaje explicativo
git commit -m "Explicación breve de los cambios realizados"
```

---

## 4. Conectar y Subir a GitHub
Comandos para enviar tus commits locales al servidor remoto de GitHub.

```bash
# Renombra la rama principal por defecto a 'main' (estándar actual de GitHub)
git branch -M main

# Vincula tu repositorio local con el repositorio remoto en GitHub (solo se hace una vez)
git remote add origin https://github.com

# Sube tus cambios locales a la rama 'main' de GitHub por primera vez
git push -u origin main

# Sube tus cambios en las siguientes ocasiones (ya configurado el comando anterior)
git push
```

---

## 5. Actualizar y Descargar Cambios
Usa esto cuando trabajes en equipo o desde computadoras diferentes para mantener tu código al día.

```bash
# Trae y fusiona los últimos cambios desde GitHub a tu repositorio local
git pull

# Muestra el historial completo de commits realizados en el proyecto
git log --oneline

## 6. Manejo de Ramas (Branches)
Las ramas te permiten experimentar con nuevas funciones sin alterar el código principal que ya funciona.

```bash
# Lista todas las ramas locales de tu proyecto
git branch

# Crea una nueva rama
git branch nueva-funcion

# Cambia de rama para empezar a trabajar en ella
git checkout nueva-funcion

# Crea una nueva rama y te cambia a ella automáticamente en un solo paso
git checkout -b otra-funcion

# Fusiona los cambios de otra rama dentro de la rama donde estás parado actualmente
git merge nueva-funcion