---
title: Extensión de Chrome Para Tomar Apuntes de Platzi
layout: post
post-image: "https://i.imgur.com/GgDYI4G.png"
description: 
tags:
- notion
- platzi
- technology
- chrome
---
  
Notion se ha convertido para mí una de las herramientas principales tanto para mi trabajo y aprendizaje, ya que me ha permitido organizar mi documentación. Y conjuntamente con lo que he aprendido sobre desarrollo web me decidí hacer una pequeña herramienta para almacenar mis apuntes en una base de datos de Notion.

 
<div  align="center"  >
	<img  width="300"  src="https://i.imgur.com/eTUKPWU.png"/>
</div>

Para usar esta extensión seguiremos algunos paso:

##  Instalación
---
  Primero debes clonar el proyecto.
```shell
https://github.com/JaviMiot/ChromeExtensionPlatziCourse.git
```
  Ya clonado el proyecto se necesitará tener ciertas autorizaciones para que conectemos la extensión de Chrome con Notion. Para eso seguiremos los siguientes pasos:

1. Tener una integración de la API de Notion esto lo puedes realizar en el siguiente [link](https://www.notion.so/my-integrations)

2. Hacer clic en el botón "+ New integration".

3. Dar un nombre a la integración.

4. Selecciona el workspace donde deseas instalar la integración (En el caso de que tengas varias cuentas de Notion selecciona la que vas a utilizar).

5. Clic en "Submit" para crear la integración.
<div  align="center"  >
	<img  width="600"  src="https://files.readme.io/2ec137d-093ad49-create-integration.gif"/>
</div>

1. Copia y  Guarda el token de la integración, esta la utilizaremos más adelante.

  <div  align="center"  >
	<img  width="400"  src="https://i.imgur.com/jRhuQgy.png"/>
</div>


Esta extensión tiene un templete que lo puedes duplicar en tu propio notion para acceder ingresa [AQUÍ](https://javimiot.notion.site/2b9380cae34b4952808065450308343a?v=903df5f0203b448fabb7150ae9f977b3) y duplica el template en tu notion.
 <div  align="center"  >
	<img  width="600"  src="https://i.imgur.com/7zNLHNU.png"/>
</div>  

Una vez duplicado el template, en la url de la base de datos **copiar y guarda el id de la base de datos**, también la usaremos más adelante.

   <div  align="center"  >
	<img  width="600"  src="https://i.imgur.com/WkIvR05.png"/>
</div>  

```
https://www.notion.so/myworkspace/a8aec43384f447ed84390e8e42c2e089?v=...
                                  |--------- Database ID --------|
```

__Ya duplicado el template de notion vamos a compartirlo con la Integración que creamos anteriormente esto nos permitirá tener acceso a nuestra base de datos para crear las páginas de nuestros apuntes:__

1. Abrir la base de datos como una página y hacer clic en el botón de "Share".

2. Seleccionar la integración que se había creado.
<div  align="center"  >
	<img  width="600"  src="https://files.readme.io/0a267dd-share-database-with-integration.gif"/>
</div>  


###  Uso del Plugin 🔧
---
Una vez que tengas el **token de la integración de Notion** y el **Id de la base de datos**.

Se procede a instalar de forma local el plugin.

1. Ingresa al administrador de extensiones mediante el navegador a `chrome://extensions`

2. Habilita el modo desarrollador.

3. Clic en el botón "Load unpacked" y selecciona el directorio de la extensión.
<div  align="center"  >
	<img  width="600"  src="https://wd.imgix.net/image/BhuKGJaIeLNPW9ehns59NfwqKxF2/vOu7iPbaapkALed96rzN.png?auto=format&w=571"/>
</div>  
4. Finalmente, tendrás instalada la extensión.

<div  align="center"  >
	<img  width="400"  src="https://i.imgur.com/nToFFcx.png"/>
</div>

##  Mostrar Plugin

Para tener disponible en tu explorador hacer clic en el icono de extensiones y habilitar la extensión.
<div  align="center"  >
	<img  width="400"  src="https://i.imgur.com/aPMOnmn.png"/>
</div>  


##  Configurar Extensión
---
1. Hacer clic derecho sobre el icono del la extensión y seleccionar "options"
<div  align="center"  >
	<img  width="300"  src="https://i.imgur.com/sIjinjC.png"/>
</div>  

2. Nos mostrará una pantalla donde colocaremos el **Token de Notion** y el **Id de la base de datos** que lo obtuvimos anteriormente al crear la integración y al duplicar el template.
<div  align="center"  >
	<img  width="400"  src="https://i.imgur.com/8vxPLfg.png"/>
</div>    
3. Dar clic en "Save" y cerramos la página.

##  Crear tu apuntes de un curso
---
Si haz seguido todos los paso podras ir a tu curso favorito de platzi y este se generar en tu notion.

1. Acceder al plugin
2. Clic en "Obtener Datos del Curso"
3. Clic en "Generar Página"
<div  align="center"  >
	<img  width="700" height="700"  src="https://i.imgur.com/GAFQbGl.png"/>
</div>    

Si te diriges a tu Notion ya tienes el curso generado.
<div  align="center"  >
	<img  width="700"  src="https://i.imgur.com/DCdN37m.png"/>
</div>    

Tambien puedes ver el codigo si quieres hacerles unas mejoras o personalizarla a tu gusto estararia encantado de ver que cosas nuevas le puedes añadir.
- [Extensión de Chrome](https://github.com/JaviMiot/ChromeExtensionPlatziCourse)
- [Api Notion](https://github.com/JaviMiot/ApiNotionChrome)

Si te ha servido de mucho esta información compartelo me ayudarías mucho 😊.