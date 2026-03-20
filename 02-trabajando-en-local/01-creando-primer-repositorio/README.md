# Tema 1: Creando tu primer repositorio (`git init`)

¡Ha llegado el momento de la verdad! Vamos a decirle a Git que empiece a vigilar una carpeta de nuestro ordenador.

Un **repositorio** (o "repo" de forma cariñosa) no es más que una carpeta normal y corriente de tu ordenador a la que Git le ha añadido superpoderes para registrar su historial.

## 📂 1. Crea una carpeta para tu proyecto

Abre tu terminal (o la terminal integrada de VS Code) y vamos a crear una carpeta nueva y a entrar en ella. Escribe estos comandos pulsando `Enter` después de cada uno:

```bash
mkdir mi-primer-repo
cd mi-primer-repo
```
*(Nota: Como vimos en el módulo anterior, `mkdir` crea la carpeta y `cd` nos mete dentro de ella. ¡Asegúrate de no saltarte el `cd`!)*

## ✨ 2. La magia de `git init`

Ahora mismo, estás dentro de una carpeta completamente normal. Para convertirla en un repositorio de Git, solo tienes que ejecutar el siguiente comando:

```bash
git init
```
Al hacerlo, verás un mensaje en la terminal parecido a este: `Initialized empty Git repository in...` (Repositorio Git vacío inicializado en...).

## 🕵️‍♂️ ¿Qué ha pasado exactamente?

A simple vista, tu carpeta sigue pareciendo vacía. Sin embargo, Git ha creado una carpeta oculta llamada `.git` en su interior (puedes comprobarlo escribiendo `ls -a` en tu terminal).

Esa carpeta oculta es el **cerebro** de Git. Ahí es donde se va a guardar todo el historial, las versiones y los viajes en el tiempo de tu código. 

> **⚠️ Regla de oro:** ¡Nunca borres ni modifiques a mano el contenido de esa carpeta oculta `.git` a menos que quieras destruir el historial de tu proyecto para siempre!

---
**Siguiente paso:** Ya tenemos nuestro repositorio listo y el "cerebro" de Git funcionando. En el próximo tema aprenderemos a crear archivos y decirle a Git que empiece a guardar nuestros cambios.