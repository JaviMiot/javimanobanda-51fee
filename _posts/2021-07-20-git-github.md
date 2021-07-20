---
title: Lo básico que debes saber de git y Github
layout: post
post-image: "https://drive.google.com/uc?export=view&id=1tHubtdKeJ26Y7eNy8NH_yC3-AUh_0qjG"
description: Git y Github son una de las herramientas principales que debes aprender si estas en el mundo del desarrollo.
tags:
  - Git
  - Github
  - Tecnología
---

Tener un cien números de carpetas para cada versión que vamos liberando de nuestra aplicación resulta al principio una forma fácil para mantener él versionamiento.

¿Pero qué pasaría si cada día tienes un nuevo cambio y debes añadir nuevas funcionalidades a tu proyecto?

<div align="center" >
	<img width="500" style="min-height: 200px;" src="https://drive.google.com/uc?export=view&id=1gOypiedL3rFVmyCbSxAMzyQ657ybAHGS"/>
</div>

Manteniendo nuestra forma de versionamiento tradicional llegaríamos a tener un grupo de carpetas nombradas de forma aleatoria.

<div align="center" >
	<img width="800" style="min-height: 100px;" src="https://drive.google.com/uc?export=view&id=1UnVUvDvgpCwF_RYmqu2PLEA-3yjxM880"/>
</div>

Es aquí donde git y github se convierte en una de nuestras herramientas principales al momento de desarrollar un proyecto.

# ¿Pero que es Git y GitHub?

## Veamos primero que es Git

Git es un sistema de control de versiones local de código abierto que permite tener el historial de todos los cambios realizados de forma rápida y eficiente. Utilizada para proyectos pequeños y complejos.

Entre sus ventajas:

- Guarda el historial de todos los cambios realizados.
- Se puede viajar en el tiempo para recuperar una versión anterior.
- Se puede crear varias ramas del proyecto para realizar pruebas.

## ¿Y que pasa con Github?

Github es una plataforma donde alojaremos nuestro proyecto usando el sistema de control de versiones de git.

Permite colaborar con otros desarrolladores principalmente en la creación de código fuente de programas ordenados.
En otras palabras es la red social de los programadores, donde compartes y colaboras en nuevos proyectos.

## ¿Cómo trabaja Git?

Imaginemos por un momento que iniciamos un archivo llamado mi proyecto.txt (para fines prácticos usaremos un archivo .txt).

<div align="center" >
	<img width="500" style="min-height: 200px;" src="https://drive.google.com/uc?export=view&id=10l4n27iwJfLAKKUgDsG9IOsWfZT_CCK0"/>
</div>

Git almacenará cada cambio que vamos realizando y tendrá un historial tanto del proyecto con el último cambio y con el cambio anterior.

Veamos como trabaja git utilizando la siguiente imagen como una guía del flujo de vida del versionamiento.

<div align="center" >
	<img width="500" style="min-height: 200px;" src="https://drive.google.com/uc?export=view&id=1YpY-g_54O99XEQHjHR9QKw1zZhNirJcH"/>
</div>

Primero para iniciar un repositorio con git se iniciará con el comando `git init` donde inicialmente todos los archivos se encuentran en memoria ubicada en el working area (directorio del proyecto).

Estos archivos no se encuentran trackeados, es decir no se tiene el historial en el repositorio de los cambios realizados en los archivos.

Al correr el comando `git add` agrega el archivo al **staging area** donde se empieza hacer un seguimiento de los cambios realizados en dicho archivo, pero aún no está en el repositorio.

Finalmente al hacer un `git commit`el archivo que se encontraba en staging pasa al repositorio local de git.

### Resumiendo un poco

---

**Archivos Untracking**: son los archivos que nunca se ha realizado un `git add`, y solo están almacenados en el disco duro. Git no sabe de la existencia de ellos.

**Archivos tracking:** son archivos que están en Git, no tienen cambios pendientes y que están en el repositorio local al hacer `git add` y `git commit`.

**Archivos stage:** son los archivos que se ha realizado un `git add`y pasan al staging area. Git conoce sobre la existencia de estos archivos, pero no están en el repositorio hasta que se realice un `git commit`.

**Archivos Unstage:** se puede considerar como archivos untracking-stage. Estos archivos ya estuvieron en el staging y el repositorio al hacer `git add`y `git commit` pero ahora tienen un nuevo cambio ocasionando que el nuevo cambio necesite realizar un `git add`para que la nueva modificación entre a staging y `git commit`para que se almacene al repositorio local.

**Working Area:** es el directorio raíz de nuestro proyecto que actualmente contiene todos nuestros archivos que deseamos versionar.

**Staging Area:** es el lugar a donde pasa un archivo al ejecutarse el comando `git add`en donde se almacena los últimos cambios de los archivos, pero no están en el repositorio hasta realizar un `git commit`.

En la siguiente figura puedes ver como es el flujo simplificado.

<div align="center" >
	<img width="500" style="min-height: 200px;" src="https://drive.google.com/uc?export=view&id=1S-WSAdq_nimD4n92Uw9QG-1polCwNYkm"/>
</div>

# Creando líneas temporales

Imagina ahora poder crear una nueva línea temporal en tu proyecto algo así como un crear nuevas ramas de la línea temporal y crear el multiverso.

<div align="center" >
	<img width="500" style="min-height: 200px;" src="https://img.vixdata.io/pd/jpg-large/es/sites/default/files/l/linea_sagrada_del_tiempo_ramificada.jpg"/>
</div>

Todo esto es posible con Git y su forma de crear ramas de tu proyecto sin afectar otra rama.

Miremos el siguiente ejemplo donde se tiene una rama principal **main** que tiene el flujo normal en el desarrollo de nuestro proyecto.

Pero en un punto en la versión número 3 se nos ocurre hacer unas pruebas en nuestro código que podría afectar al código de producción (main), en este caso podemos crear una nueva rama o una linea de tiempo diferente de nuestro proyecto, en donde no afecta al código de la rama main.

Es aquí donde vemos el potencial de git, permitiéndonos tener en paralelo dos ramas que partieron inicialmente de un proyecto en común.

Ahora tomemos la situación en donde la rama de **pruebas** en la versión 4 tiene un bug que debe ser reparado en este caso en particular vamos a crear una rama llamada **Bug Fixing** y regresaremos a nuestra rama **pruebas** para continuar con nuestro proyecto. Teniendo 2 finales alternativos de nuestro proyecto.

<div align="center" >
	<img width="700" style="min-height: 200px;" src="https://drive.google.com/uc?export=view&id=1Anne045aTBV6zmpGJzWFz_6WdQ5T_-tT"/>
</div>

Tal vez ahora te preguntes ¿qué pasaría si necesitamos unir las dos ramas en una sola y si eso es posible?.

Si, se puede unir las dos ramas haciendo un **merge** y una de las principales características de git es el control de conflictos en el caso de que 2 líneas de código fueran modificadas en las dos ramas diferentes y que ahora van a ser una sola rama. Git te permitirá mantener o borrar dicho cambio de una u otra rama al momento de hacer el merge, esa decisión la tomas tú o el encargado del proyecto.

<div align="center" >
	<img style="height: 100%; min-height: 200px; width:700px" src="https://cl.buscafs.com/www.tomatazos.com/public/uploads/images/336833/336833_1140x516.jpg"/>
</div>

Git es una de las herramientas principales que debes aprender si estas en el mundo del desarrollo. No solo tendrás un sistema de versionamiento que te evitara muchos dolores de cabeza al realizar tus aplicaciones. Te abrirá a colaborar con otros desarrolladores y tener buenas prácticas de desarrollo que muchas startups buscan en sus colaboradores.
