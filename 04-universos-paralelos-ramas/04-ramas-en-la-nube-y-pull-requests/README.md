# Tema 4: Ramas en la nube y Pull Requests (El trabajo en equipo)

Imagina que trabajas en una empresa. Has creado una rama local, has programado una función increíble y funciona perfecto. ¿Haces un `git merge` a `main` tú solo? ¡No! En los equipos de trabajo, el código siempre debe ser revisado por otra persona antes de unirse a la versión oficial.

Para eso usamos GitHub y su herramienta estrella: las **Pull Requests (Peticiones de extracción)**.



## ☁️ 1. Subiendo tu rama a Internet

Acabas de crear una rama local llamada `mi-nueva-funcion` y has hecho un par de commits en ella. El primer paso es subir esa rama a GitHub.

Como GitHub no sabe que esta rama existe (la creaste en tu ordenador), la primera vez que la subas debes decirle que cree la conexión, igual que hicimos en el Módulo 3:

```bash
git push -u origin mi-nueva-funcion
```

A partir de ese momento, si haces más commits en esa rama, bastará con hacer un simple `git push`.

## 🤝 2. Abriendo la Pull Request (PR)

Una vez que has subido tu rama, ve a tu repositorio en la página web de GitHub. ¡Verás que GitHub es muy listo! Te aparecerá un enorme recuadro amarillo o verde avisándote de que acabas de subir una rama nueva, junto con un botón que dice **"Compare & pull request"**.

1. Haz clic en ese botón.
2. Escribe un título claro y una descripción explicando qué hace tu nuevo código (ej. "Añadido botón de modo oscuro").
3. Haz clic en **"Create pull request"**.

¡Felicidades! Acabas de abrir un espacio de debate. Ahora tus compañeros pueden ver exactamente qué líneas de código has añadido o borrado, dejarte comentarios, pedirte cambios y, finalmente, aprobar tu trabajo.

## 🟢 3. Fusionando en la nube

Una vez que tu código ha sido revisado y aprobado (o si estás trabajando solo y decides aprobarlo tú mismo), es hora de fusionarlo.

En la misma página de la Pull Request en GitHub, verás un botón verde grande que dice **"Merge pull request"**. Haz clic en él y confirma. 

¡Magia! GitHub acaba de hacer el `git merge` por ti directamente en la nube. Tu rama `mi-nueva-funcion` se ha unido a la rama `main` oficial de Internet.

## 🔄 4. Sincronizando tu ordenador (¡Paso clave!)

¡Atención aquí, porque este es el error número uno de los principiantes! 

Has hecho la fusión en GitHub, por lo que el `main` de Internet está actualizado. **Pero tu ordenador no se ha enterado.** Tu `main` local sigue estando en el pasado. 

Siempre que se apruebe una Pull Request en la nube, debes bajar esos cambios a tu ordenador:

1. Viaja a tu rama principal:
```bash
git switch main
```

2. Descarga la versión actualizada de Internet:
```bash
git pull
```

---
🏆 **¡Reto del Módulo conseguido!** Ya sabes crear ramas, resolver conflictos y colaborar en GitHub como un verdadero profesional de la industria. Estás listo para trabajar en cualquier equipo de desarrollo.