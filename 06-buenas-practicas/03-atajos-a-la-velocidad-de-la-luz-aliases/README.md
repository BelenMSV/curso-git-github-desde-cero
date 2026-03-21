# Tema 3: Atajos a la velocidad de la luz (Git Aliases)

Si trabajas con Git todos los días, escribirás `git status`, `git commit` y `git checkout` cientos de veces. Parece una tontería, pero esos segundos tecleando suman horas al final del año. 

Los programadores somos eficientes por naturaleza (algunos dirían "perezosos"), así que Git incluye una herramienta maravillosa para ahorrarnos trabajo: los **Aliases** (Alias o apodos). 

Un alias te permite inventar un comando corto para sustituir a uno largo. En lugar de teclear `git status`, podrás escribir simplemente `git st`. ¡Magia!

## ⚡ 1. ¿Cómo se crea un alias?

Para decirle a Git que quieres crear un atajo, usamos el comando de configuración global (`git config --global`), seguido de la palabra `alias.` y el apodo que quieras inventar. 

La estructura es esta:
```bash
git config --global alias.apodo "comando_original"
```

## 🚀 2. Los atajos imprescindibles

Aquí tienes la lista de los alias más utilizados en la industria. Abre tu terminal y ejecuta estos comandos uno a uno para configurarlos en tu ordenador para siempre:

* **Para ver el estado rápidamente (`st` en lugar de `status`):**
  `git config --global alias.st "status"`
* **Para cambiar de rama volando (`co` en lugar de `checkout`):**
  `git config --global alias.co "checkout"`
* **Para ver las ramas (`br` en lugar de `branch`):**
  `git config --global alias.br "branch"`
* **Para hacer commits sin escribir tanto (`cm` en lugar de `commit -m`):**
  `git config --global alias.cm "commit -m"`

¡Pruébalo! Ahora, si quieres hacer un commit, solo tienes que escribir:
```bash
git cm "feat: añadir mi primer alias"
```

## 🌳 3. El atajo definitivo: Un historial bonito

¿Recuerdas que el comando `git log` por defecto es bastante feo y difícil de leer? Existe un comando muy largo en Git para que el historial se dibuje con colores y líneas conectando las ramas.

Como nadie quiere memorizar un comando de 50 letras, vamos a crear el alias definitivo. Cópialo y pégalo en tu terminal:

```bash
git config --global alias.arbol "log --oneline --graph --decorate --all"
```

A partir de hoy, cada vez que escribas `git arbol`, verás tu historial como un diagrama visual precioso y lleno de colores.

## 🗑️ 4. ¿Cómo borro un alias si me equivoco?

Si escribiste mal un alias o simplemente quieres eliminarlo, puedes decirle a Git que lo olvide con este comando (sustituyendo "apodo" por el que quieras borrar):

```bash
git config --global --unset alias.apodo
```

---
**Siguiente paso:** Ya escribes código limpio, proteges tus contraseñas y vuelas por la terminal. Solo te falta una cosa para estar listo para tu primer empleo: entender cómo se organiza todo esto en equipo. En el último tema del curso hablaremos del "GitHub Flow", la estrategia que usan las empresas reales.