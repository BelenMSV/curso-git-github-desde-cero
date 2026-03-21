# Tema 3: Cuando los universos chocan (Resolución de Conflictos)

Si llevas un tiempo usando Git, es inevitable que tarde o temprano al hacer un `merge` la terminal se llene de texto y veas la temida palabra: **CONFLICT**. 

Lo primero: **Respira. No has roto nada.** Un conflicto no es un error informático. Es simplemente Git levantando la mano y diciendo: *"Oye, las dos ramas que intentas unir han modificado exactamente la misma línea de código y no sé con cuál quedarme. ¡Ayúdame a decidir!"*.



## ⚔️ 1. ¿Cómo se ve un conflicto en el código?

Cuando ocurre un conflicto, Git detiene el `merge` a la mitad y modifica tus archivos para mostrarte las dos versiones enfrentadas. 

Si abres el archivo en conflicto en tu editor de código (como VS Code), verás algo muy parecido a esto:

```text
<<<<<<< HEAD
<h1>Bienvenidos a mi página de color Azul</h1>
=======
<h1>Bienvenidos a mi web de color Rojo</h1>
>>>>>>> experimento-colores
```
### Anatomía del conflicto:
* `<<<<<<< HEAD`: Indica dónde empieza la versión de la rama en la que estás actualmente (normalmente `main`).
* `=======`: Es la línea divisoria. Separa tu versión de la versión que viene de la otra rama.
* `>>>>>>> experimento-colores`: Indica dónde termina la versión de la rama que estás intentando absorber.

## 🛠️ 2. Cómo resolver el conflicto paso a paso

Resolver un conflicto es, literalmente, editar texto. Solo tienes que seguir estos 3 pasos:

**Paso 1: Decide qué te quedas**
Borra las líneas raras que añadió Git (`<<<<<<<`, `=======`, `>>>>>>>`) y deja el código exactamente como quieres que sea la versión final. Puedes quedarte con la versión de arriba, con la de abajo, ¡o reescribir una línea totalmente nueva combinando ambas!

Por ejemplo, lo dejamos así:
```html
<h1>Bienvenidos a mi página de color Morado</h1>
```

**Paso 2: Dile a Git que ya está solucionado**
Guarda el archivo en tu editor. Luego, ve a tu terminal y añade el archivo al "carrito" para marcarlo como resuelto:
```bash
git add nombre-del-archivo.html
```

**Paso 3: Cierra la fusión**
Por último, solo queda hacer el commit para finalizar el `merge` que se había quedado a medias:
```bash
git commit -m "fix: resolver conflicto de colores en el titulo"
```

¡Y listo! El conflicto ha desaparecido y las ramas se han fusionado con éxito.

## 🚨 3. Botón del pánico: Abortar misión

A veces te encuentras con un conflicto gigante, te agobias, borras cosas sin querer y no sabes cómo volver atrás. Git tiene un "botón del pánico" para cancelar la fusión y dejar todo exactamente como estaba antes de que escribieras `git merge`:

```bash
git merge --abort
```

Úsalo sin miedo si necesitas parar, respirar y volver a intentarlo desde cero.

---
**Siguiente paso:** Ya dominas el arte de crear ramas, fusionarlas y resolver problemas en tu propio ordenador. En el último tema de este módulo, llevaremos todo este conocimiento a GitHub para aprender a trabajar en equipo con las famosas **Pull Requests**.