# Tema 1: El baúl temporal (`git stash`)

Imagina esta situación: llevas dos horas trabajando en una nueva función en tu rama. El código está a medias, no funciona y está todo desordenado. De repente, te llama un compañero: *"¡Hay un error crítico en `main`! ¿Puedes cambiar de rama y arreglarlo rápido?"*.

Intentas hacer un `git switch main`, pero Git te lanza un error y te dice que no puedes cambiar de rama porque tienes archivos modificados sin guardar. Tampoco quieres hacer un `git commit` porque tu código actual es un desastre y está incompleto. ¿Qué haces?

¡Es la hora de usar el baúl temporal de Git!

## 📦 1. ¿Qué es `git stash`?

El comando `stash` (esconder o almacenar) actúa como un cajón de sastre o un baúl temporal. Coge todos los archivos que has modificado y que aún no has "commiteado", y los guarda de forma segura en un rincón invisible, dejando tu espacio de trabajo totalmente limpio.

Para guardar tu trabajo a medias en este baúl, solo tienes que ejecutar:

```bash
git stash
```

¡Puf! Magia. Si miras tus archivos, verás que han vuelto al estado de tu último commit. Tu código a medias ha desaparecido temporalmente y tu espacio de trabajo está limpio. Ahora ya puedes hacer `git switch main` y arreglar esa urgencia sin problemas.

## 🕵️‍♂️ 2. Ver qué hay en el baúl

Si te vas a tomar un café y al volver no recuerdas si tenías algo guardado, puedes asomarte a ver qué hay dentro del baúl con este comando:

```bash
git stash list
```

*Verás una lista con los elementos guardados. Si solo lo has usado una vez, verás algo como `stash@{0}: WIP on mi-rama...` (WIP significa Work In Progress, trabajo en progreso).*

## 🎁 3. Recuperar tu trabajo (`git stash pop`)

Ya has arreglado la urgencia en `main` y has vuelto a tu rama original. Es hora de sacar tu código a medias del baúl y seguir trabajando por donde lo dejaste.

Para "sacar" los cambios del baúl y aplicarlos de nuevo en tus archivos, usamos el comando `pop` (que literalmente significa "hacer saltar" o "sacar"):

```bash
git stash pop
```

Este comando hace dos cosas a la vez:
1. Devuelve las modificaciones a tus archivos tal y como estaban.
2. Borra esa entrada del baúl temporal para mantenerlo limpio.

> **💡 Consejo profesional:** Puedes usar `git stash` tantas veces como quieras; los cambios se irán apilando en el baúl unos encima de otros. Al hacer `git stash pop`, Git siempre sacará el **último** que guardaste. 

---
**Siguiente paso:** El `stash` nos ha salvado de un apuro por interrupción, pero ¿qué pasa cuando el error es que hemos borrado todo el contenido de un archivo sin querer y queremos que vuelva a estar como en el último commit? En el próximo tema aprenderemos a usar la goma de borrar de Git.