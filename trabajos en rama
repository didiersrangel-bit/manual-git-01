## trabajos_en_rama
ChatGPT Plus
Todo sobre el trabajo con ramas en GitHub
Las ramas (branches) son una de las herramientas más importantes de Git y GitHub. Permiten que varias personas trabajen sobre un mismo proyecto sin modificar directamente el código principal. Son fundamentales para desarrollar funcionalidades nuevas, corregir errores, experimentar, revisar cambios y organizar equipos de trabajo.

En este documento encontrarás una guía completa sobre el trabajo con ramas en Git y GitHub, desde los conceptos básicos hasta flujos de trabajo profesionales.

1. ¿Qué es Git?
Git es un sistema de control de versiones distribuido.

Su función principal es registrar los cambios realizados en los archivos de un proyecto.

Por ejemplo, imagina que tienes un proyecto:

mi-proyecto/
├── index.html
├── styles.css
└── script.js

Al trabajar normalmente, puedes modificar estos archivos y Git puede guardar diferentes versiones de ellos.

Por ejemplo:

Versión 1
   ↓
Versión 2
   ↓
Versión 3
   ↓
Versión 4

Esto permite saber:

Qué cambió.
Quién hizo el cambio.
Cuándo se hizo.
Qué archivos fueron modificados.
Volver a una versión anterior.
Comparar versiones.
Trabajar simultáneamente con otras personas.
2. ¿Qué es GitHub?
GitHub es una plataforma que permite almacenar repositorios Git en Internet y colaborar sobre ellos.

Git y GitHub no son exactamente lo mismo.

Git	GitHub
Sistema de control de versiones	Plataforma de colaboración
Funciona localmente	Funciona principalmente en la nube
Registra cambios	Aloja repositorios
Permite crear ramas	Permite administrar ramas remotamente
Permite commits	Permite Pull Requests
Permite merges	Permite revisiones de código

Por ejemplo:

Tu computadora
     │
     │ Git
     ▼
Repositorio local
     │
     │ git push
     ▼
GitHub
     │
     ▼
Repositorio remoto

3. ¿Qué es una rama?
Una rama es una línea independiente de desarrollo dentro de un repositorio Git.

En inglés se llama:

branch

La idea principal es que puedes crear una rama para trabajar en algo específico sin modificar inmediatamente la rama principal.

Por ejemplo:

main
 │
 ├── agregar-login
 │
 ├── corregir-menu
 │
 └── nueva-pagina

Cada rama puede tener sus propios commits.

4. ¿Por qué usar ramas?
Supongamos que tienes un proyecto en producción.

La rama principal contiene:

main

Y necesitas desarrollar un sistema de autenticación.

Podrías modificar directamente main, pero esto puede ser peligroso.

Una mejor estrategia es crear:

feature/login

Entonces:

main
 │
 └── feature/login

Trabajas en:

feature/login

Cuando terminas, puedes revisar los cambios y posteriormente integrarlos en:

main

5. Ventajas de trabajar con ramas
Las ramas permiten:

Desarrollar funcionalidades independientemente.
Corregir errores sin afectar main.
Experimentar con nuevas ideas.
Trabajar varias personas simultáneamente.
Hacer revisiones de código.
Crear Pull Requests.
Mantener estable el código principal.
Organizar el trabajo del equipo.
Separar funcionalidades.
Facilitar el trabajo con metodologías como GitHub Flow o Git Flow.
6. La rama main
En muchos proyectos, la rama principal se llama:

main

Históricamente muchos repositorios utilizaban:

master

pero actualmente main es muy común.

La rama principal normalmente representa una versión estable del proyecto.

Por ejemplo:

main
 │
 ├── commit A
 ├── commit B
 ├── commit C
 └── commit D

Es recomendable evitar trabajar directamente sobre main en proyectos colaborativos.

Una práctica habitual es:

main
  ↓
crear rama
  ↓
trabajar
  ↓
commit
  ↓
push
  ↓
Pull Request
  ↓
revisión
  ↓
merge
  ↓
main

7. Crear un repositorio
Puedes crear un repositorio en GitHub.

Por ejemplo:

mi-proyecto

Después puedes clonarlo en tu computadora.

git clone https://github.com/usuario/mi-proyecto.git

Después:

cd mi-proyecto

Ahora tienes una copia local del repositorio.

8. Inicializar Git en un proyecto existente
Si ya tienes un proyecto en tu computadora y quieres comenzar a utilizar Git:

git init

Después puedes comprobar el estado:

git status

Puedes agregar los archivos:

git add .

Y crear el primer commit:

git commit -m "Primer commit"

Después puedes conectar el repositorio local con GitHub:

git remote add origin https://github.com/usuario/mi-proyecto.git

Y subirlo:

git push -u origin main

9. ¿Qué es un commit?
Un commit representa un conjunto de cambios guardados en el historial de Git.

Por ejemplo:

git add .
git commit -m "Agregar formulario de login"

El commit puede verse conceptualmente así:

A
│
B
│
C
│
D

Cada letra representa un estado del proyecto.

Un commit normalmente tiene:

Un identificador.
Un autor.
Una fecha.
Un mensaje.
Los cambios realizados.
10. Ver el historial
Puedes consultar los commits con:

git log

Una versión más resumida:

git log --oneline

Por ejemplo:

a31f8c2 Agregar formulario
91b2d44 Corregir estilos
7f3a1e9 Crear página principal

11. Crear una rama
Para crear una rama puedes utilizar:

git branch nombre-rama

Por ejemplo:

git branch feature/login

Esto crea la rama, pero no cambia automáticamente a ella.

12. Cambiar de rama
Puedes utilizar:

git switch feature/login

También existe el comando tradicional:

git checkout feature/login

Actualmente se suele preferir git switch para cambiar de rama porque hace más explícita la intención.

13. Crear y cambiar a una rama en un solo comando
Una de las formas más utilizadas es:

git switch -c feature/login

Esto hace dos cosas:

Crea la rama.
Cambia a ella.
Por ejemplo:

git switch -c feature/registro

El resultado conceptual sería:

main
 │
 └── feature/registro  ← estás aquí

14. Ver las ramas
Para ver las ramas locales:

git branch

Por ejemplo:

* main
  feature/login
  feature/registro
  bugfix/menu

El símbolo:

*

indica la rama actual.

15. Ver ramas remotas
Puedes utilizar:

git branch -r

Por ejemplo:

origin/main
origin/feature/login
origin/bugfix/menu

16. Ver todas las ramas
Para ver ramas locales y remotas:

git branch -a

Podrías obtener:

* main
  feature/login
  bugfix/menu
  remotes/origin/main
  remotes/origin/feature/login
  remotes/origin/bugfix/menu

17. Rama local vs rama remota
Este concepto es muy importante.

Una rama local existe en tu computadora:

feature/login

Una rama remota representa una referencia a una rama que existe en el repositorio remoto:

origin/feature/login

Por ejemplo:

Computadora                  GitHub
───────────                  ──────

feature/login  ───────────►  origin/feature/login

Cuando haces:

git push

envías tus commits al repositorio remoto.

18. ¿Qué significa origin?
Cuando clonas un repositorio:

git clone https://github.com/usuario/proyecto.git

Git normalmente configura el repositorio remoto con el nombre:

origin

Puedes verlo mediante:

git remote -v

Por ejemplo:

origin  https://github.com/usuario/proyecto.git (fetch)
origin  https://github.com/usuario/proyecto.git (push)

origin es simplemente un nombre convencional para identificar el repositorio remoto principal.

19. Subir una rama a GitHub
Supongamos que tienes:

feature/login

Puedes subirla con:

git push -u origin feature/login

Después de esto, GitHub tendrá la rama.

Local                         GitHub

feature/login  ────────────►  feature/login

La opción:

-u

establece una relación de seguimiento entre la rama local y la remota.

Después normalmente podrás utilizar simplemente:

git push

y:

git pull

20. Descargar cambios de GitHub
Uno de los comandos fundamentales es:

git pull

Este comando obtiene cambios del repositorio remoto y los integra en tu rama actual.

Por ejemplo:

GitHub
  │
  │ git pull
  ▼
Tu computadora

21. git fetch vs git pull
Estos comandos se parecen, pero no son iguales.

git fetch
Obtiene información y cambios del repositorio remoto, pero no integra automáticamente esos cambios en tu rama actual.

git fetch

Conceptualmente:

GitHub
  │
  │ fetch
  ▼
Referencias remotas

git pull
Normalmente hace:

fetch + integración

Por ejemplo:

git pull

Puede realizar un merge o, dependiendo de la configuración y del historial, un rebase.

22. ¿Qué es hacer push?
push significa enviar tus commits locales al repositorio remoto.

Por ejemplo:

git push origin feature/login

Conceptualmente:

Tu computadora
     │
     │ push
     ▼
GitHub

23. ¿Qué es hacer pull?
pull significa traer cambios del repositorio remoto e integrarlos.

git pull

Por ejemplo:

GitHub
   │
   │ pull
   ▼
Repositorio local

24. Flujo básico de trabajo con ramas
Un flujo sencillo sería:

git switch main
git pull
git switch -c feature/login

Después haces cambios.

Compruebas:

git status

Agregas los archivos:

git add .

Creas el commit:

git commit -m "Agregar login"

Subes la rama:

git push -u origin feature/login

Después creas un Pull Request en GitHub.

25. El comando git status
Es uno de los comandos que más utilizarás.

git status

Te informa, entre otras cosas:

En qué rama estás.
Qué archivos fueron modificados.
Qué archivos están preparados para commit.
Qué archivos no están siendo rastreados.
Si tu rama está adelantada o atrasada respecto al remoto.
Ejemplo:

On branch feature/login

Changes not staged for commit:
  modified: login.html
  modified: styles.css

26. El área de staging
Git tiene una zona intermedia llamada staging area.

El flujo puede representarse así:

Archivos
   │
   │ git add
   ▼
Staging
   │
   │ git commit
   ▼
Repositorio

Por ejemplo:

git add login.html

Después:

git commit -m "Agregar formulario de login"

27. git add .
Puedes agregar todos los cambios:

git add .

Pero hay que utilizarlo con cuidado.

Si tienes archivos que no querías incluir, podrían terminar en el staging.

Puedes agregar archivos específicos:

git add login.html
git add styles.css

Esto proporciona un mayor control.

28. Crear buenos commits
Los mensajes de commit deberían explicar qué cambio se realizó.

Buenos ejemplos:

Agregar formulario de registro
Corregir validación del correo
Actualizar estilos del menú
Eliminar función obsoleta
Agregar autenticación con JWT

Evita mensajes poco descriptivos como:

cambios
arreglos
cosas
update
final
final2
ahora si

29. Convención de commits
Algunos equipos utilizan Conventional Commits.

Ejemplos:

feat: agregar login
fix: corregir validación del formulario
docs: actualizar README
refactor: reorganizar servicio de usuarios
test: agregar pruebas de autenticación
chore: actualizar dependencias

Los tipos habituales incluyen:

feat
fix
docs
refactor
test
chore
perf

Por ejemplo:

git commit -m "feat: agregar autenticación"

30. Nombres de ramas
Es importante utilizar nombres claros.

Ejemplos:

feature/login
feature/register
feature/payment-system

bugfix/login-error
bugfix/navbar-mobile

hotfix/security-vulnerability

docs/readme
refactor/user-service

Algunas convenciones frecuentes son:

feature/
bugfix/
hotfix/
docs/
refactor/
test/
chore/

31. Ejemplo de nombres incorrectos
Evita nombres como:

rama1
prueba
cosas
nueva
juan
trabajo
cambios
rama-final
rama-final-2

El nombre debería explicar la finalidad de la rama.

Mejor:

feature/user-authentication

que:

rama2

32. Una rama debe tener un objetivo
Una buena rama normalmente debería representar un trabajo específico.

Por ejemplo:

feature/login

No conviene utilizar una sola rama para:

login
+ registro
+ pagos
+ cambio de colores
+ documentación
+ nueva base de datos

Es mejor separar:

feature/login
feature/register
feature/payments
feature/new-theme
docs/update-readme

Esto facilita las revisiones y los merges.

33. Pull Request
Un Pull Request, normalmente abreviado como:

PR

es una solicitud para integrar los cambios de una rama en otra.

Por ejemplo:

feature/login
       │
       │ Pull Request
       ▼
      main

Un Pull Request permite que otras personas revisen el código antes de incorporarlo a la rama destino.

34. ¿Qué contiene un Pull Request?
Un Pull Request puede incluir:

Título.
Descripción.
Commits.
Archivos modificados.
Diferencias de código.
Comentarios.
Revisiones.
Aprobaciones.
Resultados de pruebas automáticas.
Checks de CI/CD.
35. Crear un Pull Request
Después de hacer:

git push -u origin feature/login

GitHub detectará que existe una nueva rama.

Puedes crear un Pull Request desde:

feature/login

hacia:

main

El flujo sería:

feature/login
      │
      │ push
      ▼
   GitHub
      │
      │ Pull Request
      ▼
     main

36. Source y target en un Pull Request
En un Pull Request existen normalmente:

source branch

y:

target branch

Por ejemplo:

source:
feature/login

target:
main

Significa:

Quiero integrar los cambios de feature/login en main.

37. Revisiones de código
Una de las grandes ventajas de los Pull Requests es el code review.

Un compañero puede revisar:

login.js

y comentar:

¿Podemos extraer esta lógica a una función?

O:

Aquí deberíamos validar que el correo sea obligatorio.

El autor puede realizar nuevos cambios.

Por ejemplo:

Commit 1
Agregar login

Commit 2
Corregir validación

Commit 3
Mejorar manejo de errores

Todos forman parte del Pull Request.

38. Aprobar un Pull Request
Un revisor puede:

Aprobar.
Solicitar cambios.
Comentar.
Revisar archivos específicos.
Por ejemplo:

Reviewer
   │
   ├── Comment
   ├── Approve
   └── Request changes

39. Merge
Cuando un Pull Request está listo, sus cambios pueden integrarse mediante un merge.

Por ejemplo:

main
 │
 ├── A
 ├── B
 │
 └───────────────┐
                 │
feature/login    │
 │               │
 ├── C           │
 ├── D           │
 └── E ──────────┘
                 ↓
                merge
                 ↓
                main

40. Tipos de merge en GitHub
GitHub puede ofrecer diferentes estrategias de integración.

Las más conocidas son:

Create a merge commit
Squash and merge
Rebase and merge

Cada una produce un historial diferente.

41. Merge commit
Un merge tradicional puede crear un commit de merge.

Por ejemplo:

A---B---C---------F
     \           /
      D---E------

Donde:

F

es el commit de merge.

Ventaja:

Conserva explícitamente la historia de la ramificación.
Desventaja:

Puede producir un historial más complejo.
42. Squash and merge
Con Squash and merge, varios commits de una rama se combinan en uno.

Por ejemplo:

feature/login

A
│
B
│
C
│
D

Puede convertirse en:

main

A
│
B
│
X

Donde X representa todos los cambios de la rama.

Es muy útil cuando una rama contiene commits como:

Agregar login
corrección
fix
fix final
cambio
arreglo

y se quiere mantener un historial más limpio.

43. Rebase and merge
Con rebase and merge, GitHub puede integrar la rama manteniendo una historia lineal cuando las condiciones lo permiten.

Conceptualmente:

Antes:

A---B---C
     \
      D---E

Después de rebase:

A---B---C---D'---E'

No siempre conviene hacer rebase indiscriminadamente, especialmente sobre ramas compartidas.

44. Merge local
También puedes hacer un merge desde tu computadora.

Por ejemplo:

git switch main
git merge feature/login

Esto intenta integrar:

feature/login

en:

main

45. El error de trabajar directamente en main
Imagina:

main
 │
 ├── commit estable
 │
 └── tú empiezas a modificar cosas

Si el código queda roto:

main
 │
 ├── estable
 │
 └── código roto

Ahora otras personas pueden verse afectadas.

Por eso es habitual trabajar así:

main
 │
 └── feature/nueva-funcionalidad

46. Mantener actualizada una rama
Supongamos que tienes:

feature/login

y mientras trabajabas otra persona modificó main.

Ahora:

GitHub main
A---B---C---D

Tu rama
A---B---C---E---F

Tu rama está basada en un estado anterior de main.

Antes de integrar tus cambios, puede ser necesario actualizarla.

47. Actualizar usando merge
Puedes hacer:

git switch main
git pull
git switch feature/login
git merge main

Esto incorpora los cambios de main a tu rama.

Resultado conceptual:

A---B---C---D
     \
      E---F---G

Donde G podría ser el merge.

48. Actualizar usando rebase
Otra opción:

git switch main
git pull
git switch feature/login
git rebase main

Conceptualmente:

Antes:

A---B---C---D   main
     \
      E---F     feature/login

Después:

A---B---C---D---E'---F'

La rama parece haber sido construida a partir de la versión más reciente de main.

49. ¿Merge o rebase?
Una regla práctica:

Merge
git merge main

Es sencillo y conserva explícitamente la historia de las ramas.

Rebase
git rebase main

Produce una historia más lineal, pero reescribe commits.

Una recomendación importante:

Evita hacer rebase de commits que otras personas ya están utilizando en una rama compartida, salvo que el equipo tenga una política clara para ello.

50. ¿Qué significa reescribir la historia?
Cuando haces:

git rebase

Git puede crear nuevos commits equivalentes.

Por eso:

E
F

puede convertirse conceptualmente en:

E'
F'

Aunque los cambios sean similares, los identificadores de commit pueden ser diferentes.

51. Conflictos
Uno de los temas más importantes al trabajar con ramas son los merge conflicts.

Un conflicto ocurre cuando Git no puede determinar automáticamente cómo combinar dos cambios incompatibles.

Por ejemplo, en main:

const color = "blue";

Y en tu rama:

const color = "red";

Si ambas ramas modifican exactamente la misma parte de una forma incompatible, Git puede detenerse.