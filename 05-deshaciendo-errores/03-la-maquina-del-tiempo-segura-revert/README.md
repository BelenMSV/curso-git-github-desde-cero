# Tema 3: La máquina del tiempo segura (`git revert`)

Imagina el peor escenario posible: el gato saltó al teclado, rompiste el código, le diste a guardar, hiciste un `git add`, luego un `git commit` y, para rematar, hiciste un `git push` y lo subiste a GitHub. 

El error ya es oficial. Ya está en el historial y tus compañeros de equipo pueden verlo. ¿Podemos borrar ese commit? **Poder se puede, pero no se debe.** Borrar historia que ya está en Internet es la receta perfecta para volver locos a tus compañeros y desincronizar el proyecto.

La solución elegante y profesional es usar la "máquina del tiempo segura": crear un **anti-commit**.

## ⏪ 1. ¿Qué es un anti-commit (`git revert`)?

El comando `git revert` no borra el pasado. Lo que hace es analizar el commit donde te equivocaste y crear un **nuevo commit** que hace exactamente lo contrario. 

* Si en el commit original añadiste una línea, el *revert* la borra.
* Si en el original borraste un archivo, el *revert* lo vuelve a crear.

De esta forma, el error se deshace en el código, pero queda un registro histórico transparente de que hubo un fallo y se arregló. ¡A los equipos de desarrollo les encanta esta transparencia!

## 🛠️ 2. Cómo revertir un error paso a paso

**Paso 1: Busca el DNI del commit culpable**
Abre tu historial y busca el código *hash* (los números y letras alfanuméricos) del commit que quieres deshacer:
```bash
git log --oneline
```
Imagina que descubres que el commit problemático es el `a1b2c3d`.

**Paso 2: Ejecuta la reversión**
Dile a Git que cree el anti-commit apuntando a ese código específico:
```bash
git revert a1b2c3d
```

**Paso 3: Confirma el mensaje**
Como Git está creando un *nuevo* commit para deshacer los cambios, abrirá tu editor de texto predeterminado pidiéndote un mensaje. Por defecto, Git te sugiere algo perfecto como `Revert "mensaje del commit malo"`. 

Simplemente guarda y cierra ese archivo (si se abre en la terminal con Vim, recuerda el truco de escape: pulsa `Esc`, escribe `:wq` y pulsa `Enter`).

¡Y listo! Tu código ha vuelto a funcionar. Como esto acaba de crear un nuevo commit en tu ordenador local, no olvides hacer un `git push` para subir la cura a GitHub y salvar el día.

---
**Siguiente paso:** Ya dominas la forma segura de viajar en el tiempo en entornos colaborativos. Pero, ¿y si estás trabajando tú solo, aún no has subido nada a Internet y *realmente* quieres borrar los últimos commits del historial como si nunca hubieran existido? En el próximo y último tema del módulo, entraremos en territorio peligroso con `git reset`.