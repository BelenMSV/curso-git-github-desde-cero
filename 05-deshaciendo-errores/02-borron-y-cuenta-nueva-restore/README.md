# Tema 2: Borrón y cuenta nueva (`git restore`)

Ponte en situación: estás modificando el archivo `index.html`. De repente, el gato salta sobre el teclado, borras la mitad del código sin querer, le das a guardar por inercia y la página web deja de funcionar por completo. 

El pánico se apodera de ti. ¡Has roto el proyecto! 

Pero entonces recuerdas la regla de oro de Git: **si no has hecho commit, no ha pasado nada.** Como todavía no has guardado esto en el historial, Git tiene una copia perfecta de cómo estaba ese archivo la última vez que hiciste un commit. Vamos a recuperarla.

## 🧽 1. Descartar cambios en un archivo

Para decirle a Git "olvida todo lo que he escrito hoy en este archivo y devuélvelo a como estaba en el último commit", usamos el comando `restore` (restaurar):

```bash
git restore index.html
```

¡Y ya está! Si vuelves a abrir tu editor de código, verás que el archivo ha vuelto mágicamente a la normalidad. Todos los cambios desastrosos que habías hecho sin guardar han desaparecido para siempre.

*(Nota: En tutoriales antiguos de Internet puedes encontrar esto escrito como `git checkout -- index.html`. Hace exactamente lo mismo, pero `git restore` es la forma moderna y recomendada de hacerlo).*

## 🛒 2. ¿Y si ya lo había metido en el carrito?

Imagina otro escenario: hiciste los cambios desastrosos, no te diste cuenta y ejecutaste `git add index.html`. El archivo ya está en el área de preparación (*staging area* o "el carrito"), listo para ser commiteado. 

Si haces un `git status`, verás el archivo en verde. ¡Aún podemos pararlo! Solo tenemos que sacarlo del carrito añadiendo la bandera `--staged` (preparado):

```bash
git restore --staged index.html
```

**Ojo aquí:** Este comando **no borra el código** que has escrito. Simplemente saca el archivo del carrito de Git (pasa de verde a rojo en el `git status`). 

Una vez que está fuera del carrito, si realmente quieres destruir esos cambios y que el archivo vuelva a su estado original, tendrías que ejecutar el comando del primer punto: `git restore index.html`.

## ⚠️ 3. Advertencia de seguridad

El comando `git restore` sin `--staged` es uno de los pocos comandos destructivos en Git. Lo que borres con él, **no se puede recuperar**. Úsalo solo cuando estés 100% seguro de que quieres tirar a la basura las modificaciones que acabas de hacer en ese archivo.

---
**Siguiente paso:** Ya sabemos qué hacer si nos equivocamos antes de hacer el commit. Pero... ¿qué pasa si el gato saltó al teclado, le diste a guardar, hiciste `git add`, hiciste `git commit` y, para colmo, lo subiste a GitHub? ¡Parece el fin del mundo! Tranquilo, en el próximo tema aprenderemos a crear "anti-commits" con `git revert`.