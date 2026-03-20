# Tema 3: Los "ojos" de Git (`git status` y `git log`)

Hasta ahora hemos creado un repositorio, añadido un archivo al "carrito" y guardado nuestro primer cambio a ciegas. 

Para trabajar con seguridad, necesitamos saber en todo momento qué está pasando. Git nos ofrece dos comandos que funcionan como nuestros "ojos" dentro del proyecto.

## 📡 1. El Radar: `git status`

Este es, sin duda, **el comando que más vas a utilizar en toda tu vida como desarrollador**. 

`git status` te dice exactamente en qué estado se encuentra tu proyecto en este preciso instante. Ábrelo en tu terminal y escribe:

```bash
git status
```
Git te responderá con información súper valiosa. Te dirá si:

* Hay archivos nuevos que Git aún no está vigilando (*Untracked files*).
* Hay archivos modificados que no has metido en el carrito.
* Hay archivos en el carrito (*Staging area*) listos para el próximo `commit`.
* O si todo está limpio y guardado (*working tree clean*).

> **💡 Regla de oro:** Acostúmbrate a escribir `git status` antes de hacer un `git add`, y vuélvelo a escribir antes de hacer un `git commit`. ¡Te ahorrará muchísimos dolores de cabeza!

## 📖 2. La Máquina del Tiempo: `git log`

Mientras que `status` te dice el presente, `log` te cuenta el pasado. Este comando te muestra el historial de todos los commits que se han hecho en el proyecto.

Escribe en tu terminal:
```bash
git log
```
Verás una lista con tu primer commit. Por cada commit, Git te muestra:

1. Un código largo de letras y números (el **hash** o identificador único de ese commit).
2. El autor (tu nombre y tu correo, ¡por eso los configuramos en el Módulo 1!).
3. La fecha exacta.
4. El mensaje del commit que escribiste.

*(Nota: Si alguna vez el historial es muy largo y la terminal se queda "atrapada" mostrando el texto, simplemente pulsa la tecla **`q`** para salir y volver a escribir comandos).*

### ✨ El truco para profesionales: `git log --oneline`

Cuando tengas 50 commits, leer el historial normal será eterno. Prueba a escribir este comando:

```bash
git log --oneline
```

Esto comprimirá cada commit en una sola línea, mostrándote solo el identificador corto y el mensaje. ¡Es una vista mucho más limpia y rápida!

---
**Siguiente paso:** Ahora que sabemos cómo leer el historial, te habrás dado cuenta de que si los mensajes de los commits son malos, el historial no sirve de nada. En el próximo tema aprenderemos a escribir mensajes como un auténtico profesional.