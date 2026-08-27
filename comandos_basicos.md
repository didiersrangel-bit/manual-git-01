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

## Resumen del Flujo Diario 
Si ya tienes todo configurado, tu rutina diaria de comandos se reduce a esto:
1. `git pull` *(para empezar el día con el código actualizado)*
2. Haces tus cambios en el código...
3. `git add .` *(preparas los archivos)*
4. `git commit -m "mensaje"` *(guardas localmente)*
5. `git push` *(lo subes a GitHub)*

## Ventajas y Desventajas de los Comandos Básicos de Git y GitHub

El control de versiones mediante la terminal de comandos es el estándar de la industria del software. A continuación, se presenta un análisis de los pros y contras de dominar estos comandos fundamentales.

### Ventajas
* **Velocidad y Eficiencia:** La ejecución de comandos por terminal consume menos recursos del sistema y es drásticamente más rápida que hacer clics en una interfaz gráfica (GUI).
* **Control Total del Historial:** Permite rastrear, modificar, fusionar o revertir cualquier cambio línea por línea con precisión absoluta mediante hashes de confirmación específicos.
* **Automatización de Tareas:** Los comandos se pueden integrar fácilmente en scripts externos, flujos de trabajo automáticos (como GitHub Actions) y procesos de despliegue continuo (CI/CD).
* **Compatibilidad Universal:** Funciona exactamente igual en cualquier sistema operativo (Linux, macOS, Windows) y en entornos remotos de servidores donde no existe una interfaz visual.

### Desventajas
* **Curva de Aprendizaje Elevada:** Memorizar la sintaxis exacta, los modificadores y los parámetros iniciales resulta complejo y poco intuitivo para usuarios principiantes.
* **Riesgo de Errores Críticos:** Un comando mal ejecutado (como un `git push --force` o un `git reset --hard`) puede borrar permanentemente semanas de trabajo del repositorio local o remoto.
* **Complejidad en Conflictos:** Resolver conflictos de fusión (*merge conflicts*) complejos a través de líneas de texto en la terminal puede ser confuso sin el apoyo visual de un editor de código.
* **Falta de Feedback Visual:** No ofrece mapas visuales automáticos ni diagramas de la estructura de las ramas a menos que se utilicen comandos avanzados de formato muy largos.