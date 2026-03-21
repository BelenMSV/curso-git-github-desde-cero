# Tema 4: Llevando tu código a todas partes (`git clone`)

La magia de GitHub no es solo subir archivos, sino poder recuperarlos en cualquier momento y en cualquier lugar. Imagina que te compras un ordenador nuevo, que quieres trabajar desde el portátil o que quieres colaborar en el proyecto de un compañero. ¿Cómo te traes todo ese historial a tu máquina?

## 👯 1. El comando `git clone`

`git clone` es el comando que se encarga de descargar un repositorio completo desde GitHub a tu ordenador. No solo descarga la última versión de los archivos, sino **todo el historial de commits, ramas y cambios** que se hayan hecho desde el principio.



## 📍 2. ¿Dónde encontrar el enlace para clonar?

Para clonar un proyecto, necesitas su "dirección de casa". Sigue estos pasos en GitHub:

1. Entra en la página principal del repositorio que quieras descargar.
2. Busca el botón verde brillante que dice **`<> Code`** (está justo encima de la lista de archivos).
3. Al hacer clic, se abrirá un desplegable. Asegúrate de que esté seleccionada la pestaña **HTTPS**.
4. Verás una URL que termina en `.git` (por ejemplo: `https://github.com/usuario/proyecto.git`).
5. Haz clic en el icono de los **dos cuadraditos** a la derecha de la URL para copiarla al portapapeles.

## 🛠️ 3. Cómo clonar en tu terminal

Una vez tengas la URL, ve a tu terminal y sigue estos pasos:

1. Navega hasta la carpeta donde quieras guardar el proyecto (ej: `cd Documentos/Proyectos`).
2. Escribe el comando seguido de la URL que copiaste:

```bash
git clone https://github.com/tu-usuario/mi-primer-repo.git
```

**¿Qué pasará entonces?**
* Git creará una carpeta nueva con el nombre del repositorio.
* Descargará todos los archivos dentro.
* Configurará automáticamente el "puente" (`remote origin`) para que puedas hacer `push` y `pull` de inmediato.

## 🔄 4. Mantenerse actualizado (`git pull`)

Si el repositorio ya lo tienes en tu ordenador pero alguien (o tú mismo desde otro PC) ha subido cambios nuevos a GitHub, no necesitas volver a clonar. Solo tienes que "traer" las novedades:

```bash
git pull origin main
```
*Este comando compara lo que tienes tú con lo que hay en la nube y descarga solo lo que te falte.*

---
**🏆 ¡Módulo 3 Completado!** Has dominado el ciclo de vida profesional: creas en local, subes a la nube y descargas donde quieras. Ya estás listo para el siguiente nivel: **las ramas y el trabajo en equipo**.