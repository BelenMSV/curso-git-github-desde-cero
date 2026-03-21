# Tema 1: Tu casa en la nube (Creando un repositorio en GitHub)

Hasta ahora, todo nuestro trabajo ha vivido únicamente en nuestro ordenador. Si tu disco duro se rompe hoy, perderías tu proyecto para siempre. 😱

¡Es hora de solucionarlo! Vamos a crear un espacio seguro en **GitHub** para guardar una copia exacta de nuestro código.

## 🌐 1. Entra en GitHub

Abre tu navegador, entra en [github.com](https://github.com) e inicia sesión con la cuenta que creaste en el Módulo 1.

Una vez dentro, busca un botón verde que dice **"New"** (Nuevo) en la parte izquierda, o haz clic en el símbolo de **"+"** en la esquina superior derecha y selecciona **"New repository"**.

## 📝 2. Rellena el formulario

Verás una pantalla para configurar tu nuevo proyecto. Sigue estos pasos:

1. **Repository name (Nombre del repositorio):** Para mantener el orden, es una buena práctica usar el mismo nombre que le pusimos a nuestra carpeta local. Escribe: `mi-primer-repo`.
2. **Description (Descripción):** (Opcional) Puedes poner algo como "Mi primer proyecto de prueba aprendiendo Git".
3. **Public vs Private (Público o Privado):**
   * **Public:** Todo el mundo en Internet podrá ver tu código (ideal para crear tu portafolio y conseguir trabajo).
   * **Private:** Solo tú y las personas que invites explícitamente podrán verlo.
   * *Recomendación:* Elige **Public** para este curso.
4. **⚠️ EL PASO MÁS IMPORTANTE:** Asegúrate de dejar **DESMARCADAS** las opciones de "Add a README file", "Add .gitignore" y "Choose a license". 

> **💡 ¿Por qué no marcamos esas casillas?**
> Como nosotros *ya tenemos* un repositorio creado en nuestro ordenador (con los commits y archivos que hicimos en el Módulo 2), necesitamos que la "caja" en GitHub esté **completamente vacía**. Si le pedimos a GitHub que cree archivos iniciales por su cuenta, luego habrá un conflicto al intentar subir nuestro trabajo local.

## 🚀 3. Crea el repositorio

Baja hasta el final de la página y haz clic en el botón verde **"Create repository"**.

¡Y ya está! GitHub te llevará a una página nueva llena de comandos y enlaces. No cierres esa pestaña ni te asustes; es la pantalla de instrucciones que usaremos a continuación.

---
**Siguiente paso:** Ya tenemos la "caja fuerte" vacía en Internet y nuestro código en el ordenador. En el próximo tema aprenderemos a usar `git remote` para construir un puente invisible entre ambos.