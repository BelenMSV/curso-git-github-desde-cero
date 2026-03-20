# Tema 4: Commits Convencionales (Escribiendo como un profesional)

Ahora que sabes cómo hacer *commits* y cómo leer el historial con `git log`, te darás cuenta de un pequeño problema: si escribes mensajes como "guardando cambios", "ahora sí funciona" o "asdasdasd", en unas semanas no tendrás ni idea de qué hiciste.

Para solucionar esto, la industria del software utiliza un estándar llamado **Commits Convencionales** (*Conventional Commits*). 

## 📏 ¿Qué son los Commits Convencionales?

Es un conjunto sencillo de reglas para escribir mensajes. Su objetivo es crear un historial de proyecto que sea fácil de leer tanto para humanos como para herramientas automáticas.

Además, esta convención encaja perfectamente con **SemVer** (Versionado Semántico, es decir, cómo se numeran las versiones de los programas, por ejemplo: `v1.2.0`), ya que el tipo de commit ayuda a decidir si la nueva versión es una actualización mayor o menor.

## 🏗️ La Estructura de un Mensaje

Un mensaje de commit profesional debe tener la siguiente estructura básica:

```text
<tipo>(<ámbito opcional>): <descripción breve>

[cuerpo opcional con más detalles]
```
* **Tipo:** La palabra clave que indica qué clase de trabajo has hecho.
* **Ámbito (Scope):** (Opcional) Indica la parte del código afectada (ej: `(carrito)`, `(login)`).
* **Descripción:** Un resumen corto de lo que hace el commit (se escribe en infinitivo).
* **Cuerpo:** Explicación mas completa de lo que hace el commit.

### 1. 🏷️ Tipos de Commits (El vocabulario clave)

Aquí tienes la lista de los prefijos más utilizados y cuándo debes usarlos:

* ✨ **`feat:`** (Feature) Una nueva funcionalidad o característica para el usuario.
  * *Ejemplo:* `feat: añadir botón de inicio de sesión con Google`
* 🐛 **`fix:`** Corrección de un error o bug.
  * *Ejemplo:* `fix: corregir cálculo de impuestos en el carrito`
* 📚 **`docs:`** Cambios exclusivos en la documentación (como este archivo README).
  * *Ejemplo:* `docs: actualizar instrucciones de instalación`
* 💅 **`style:`** Cambios visuales o de formato en el código (espacios, comas, puntos) que no afectan a cómo funciona el programa.
  * *Ejemplo:* `style: eliminar espacios en blanco sobrantes`
* ♻️ **`refactor:`** Cambios en el código que no corrigen errores ni añaden funcionalidades, pero mejoran la estructura o la limpieza del código interno.
  * *Ejemplo:* `refactor: simplificar la función de validación de correos`
* 🧪 **`test:`** Adición o modificación de pruebas automáticas.
  * *Ejemplo:* `test: añadir pruebas para el registro de usuarios`
* 🛠️ **`chore:`** Tareas rutinarias, actualizaciones de dependencias o configuración que no modifican el código de tu aplicación directamente.
  * *Ejemplo:* `chore: actualizar la librería de iconos a la versión 2.0`

#### Tipos avanzados (Para cuando trabajes en grandes proyectos)
* 🚀 **`perf:`** (Performance) Cambios que mejoran el rendimiento y la velocidad.
* ⏪ **`revert:`** Revierte (deshace) un commit anterior.
* 🤖 **`ci:`** Cambios en archivos de configuración de Integración Continua (ej: GitHub Actions).
* 📦 **`build:`** Cambios que afectan al sistema de compilación o empaquetado del proyecto.

### 2. El Ámbito (Scope): ¿Dónde hiciste el cambio?
Justo después del tipo de commit, puedes añadir opcionalmente entre **paréntesis** el ámbito o contexto de tu cambio. Esto le dice a tu equipo exactamente qué parte del proyecto has tocado.

* *Ejemplo sin ámbito:* `feat: añadir botón de pago`
* *Ejemplo con ámbito:* `feat(carrito): añadir botón de pago`
* *Otro ejemplo:* `fix(login): corregir error al recuperar contraseña`

### 3. La Descripción
Es el resumen corto de lo que hace el commit. 

> **💡 Regla de oro para la descripción:** Escríbela siempre en **infinitivo** o imperativo (ej: "añadir", "corregir", "eliminar"), todo en minúsculas, sin punto final y que no supere los 50 caracteres.

### 4. El Cuerpo (Mensajes largos)
La descripción corta está muy bien para cambios simples, pero a veces necesitas explicar **por qué** hiciste un cambio complejo o **cómo** lo solucionaste. 

Para ello, usamos el cuerpo del mensaje. Se escribe dejando una línea en blanco obligatoria después de la descripción. 

Aquí tienes un ejemplo de un commit completo y profesional:

```text
feat(perfil): añadir opción para subir foto de avatar

Se ha integrado la nueva librería de compresión de imágenes para que los
usuarios puedan personalizar su perfil sin sobrecargar el servidor. 

- Se aceptan formatos JPG y PNG.
- El tamaño máximo de subida es de 2MB.
- La imagen se recorta automáticamente a un formato cuadrado.
```

> **⌨️ ¿Cómo escribo mensajes de varias líneas en la terminal?**  Si usas `git commit -m "mensaje"`, solo puedes escribir una línea. Para escribir mensajes largos, simplemente escribe `git commit` (sin la `-m`) en tu terminal y pulsa Enter. 
> Git abrirá tu editor de texto predeterminado para que puedas escribir con calma todo el texto que necesites. Cuando termines, guardas el archivo, lo cierras, ¡y el commit se creará automáticamente!

---

**🏆 ¡Felicidades! Has terminado el Módulo 2.** Ya sabes crear repositorios locales, guardar cambios de forma profesional y leer el historial. En el próximo módulo, daremos el salto a la nube y aprenderemos a conectar nuestro trabajo con **GitHub**.
