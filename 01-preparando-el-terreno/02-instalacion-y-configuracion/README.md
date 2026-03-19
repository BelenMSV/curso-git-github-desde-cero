# Tema 2: Instalación y Configuración Inicial

Antes de empezar a guardar nuestros proyectos y viajar en el tiempo con nuestro código, necesitamos instalar Git y presentarnos formalmente ante él.

## 🛠️ 1. Instalación de Git

Dependiendo de tu sistema operativo, los pasos varían un poco:

* **Windows:** Descarga el instalador desde la [página oficial de Git for Windows](https://gitforwindows.org/) e instálalo (puedes darle a "Siguiente" a todo en la instalación por defecto). Esto instalará un programa llamado **Git Bash**, que es la terminal que usaremos de ahora en adelante.
* **macOS:** Abre la aplicación "Terminal" (la puedes buscar en Spotlight) y escribe `git --version`. Si no lo tienes instalado, el propio Mac te abrirá una ventana preguntándote si deseas instalar las herramientas de desarrollo. Dile que sí.
* **Linux:** Abre tu terminal y usa tu gestor de paquetes. Por ejemplo, en Ubuntu/Debian solo tienes que escribir: `sudo apt install git`.

## 👤 2. Configuración de tu Identidad

Git es muy estricto con la autoría. Necesita saber **quién** está haciendo los cambios en el código para dejarlo registrado en el historial.

Abre tu terminal (recuerda: usa **Git Bash** si estás en Windows) y escribe estos dos comandos. Pulsa `Enter` después de cada uno. 

> **⚠️ Importante:** Asegúrate de cambiar "Tu Nombre" y "tu@email.com" por tus datos reales, manteniendo las comillas. Si ya tienes una cuenta en GitHub, usa el mismo correo electrónico aquí.

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```

## ✅ 3. Comprobación

Para asegurarnos de que todo se ha guardado correctamente, pídele a Git que te muestre la configuración actual escribiendo:

```bash
git config --global --list
```
Si en la lista que aparece en pantalla ves tu nombre y tu correo electrónico... ¡Misión cumplida! Ya tienes tu equipo completamente preparado.