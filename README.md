




# Introducción a Git y GitHub

---

## 1. ¿Qué es Git?

**Git** es un sistema de control de versiones distribuido, gratuito y de código abierto. Está diseñado para gestionar con velocidad y eficiencia todo tipo de proyectos, desde los más pequeños hasta los de gran envergadura. Destaca por su facilidad de aprendizaje, su bajo consumo de recursos y sus operaciones ultrarrápidas (*lightning-fast*).

* **Origen e historia**: Fue creado en **2005** por **Linus Torvalds** (creador del sistema operativo Linux) con el propósito de rastrear los cambios en el código fuente durante el desarrollo de software. Actualmente, es el sistema de control de versiones más popular entre los desarrolladores.

---

## 2. ¿Por qué necesitamos Git?

El trabajo técnico va mucho más allá de simplemente escribir código. Git resulta indispensable porque facilita tareas críticas en distintos ámbitos:

* **En el desarrollo de software**: Permite hacer seguimiento de modificaciones, colaborar en equipo, probar nuevas funcionalidades de forma segura y revertir cambios que hayan resultado erróneos.
* **En ciencia y análisis de datos**: Facilita el control de cambios en conjuntos de datos (*datasets*), modelos de aprendizaje automático (*machine learning*) y *notebooks* de Jupyter, impulsando la experimentación y el trabajo colaborativo.

---

## 3. ¿Cómo funciona Git?

Git rastrea y registra las modificaciones de los archivos dentro de un directorio denominado **repositorio**. 

* **Sistema de instantáneas (*snapshots*)**: Cada vez que se registra un cambio, Git toma una instantánea del estado actual de los archivos y guarda una referencia a ella.
* **Optimización de espacio**: Si un archivo no ha sufrido modificaciones respecto a la versión anterior, Git no lo vuelve a almacenar; simplemente crea un enlace al archivo idéntico previo que ya tiene guardado.

---

## 4. Configuración básica de Git

Antes de empezar a trabajar con Git, es necesario configurar la identidad del usuario (nombre y correo electrónico), ya que Git utiliza estos datos para asociar cada registro de cambios (*commit*) con su autor.

Se configura ejecutando los siguientes comandos en la terminal:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@ejemplo.com"
```

---

## 5. Conceptos fundamentales de Git

Para operar con Git es imprescindible dominar cuatro conceptos clave:

* **Repositorio**: Contenedor donde se aloja un proyecto rastreado por Git. Incluye tanto los archivos del proyecto como todo su historial completo de cambios.
* **Staging Area (Área de preparación)**: Espacio intermedio donde se agrupan y preparan los archivos modificados antes de confirmarlos definitivamente.
* **Commit**: Instantánea o "versión guardada" de los archivos en un momento concreto.
* **Branch (Rama)**: Línea o versión paralela de un repositorio que permite trabajar en distintas funcionalidades o versiones de un proyecto de manera simultánea.

---

## 6. Comandos básicos de Git

### Inicialización, clonación y estado
* `git init`: Inicia un nuevo repositorio de Git en el directorio actual.
* `git clone <url>`: Descarga (clona) un repositorio existente desde una URL remota.
* `git status`: Muestra el estado actual del repositorio (archivos modificados, preparados o sin rastrear).
* `git log`: Muestra el historial de *commits* realizados.

### Registro de cambios (Flujo local)
* `git add <archivo>`: Añade un archivo específico al *Staging Area*. *(Nota: usando `git add .` se añaden todos los cambios)*.
* `git commit -m "<mensaje>"`: Crea un nuevo *commit* con las modificaciones del *Staging Area* acompañado de un mensaje descriptivo.

### Gestión de ramas (*Branches*)
* `git branch <nombre>`: Crea una nueva rama con el nombre indicado.
* `git checkout <nombre>`: Cambia el espacio de trabajo a la rama especificada.
* `git merge <nombre>`: Fusiona los cambios de la rama especificada dentro de la rama en la que te encuentras actualmente.

### Sincronización remota
* `git pull`: Descarga y actualiza en tu repositorio local los cambios provenientes del repositorio remoto.
* `git push`: Sube los *commits* locales al repositorio remoto.

---

## 7. ¿Qué es GitHub? y ¿Cómo funciona?

* **Definición**: **GitHub** es una plataforma de alojamiento en la nube para repositorios de Git. Ofrece tanto una interfaz web como integración con la línea de comandos, además de múltiples herramientas diseñadas para colaborar en proyectos públicos (código abierto) o privados.
* **Funcionamiento (Local vs. Remoto)**:
  * **Repositorio local**: Es el repositorio de Git alojado en tu propia computadora.
  * **Repositorio remoto**: Es la copia alojada en la nube de GitHub. Subir el proyecto a GitHub funciona como copia de seguridad ante fallos en el equipo local y permite que otros desarrolladores accedan, descarguen y colaboren en el código.

---

## 8. Flujo de trabajo práctico en GitHub

### A. Crear una cuenta en GitHub
1. Acceder a [GitHub](https://github.com).
2. Hacer clic en **"Sign up for GitHub"**.
3. Completar el formulario de registro.
4. Verificar la dirección de correo electrónico.

### B. Crear un nuevo repositorio en GitHub
1. Iniciar sesión en la plataforma.
2. Seleccionar la opción **"New repository"**.
3. Asignar un nombre al repositorio, añadir una descripción (opcional), definir su visibilidad (público o privado) y decidir si se inicializa con un archivo `README`.
4. Hacer clic en **"Create repository"**.

### C. Clonar un repositorio remoto a local
Para descargar una copia de un proyecto de GitHub en tu equipo local:

```bash
git clone <URL del repositorio>
```

### D. Subir cambios locales a GitHub
Para enviar las modificaciones realizadas en tu máquina hacia el repositorio remoto en GitHub, se siguen tres pasos (añadir, confirmar y subir):

```bash
git add .
git commit -m "mensaje"
git push
```

*(Nota: Para especificar la rama de destino, se utiliza `git push origin <branch>`. Si se trabaja en la rama principal, el comando es `git push origin main`)*.

---

## 9. Referencias y recursos adicionales

* [Documentación oficial de Git](https://git-scm.com)
* [Guía de GitHub para principiantes](https://github.com)
* [Tutorial interactivo de Git (Learn Git Branching)](https://js.org)







<hr>











# Manual de GitHub: Guía Completa de Teoría y Comandos

---

## 1. ¿Qué es Git, qué es GitHub y cuál es su diferencia?

* **Git**: Es un **sistema de control de versiones distribuido**. Es la herramienta local que permite a los desarrolladores rastrear los cambios realizados en su código fuente a lo largo del tiempo dentro de su computadora.
* **GitHub**: Es una **plataforma en línea** que utiliza Git como motor subyacente para alojar repositorios en la nube.
* **Diferencia clave**: Mientras que **Git** gestiona y rastrea el historial de versiones de forma local en tu máquina, **GitHub** actúa como un servicio en la nube que almacena esos repositorios de forma remota para facilitar la colaboración y la gestión de proyectos de software en equipo.

---

## 2. Primeros pasos: Configuración en VSC y creación de repositorio

### Configuración inicial en Visual Studio Code (VSC)
Antes de empezar a trabajar, es necesario vincular tu identidad de GitHub en la consola integrada de VSC ejecutando los comandos de configuración global (sustituyendo los datos por tu usuario y correo electrónico de GitHub):

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```

### Creación de un repositorio en GitHub
Para crear un nuevo espacio de alojamiento en la nube, sigue estos pasos desde la web de GitHub:
1. Inicia sesión en tu cuenta de GitHub.
2. Accede a la pestaña **Repositories** y haz clic en el botón **New**.
3. Asigna un nombre al repositorio.
4. Define la visibilidad del proyecto (**Público** o **Privado**).
5. **Paso fundamental**: Marca siempre la opción para añadir un archivo **`README.md`**.
6. Haz clic en **Create repository**.

---

## 3. Clonar un repositorio en Visual Studio Code (VSC)

Clonar consiste en descargar una copia exacta del repositorio remoto en tu equipo local para empezar a trabajar sobre él:

1. Entra en tu repositorio en GitHub, haz clic en el botón **Code** y copia la URL del enlace.
2. En Visual Studio Code, abre o añade un **espacio de trabajo nuevo** seleccionando una carpeta local que esté vacía.
3. Haz clic derecho sobre la carpeta en el explorador de VSC y selecciona **"Abrir en terminal integrado"**.
4. Ejecuta el comando de clonación en la consola:

```bash
git clone <link-del-repositorio>
```

---

## 4. Cómo añadir nueva información al repositorio

Una vez creados o modificados los archivos en local, es imprescindible **guardar todos los documentos** antes de sincronizarlos. El ciclo estándar de subida consta siempre de **3 pasos**:

1. **Add**: Selección de los archivos modificados que se desean preparar para subir.
2. **Commit**: Registro de los cambios con un comentario descriptivo de la versión.
3. **Push**: Envío definitivo de los cambios confirmados al repositorio remoto en GitHub.

### Flujo desde la Terminal
* **Preparar archivos (`add`)**:
  * Para añadir todos los cambios realizados: `git add .` *(no olvidar el punto final)* o `git add -A`.
  * Para añadir únicamente un archivo concreto: `git add nombre_del_archivo.extension`.
* **Verificar selección (`status`)**:
  * Para comprobar qué archivos están seleccionados y el estado actual: `git status`.
* **Deshacer selección (`reset`)**:
  * Para quitar un archivo concreto de la lista de seleccionados: `git reset HEAD nombre_del_archivo.extension`.
  * Para deseleccionar todos los archivos preparados: `git reset`.
* **Confirmar cambios (`commit`)**:
  * Para guardar la instantánea con un mensaje claro: `git commit -m "mensaje descriptivo de los cambios"`.
* **Subir al repositorio remoto (`push`)**:
  * Para enviar los *commits* a GitHub: `git push`.

### Flujo desde la Interfaz Gráfica de VSC
1. Accede a la pestaña de **Source Control** (Control de código fuente) en el panel lateral izquierdo de VSC.
2. Añade (marca con el símbolo `+`) los archivos modificados que aparecen listados.
3. Escribe el mensaje de confirmación y selecciona la opción **Commit & Push** con un clic.

---

## 5. Utilización y creación de ramas (*Branches*)

### ¿Qué es una rama?
Las ramas (*branches*) permiten que varias personas trabajen **en paralelo y de forma simultánea** en diferentes funcionalidades o partes de un mismo proyecto sin interferir con el código principal.

### Gestión de ramas por Terminal
* **Crear una rama en local**: `git branch nombre-de-tu-branch`
* **Listar ramas locales actuales**: `git branch --list`
* **Ver ramas creadas remotamente por otros usuarios**: `git branch -a`
* **Moverse (cambiar) a una rama existente**: `git checkout nombre-de-tu-branch`
* **Crear una rama y cambiar a ella al mismo tiempo**: `git checkout -b nombre-de-la-rama`
* **Eliminar una rama local**: `git branch -d nombre-de-tu-branch` *(Debes estar situado fuera de la rama que deseas borrar para evitar errores)*.
* **Publicar (subir) una rama local a GitHub**: `git push origin nombre-de-tu-branch` *(Debes estar situado dentro de la rama que vas a subir)*.

### Gestión de ramas desde la Interfaz de VSC
* Haz clic en el indicador de la rama actual situado en la **esquina inferior izquierda** de VSC.
* Se desplegará un panel superior que permite crear una rama nueva (desde la rama actual o desde otra específica) o cambiar entre ramas existentes.
* Desde el menú de **Source Control**, también es posible subir la rama recién creada al repositorio remoto haciendo clic en **Publish Branch**.

---

## 6. Juntar ramas (*Merge*) y Resolución de Conflictos

### Fusión de ramas (*Merge*)
Cuando terminas tu desarrollo en una rama secundaria, debes integrarlo en la rama padre (habitualmente `dev` o `main`):
1. Sitúate en la rama de destino (la rama padre que recibirá los cambios) mediante `git checkout main` (o `dev`).
2. Ejecuta la fusión desde la terminal o desde la interfaz de Source Control de VSC *(es recomendable realizarlo por terminal teniendo claro desde qué rama se ejecuta y qué cambios se van a integrar)*.

### Resolución de conflictos
* **¿Por qué ocurren?**: Suceden cuando el código modificado por un compañero entra en contradicción con el código que tú has modificado en las mismas líneas al intentar mezclar (*merge*) las ramas.
* **¿Cómo se resuelven?**:
  1. Al detectarse el error, la pestaña **Source Control** de VSC señalará los archivos que presentan conflictos.
  2. Al abrir el archivo afectado y pulsar en **"Resolve in Merge Editor"**, VSC mostrará una interfaz visual comparativa para revisar ambas versiones, decidir qué cambios conservar y completar la fusión.

---

## 7. Pull Request (PR): ¿Qué es y para qué sirve?

Un **Pull Request** es una herramienta fundamental en el flujo de trabajo colaborativo. Permite a los integrantes de un equipo **revisar, discutir y aprobar** los cambios realizados en una rama antes de integrarlos definitivamente en la rama principal del proyecto, garantizando la calidad del código y previniendo errores.

### Flujo de trabajo de un Pull Request en GitHub
1. Asegúrate de tener todo tu trabajo guardado y subido (`push`) a tu rama remota en GitHub.
2. Accede al repositorio en la web de GitHub y selecciona tu rama o haz clic en el aviso para crear un **Pull Request**.
3. Revisa la comparación entre la rama base (destino) y tu rama (origen), añade un título y descripción de los cambios, y confirma la creación del Pull Request.
4. Una vez revisado y aprobado, haz clic en **Merge pull request** para integrar los cambios en la rama principal.
5. Tras completar la fusión, puedes eliminar la rama secundaria desde la misma interfaz de GitHub (**Delete branch**) para mantener el repositorio limpio.

---

## 8. Resumen de Comandos Básicos de Git

| Acción | Comando en Terminal |
| :--- | :--- |
| **Clonar un repositorio remoto** | `git clone <link-del-repositorio>` |
| **Añadir un archivo específico al área de preparación** | `git add <archivo>` |
| **Añadir todos los archivos modificados** | `git add -A` o `git add .` |
| **Comprobar estado y archivos seleccionados** | `git status` |
| **Deshacer selección de un archivo / todos** | `git reset HEAD <archivo>` / `git reset` |
| **Guardar cambios con mensaje (Commit)** | `git commit -m "mensaje descriptivo"` |
| **Subir cambios al repositorio remoto** | `git push` |
| **Subir una rama nueva al repositorio remoto** | `git push origin <nombre-rama>` |
| **Descargar y actualizar cambios desde remoto** | `git pull` |
| **Listar ramas locales** | `git branch --list` |
| **Listar ramas remotas** | `git branch -a` |
| **Crear una rama nueva** | `git branch <nombre-rama>` |
| **Cambiar a una rama existente** | `git checkout <nombre-rama>` |
| **Crear una rama y cambiar a ella directamente** | `git checkout -b <nombre-rama>` |
| **Eliminar una rama local** | `git branch -d <nombre-rama>` |
| **Ver historial de commits (salir pulsando `q`)** | `git log` |
| **Ver historial resumido (solo código y título)** | `git log --oneline` |
| **Deshacer un commit específico** | `git revert <codigo-del-commit>` |









<hr>
