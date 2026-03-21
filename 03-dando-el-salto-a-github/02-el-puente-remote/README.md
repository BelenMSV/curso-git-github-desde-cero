# Tema 2: El puente de conexión (`git remote`)

Tu ordenador es una isla y GitHub es otra. Para que puedan intercambiar archivos, necesitamos construir un puente invisible. En Git, ese puente se llama **Remote** (Remoto).

## 🔗 1. ¿Qué es un "Remote"?

Un remoto es simplemente una URL (una dirección web) que Git guarda internamente para saber a dónde debe enviar tus cambios. 

Por convención, al puente principal que conecta con GitHub siempre se le llama **`origin`**.

## 🛠️ 2. Cómo añadir el remoto

Vuelve a la pestaña de GitHub que dejamos abierta en el tema anterior. Verás una sección que dice **"…or push an existing repository from the command line"**.

Copia la línea que se parece a esta (¡pero con tu propio usuario!):

```bash
git remote add origin https://github.com/TU_USUARIO/mi-primer-repo.git
```

### Desglose del comando:
* **`git remote add`**: "Git, añade una conexión remota".
* **`origin`**: El nombre que le damos a ese puente (puedes imaginarlo como un alias).
* **`https://...`**: La dirección exacta de tu caja fuerte en la nube.

## 🕵️‍♂️ 3. Comprueba la conexión

¿Quieres estar seguro de que Git ha guardado bien la dirección? Escribe este comando en tu terminal:

```bash
git remote -v
```
Si todo ha ido bien, Git te responderá con dos líneas que muestran la URL de tu repositorio junto a las palabras (fetch) y (push). ¡Felicidades, el puente ya está construido!

> **⚠️ Nota importante:** Si te equivocas al escribir la URL, no te preocupes. Puedes borrar el puente con `git remote remove origin` y volver a empezar, o corregirlo con `git remote set-url origin <nueva_url>`.

---
**Siguiente paso:** El puente está listo, pero aún está vacío. En el próximo tema aprenderemos el comando para "empujar" nuestros archivos a través de ese puente y verlos por fin en GitHub.