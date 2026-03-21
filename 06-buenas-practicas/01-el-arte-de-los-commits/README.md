# Tema 1: El arte de escribir commits (Conventional Commits)

Imagina que entras a trabajar en una empresa y te piden que revises el historial de un proyecto para saber qué se hizo la semana pasada. Abres la terminal, escribes `git log` y te encuentras esto:

* `commit 8a2b1`: *arreglado*
* `commit 9c4d2`: *cosas*
* `commit 1f3a4`: *asdfghjkl*
* `commit 7e5t6`: *ahora sí funciona por favor*

¿Te enteras de algo? Exacto, de nada. Escribir buenos mensajes de commit no es solo una cuestión estética; es una herramienta de comunicación vital para tu equipo (y para tu "yo" del futuro cuando vuelvas a leer tu código en seis meses).

Para solucionar este problema, la industria del software creó un estándar llamado **Conventional Commits** (Commits Convencionales).

## 🏷️ 1. ¿Qué son los Conventional Commits?

Es una convención muy sencilla para dar formato a los mensajes de commit. Se basa en añadir un **prefijo** que indique claramente qué tipo de cambio se ha hecho, seguido de dos puntos y una breve descripción en minúsculas.

La estructura básica es:
`tipo: descripción breve de lo que has hecho`

Por ejemplo: 
`git commit -m "feat: añadir botón de inicio de sesión"`

## 🛠️ 2. Los prefijos más utilizados en la industria

Aquí tienes la lista de los prefijos estándar que deberías empezar a usar desde hoy mismo:

* **`feat:`** (Feature): Cuando añades una funcionalidad nueva a tu proyecto. *(Ej: `feat: crear formulario de contacto`)*
* **`fix:`** Cuando solucionas un error o bug en el código. *(Ej: `fix: corregir error de cálculo en el carrito`)*
* **`docs:`** (Documentation): Cuando solo modificas archivos de texto, como los `README.md`. *(Ej: `docs: actualizar instrucciones de instalación`)*
* **`style:`** Cuando haces cambios de formato que no afectan al funcionamiento del código (espacios, comas, puntos, tabulaciones). *(Ej: `style: formatear archivo index.js`)*
* **`refactor:`** Cuando reescribes una parte del código para que sea más limpio o eficiente, pero no añades funciones nuevas ni arreglas bugs. *(Ej: `refactor: simplificar función de validación`)*
* **`test:`** Cuando añades o modificas pruebas automatizadas. *(Ej: `test: añadir pruebas para el login`)*
* **`chore:`** (Tareas rutinarias): Para cambios de configuración, actualización de dependencias o herramientas. *(Ej: `chore: actualizar versión de React`)*

## ⚖️ 3. El antes y el después

Veamos la diferencia entre un historial de principiante y uno profesional usando estas convenciones:

**❌ Historial de Principiante (Caótico):**
> * actualizado el readme
> * arreglado el bug del menú
> * diseño nuevo
> * me faltaba un punto y coma

**✅ Historial Profesional (Limpio y escaneable):**
> * `docs: añadir instrucciones al readme`
> * `fix: reparar colapso del menú en móviles`
> * `feat: implementar nuevo diseño de la página principal`
> * `style: corregir formato y sintaxis en app.js`

## 💡 4. Reglas de oro para un buen mensaje

1. **Sé directo y usa verbos en infinitivo:** Usa "añadir", "arreglar", "cambiar" en lugar de "añadido", "arreglando" o "cambios en".
2. **Menos es más:** El mensaje debe caber en una sola línea (idealmente menos de 50 caracteres).
3. **No mientas:** Si el commit es un `fix`, no metas también una funcionalidad nueva (`feat`) en el mismo guardado. ¡Sepáralos en dos commits distintos!

---
**Siguiente paso:** Ahora que tu historial luce como el de un programador Senior, vamos a aprender a proteger tu proyecto. ¿Sabías que subir contraseñas o carpetas súper pesadas a GitHub es uno de los mayores errores de seguridad? En el próximo tema aprenderemos a crear un escudo protector: el archivo `.gitignore`.