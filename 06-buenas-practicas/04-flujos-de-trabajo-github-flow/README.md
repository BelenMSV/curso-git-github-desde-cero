# Tema 4: Flujos de trabajo (GitHub Flow)

Has aprendido a hacer commits, ramas, a fusionar código, a resolver conflictos y a viajar en el tiempo. Tienes todas las piezas del puzzle. Ahora la pregunta es: cuando entras a trabajar a una empresa real el lunes a las 9:00 de la mañana... ¿en qué orden usas todas estas herramientas?

Para que los equipos no se vuelvan locos pisándose el código unos a otros, las empresas usan "Flujos de Trabajo" (Workflows). El más famoso, moderno y utilizado hoy en día se llama **GitHub Flow**.

## 🌊 ¿Qué es el GitHub Flow?

Es una regla de trabajo muy sencilla basada en 5 pasos que garantiza que el código principal del proyecto nunca se rompa.  Funciona así:

### 1. La rama `main` es sagrada 🏛️
En cualquier empresa, la rama `main` es la que está en producción (la que ven los clientes reales en Internet). **La regla de oro absoluta es: nunca, jamás, se hacen commits directamente en `main`.** Esta rama siempre tiene que funcionar a la perfección.

### 2. Crea una rama para tu tarea 🌿
Cuando tu jefe te pide una nueva funcionalidad (por ejemplo, añadir un modo oscuro), lo primero que haces es actualizar tu código y crear una rama nueva a partir de `main` con un nombre descriptivo:
```bash
git checkout main
git pull
git checkout -b feat/modo-oscuro
```

### 3. Trabaja y haz commits 💻
Ahora trabajas en tu ordenador de forma aislada. Haces tus cambios, pruebas que funcionan y vas guardando tu progreso usando los *Conventional Commits* que aprendimos en el Tema 1:
```bash
git add .
git commit -m "feat: crear botón de modo oscuro"
```

### 4. Abre una Pull Request (PR) 📢
Cuando terminas, subes tu rama a GitHub (`git push origin feat/modo-oscuro`). En lugar de fusionarla tú mismo, vas a la web de GitHub y abres una **Pull Request**. 

Una PR es simplemente una petición oficial que dice: *"Hola equipo, he terminado esta tarea. Aquí está mi código, ¿podéis revisarlo antes de meterlo en la rama principal?"*.

### 5. Revisión y Fusión (Merge) 🤝
Tus compañeros leerán tu código, te dejarán comentarios y comprobarán que no rompes nada. Si todo está perfecto, un compañero (o tú mismo, según la empresa) le dará al botón verde de "Merge Pull Request" en GitHub. 

Tu código se fusionará con `main`, ¡y la tarea estará terminada! Después, la rama `feat/modo-oscuro` se borra para mantener el repositorio limpio.

## 🏆 Resumen del flujo

1. Crea una rama desde `main`.
2. Haz commits con tus cambios.
3. Sube la rama y abre una Pull Request.
4. Debate y revisa el código con tu equipo.
5. Haz Merge a `main` y borra tu rama.

---
**🎉 ¡ENHORABUENA! ¡HAS TERMINADO EL CURSO! 🎉**

Mírate. Empezaste sin saber qué era la terminal y ahora dominas el control de versiones, escribes historiales impecables, sabes salir de cualquier apuro y conoces cómo operan los equipos profesionales. Ya tienes la habilidad número uno que exige la industria del software. ¡Estás listo para salir ahí fuera y escribir código increíble!