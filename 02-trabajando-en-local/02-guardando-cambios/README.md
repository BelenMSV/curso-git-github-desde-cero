# Tema 2: Guardando tus cambios (`git add` y `git commit`)

En Git, guardar los cambios que haces en tus archivos no es automático como cuando pulsas `Ctrl + S`. Es un proceso más seguro que consta de **dos pasos**. 

Para entenderlo fácilmente, imagina que estás haciendo una compra en un supermercado online:
1. **`git add`**: Es meter los productos en el "carrito de la compra". Seleccionas qué cambios exactos quieres guardar.
2. **`git commit`**: Es darle al botón de "Pagar". Confirmas la compra y queda registrada para siempre con su ticket.

## 📝 1. Crea un archivo de prueba

Antes de guardar nada, necesitamos tener un archivo. Abre tu editor (VS Code) dentro de la carpeta `mi-primer-repo` que creamos en el tema anterior y crea un archivo llamado `historia.txt`. Escribe cualquier frase dentro y guárdalo.

*(Si prefieres usar la terminal en lugar del editor, puedes escribir `echo "Había una vez..." > historia.txt` para crearlo rápidamente).*

## 🛒 2. El carrito de la compra (`git add`)

Ahora, dile a Git que quieres "preparar" este archivo para guardarlo. En Git, a esta zona de preparación se le llama **Staging Area**.

En tu terminal, escribe:
```bash
git add historia.txt
```
> **💡 Truco de oro (`git add .`):** Si has modificado 20 archivos distintos a la vez, no tienes que añadirlos uno por uno. Puedes usar el comando `git add .` (con un punto al final) para meter en el carrito *todos* los archivos modificados de golpe.

## 📸 3. Guardando en el historial (`git commit`)

Ahora que el archivo está en la zona de preparación (en el carrito), vamos a confirmar el cambio y guardarlo en el historial de forma permanente. 

Para ello, hacemos un **commit**. Cada commit necesita obligatoriamente un mensaje corto que explique qué es exactamente lo que estás guardando. Escribe:

```bash
git commit -m "feat: crear archivo de historia inicial"
```
* El parámetro `-m` significa *message* (mensaje).
* El texto entre comillas es tu mensaje. ¡Acostúmbrate a que sean descriptivos y claros!

🎉 **¡Felicidades!** Acabas de realizar tu primer "commit". Ese cambio ya forma parte de la máquina del tiempo de tu proyecto.

---
**Siguiente paso:** Acabas de guardar a ciegas. En el próximo tema aprenderemos a usar los "ojos" de Git para ver qué está pasando en nuestro repositorio en todo momento.