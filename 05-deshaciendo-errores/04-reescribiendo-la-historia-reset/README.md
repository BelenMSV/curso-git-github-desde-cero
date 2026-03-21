# Tema 4: Reescribiendo la historia (`git reset`)

A veces, el `git revert` no es lo que necesitas. Imagina que estás trabajando solo en tu ordenador, has hecho tres commits seguidos que son un desastre absoluto, y **aún no has subido nada a GitHub**. 

No quieres llenar tu historial de "anti-commits" porque quedaría muy sucio. Lo que realmente quieres es viajar en el tiempo, borrar esos tres commits como si nunca hubieran existido y hacer como que esa tarde de trabajo nunca ocurrió. 

Para eso usamos la máquina del tiempo definitiva: `git reset`.

## 🚨 Regla de oro: El peligro del Reset

Antes de usar este comando, grábate esto a fuego: **NUNCA uses `git reset` para borrar commits que ya has subido a GitHub (con `git push`) si trabajas con más gente**. 

Si borras la historia en tu ordenador y fuerzas la subida a Internet, vas a desincronizar los repositorios de todos tus compañeros y causarás un caos absoluto. `git reset` es una herramienta estrictamente para **código local** (que solo existe en tu ordenador).

## 🎛️ 1. Los tres sabores del Reset

Para usar `git reset`, primero miras tu historial (`git log --oneline`) y buscas el código (hash) del **último commit bueno** al que quieres regresar. Supongamos que es el `b2c3d4e`. 

Git te permite viajar a ese punto del pasado de tres formas diferentes, dependiendo de lo que quieras hacer con los archivos en los que estabas trabajando:

### Opción A: El suave (`--soft`)
```bash
git reset --soft b2c3d4e
```

Borra los commits malos del historial, pero **conserva todos tus cambios** en los archivos y los deja metidos en el "carrito" (verdes en el `git status`), listos para hacer un nuevo commit mejor organizado.

### Opción B: El intermedio (Por defecto)
```bash
git reset b2c3d4e
```

Borra los commits del historial, conserva los cambios en tus archivos, pero los **saca del carrito** (rojos en el `git status`). Tienes que volver a hacer `git add` de lo que quieras guardar. Es ideal si quieres revisar tu código con calma.

### Opción C: La opción nuclear (`--hard`)
```bash
git reset --hard b2c3d4e
```

¡Cuidado aquí! Esto borra los commits del historial y **destruye por completo cualquier cambio** que hubieras hecho en los archivos después de ese punto. Tu código volverá a estar exactamente igual que en el commit `b2c3d4e`. Lo que se borra aquí, no se puede recuperar.

## 🛠️ 2. Ejemplo práctico: Borrando el último commit

El uso más común del `git reset` es cuando acabas de hacer un commit y te das cuenta de que te olvidaste de incluir un archivo. En lugar de hacer un commit nuevo, puedes deshacer el último.

En Git, el "lugar donde estás ahora mismo" se llama `HEAD`. Si quieres deshacer el último commit (viajar un paso atrás) conservando tus archivos para añadir lo que faltaba, puedes usar este atajo sin necesidad de buscar el código hash:

```bash
git reset HEAD~1
```

*(El `~1` significa "un paso atrás desde donde estoy ahora").* Ahora puedes añadir el archivo olvidado y volver a hacer el commit correctamente. ¡Nadie sabrá que te equivocaste!

---
**🏆 ¡Reto del Módulo conseguido!** ¡Felicidades! Acabas de dominar las herramientas de rescate de Git. Ya sabes cómo guardar trabajo a medias (`stash`), descartar desastres locales (`restore`), deshacer errores en equipo (`revert`) y reescribir tu propia historia (`reset`). ¡Ya no hay error que se te resista!