# Tema 3: Primeros pasos en la Terminal (Consola)

Muchos principiantes le tienen pánico a la pantalla negra (la terminal o consola). Sin embargo, Git nació en la terminal, y aprender a usarla te dará un control absoluto sobre tus proyectos.

No necesitas ser un hacker de las películas. Para trabajar con Git, solo necesitas conocer **cuatro comandos básicos de supervivencia**. 

Abre tu terminal (Git Bash en Windows) y pruébalos:

## 1. `pwd` (¿Dónde estoy?)
La terminal es como un explorador de archivos, pero sin interfaz gráfica. Si no sabes en qué carpeta estás actualmente, escribe `pwd` (*Print Working Directory*) y pulsa Enter.
* **Por qué es útil para Git:** Antes de decirle a Git que guarde un proyecto, ¡necesitas asegurarte de que estás dentro de la carpeta correcta!

## 2. `ls` (¿Qué hay aquí?)
Escribe `ls` (*List*) para ver los archivos y carpetas que hay donde estás ahora mismo. 
* **El truco de Git (`ls -a`):** Si escribes `ls -a` (la `-a` significa *all*, todo), verás también los archivos ocultos. Esto es crucial en Git, porque cuando inicialicemos un proyecto, Git creará una carpeta oculta llamada `.git` que almacena todo tu historial. Con `ls -a` podrás confirmar que está ahí.

## 3. `mkdir` (Crear una carpeta)
Escribe `mkdir nombre-de-tu-proyecto` (*Make Directory*) para crear una nueva carpeta.
* **Por qué es útil para Git:** Cada nuevo repositorio de GitHub empieza su vida como una simple carpeta vacía en tu ordenador creada con este comando.

## 4. `cd` (Entrar a una carpeta)
Escribe `cd nombre-de-la-carpeta` (*Change Directory*) para entrar en la carpeta que acabas de crear. (Si quieres volver hacia atrás, escribe `cd ..`).
* **Por qué es útil para Git:** Si creas una carpeta para tu código pero olvidas hacer `cd` para entrar en ella, terminarás inicializando Git en el lugar equivocado (¡un error muy común!).

---
> **💡 Consejo pro:** En la terminal, si empiezas a escribir el nombre de una carpeta y pulsas la tecla `Tabulador`, la terminal autocompletará el nombre por ti. ¡Ahorra mucho tiempo!