# Tema 3: Subiendo tus cambios (`git push`)

Ya tienes el repositorio en GitHub y ya has construido el puente con `remote`. Ahora falta el paso final: enviar tus archivos desde tu ordenador a la nube.

En Git, esta acción se llama **Push** (Empujar).



## 🚀 1. El comando mágico

Para subir tus cambios por primera vez, necesitas ejecutar este comando en tu terminal:

```bash
git push -u origin main
```

### ¿Qué significa cada parte?
* **`git push`**: "Git, empuja mis cambios".
* **`-u`**: (Upstream) Solo se usa la primera vez. Sirve para que Git "recuerde" que, a partir de ahora, tu rama local está conectada siempre con `origin`.
* **`origin`**: El nombre del puente que creamos en el tema anterior.
* **`main`**: El nombre de tu rama principal (donde están tus commits).

⚠️ **¿Te da un error con la palabra "main"?**
Si al ejecutar el comando la terminal te lanza un error diciendo algo parecido a `error: src refspec main does not match any`, es muy probable que tu rama principal se llame `master` (esto es común en versiones más antiguas de Git). La solución es muy sencilla, simplemente cambia la última palabra:

```bash
git push -u origin master
```
> **Nota:** Si tu terminal te pide usuario y contraseña, recuerda que GitHub ya no usa contraseñas normales para la terminal, sino **Tokens de Acceso Personal (PAT)** o la autenticación a través del navegador que configuramos en el Módulo 1.

## 🔄 2. ¿Cómo será a partir de ahora?

La gran ventaja de haber usado el parámetro `-u` la primera vez es que, para todos tus futuros cambios, el comando se simplifica al máximo. 

A partir de ahora, cada vez que hagas un nuevo commit y quieras subirlo, solo tendrás que escribir:

```bash
git push
```
## 🕵️‍♂️ 3. Comprueba el resultado

Una vez que la terminal termine de mostrar mensajes de "Writing objects", haz lo siguiente:
1. Ve a tu navegador.
2. Refresca la página de tu repositorio en GitHub.
3. **¡Magia!** Verás tus archivos, tus carpetas y, lo más importante, tus mensajes de commit profesionales apareciendo en la web.

---
**Siguiente paso:** ¡Enhorabuena! Tu código ya es internacional. Ahora que ya sabes subir contenido, en el próximo tema veremos cómo descargar proyectos (tuyos o de otros) usando la clonación.