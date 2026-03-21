# Tema 1: Creando universos paralelos (`git branch` y `git switch`)

Imagina que tu proyecto funciona a la perfección, pero tienes una idea para una nueva función. Quieres probarla, pero te da miedo modificar el código y estropear lo que ya está hecho. 

¿La solución? Crear un "universo paralelo". En Git, a esto lo llamamos **Ramas (Branches)**.



## 🌳 1. ¿Qué es una rama?

Por defecto, Git te crea una línea de tiempo principal llamada `main`. Piensa en `main` como la versión "oficial" y estable de tu proyecto. **La regla de oro es: en `main` nunca debe haber código roto.**

Cuando creas una rama nueva, Git hace una copia exacta de tu proyecto en ese momento. A partir de ahí, puedes trabajar en tu rama de forma totalmente aislada. Si tu experimento sale mal, lo borras y aquí no ha pasado nada. `main` seguirá intacto.

## 👀 2. Ver y crear ramas (`git branch`)

Para saber en qué "universo" estás ahora mismo, abre tu terminal y escribe:

```bash
git branch
```

*Verás una lista con tus ramas y un asterisco `*` (o un color distinto) señalando en la que te encuentras actualmente (seguramente solo verás `* main`).*

Para crear un nuevo universo paralelo (una nueva rama) para hacer un experimento, usamos el mismo comando seguido del nombre que le queramos dar:

```bash
git branch experimento-boton
```

> **💡 Consejo profesional:** Usa nombres descriptivos, en minúsculas y separados por guiones. Por ejemplo: `feat-login`, `correccion-menu`, o `prueba-colores`.

## 🚀 3. Viajar a otro universo (`git switch`)

El comando anterior ha creado la rama, pero **aún sigues en `main`**. Para "viajar" a tu nueva rama y empezar a trabajar en ella, usamos el comando `switch` (cambiar):

```bash
git switch experimento-boton
```
¡Felicidades! Ahora estás en tu universo paralelo. Cualquier cambio que hagas, los `git add` y `git commit` que ejecutes, solo se guardarán en esta rama.

### ⚡ El truco ninja (Crear y viajar a la vez)

En tu día a día, casi siempre querrás crear una rama y viajar a ella inmediatamente. Puedes hacerlo todo en un solo paso añadiendo el parámetro `-c` (create):

```bash
git switch -c mi-nueva-idea
```

> 👴 **Un poco de historia (`git checkout`)**
> Si buscas tutoriales en internet, verás que mucha gente usa el comando `git checkout mi-rama` o `git checkout -b mi-rama` para viajar y crear ramas. Es el comando antiguo. Git introdujo `switch` hace poco porque es mucho más intuitivo (literalmente significa "cambiar"). Ambos funcionan igual, pero `switch` es la forma moderna.

---
**Siguiente paso:** Ya sabemos crear ramas y viajar entre ellas. Pero, ¿qué pasa cuando nuestro experimento es un éxito y queremos juntarlo con nuestra versión oficial? Eso lo veremos en el próximo tema con el comando `merge`.