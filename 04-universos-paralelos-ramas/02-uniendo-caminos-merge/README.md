# Tema 2: Uniendo los caminos (`git merge`)

Tu experimento en el "universo paralelo" ha sido un éxito rotundo. Has programado esa nueva función, la has probado y no ha roto nada. ¡Genial! 

Ahora llega el momento de llevar todo ese buen trabajo a tu proyecto oficial. En Git, la acción de fusionar una rama con otra se llama **Merge** (Unir o Fusionar).



## 🎯 1. La regla de oro del Merge

Antes de ejecutar ningún comando, debes entender cómo piensa Git: **las fusiones siempre atraen los cambios hacia ti**. 

Piensa que eres un imán. Si quieres traer los cambios de tu rama experimental hacia la rama `main`, **primero tienes que viajar a `main`**.

### Paso 1: Viaja a la rama de destino
Asegúrate de estar en la línea de tiempo principal:
```bash
git switch main
```

*(Opcional pero recomendado):* Si trabajas con más gente, siempre es buena idea hacer un `git pull` aquí para asegurarte de tener la última versión de la nube antes de fusionar nada.

## 🧲 2. El comando mágico (`git merge`)

Una vez que estás seguro y acomodado en tu rama `main`, solo tienes que decirle a Git qué rama quieres "absorber". 

Ejecuta este comando usando el nombre de la rama que creaste en el tema anterior:

```bash
git merge experimento-boton
```

**¿Qué pasará entonces?**
Git cogerá todos los commits que hiciste en tu rama `experimento-boton` y los aplicará en `main`. ¡Tu línea de tiempo oficial ahora tiene la nueva función!

## 🧹 3. Limpiando la casa (`git branch -d`)

Una vez que has fusionado tu rama, ese universo paralelo ya no tiene ninguna utilidad. Ya cumplió su propósito. 

Es una excelente práctica borrar las ramas que ya han sido fusionadas para no acumular basura en tu proyecto. Para borrar una rama local, usamos el parámetro `-d` (delete):

```bash
git branch -d experimento-boton
```

> **🛡️ Git te protege:** Si intentas borrar una rama con `-d` pero se te olvidó hacer el `merge` primero, Git lanzará un error y no te dejará borrarla para que no pierdas tu trabajo. (Si *realmente* quieres borrarla aunque pierdas el trabajo, tendrías que forzarlo con una D mayúscula: `-D`).

---
**Siguiente paso:** En un mundo ideal, todos los `merge` funcionan a la primera. Pero, ¿qué pasa si tú modificaste la línea 10 en `main` y también modificaste la línea 10 en tu rama experimental? ¡Git no sabrá con cuál quedarse! Eso se llama **Conflicto**, y en el próximo tema aprenderemos a resolverlo sin pánico.