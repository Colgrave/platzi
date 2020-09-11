#¿Qué es Responsive Design?
Son todas esas técnicas que usamos para adaptar nuestras aplicaciones web a la mayor cantidad de pantallas

##Patrones en Reponsive Design:

Mostly Fluid (buscar imagenes)
Colocación de columnas (buscar imagenes)
Layout shifter(buscar imagenes)
Tiny tweaks (buscar imagenes)
Off canvas (buscar imagenes)
Para mas información: https://mediaqueri.es

##Conceptos nuevos:

Viewport: área visible del navegador
Portrait: el celular puesto de manera vertical
Landscape: el celular puesto de manera horizontal
Mobile first: empezar un websit desde la menor resolución soportada
Desktop first: empezar un websit desde la mayor resolución soportada

##atributo meta datos
width=device-width para que se adapte según la pantalla del dispositivo
initial-scale=1.0 para indicar el escalado según el dispositivo, donde 0 el 0% de zoom, y 1 el 100%

##Unidades relativas de medida:

Porcentaje: longitud referente al tamaño de los elementos padre
em: unidad relativa al tamaño de fuente especificada más cercano
    
	ejmp <ul>font-size:"15px"
		<li>font-size: 2em (esto equivalira a 30px)
		<a href="">font-size :"0.5em" <stong>font-size 1em </strong><a> ( el a equivaleria a 15 px y como la unidad relativa mas cercana es el a, el strong mediria 15px)

rem: unidad relativa al tamaño de fuente especificada en el ancestro más lejano (html o body)
vw / vh: unidad relativa porcentual con respecto al viewport

##¿Qué son Media Queries?
Es el módulo CSS3 que permite adaptar la representación del contenido a características del dispositivo.

###Estructura del Media Querie:

@media media type and (condición) { }
Mobile First usa min-width y Desktop First usa max-width

 max-width ( hasta)
 min-witdh (desde)


##formas de traer una media queries

 con una hoja nueva de estilos : <link rel="stylesheet" href="media.css" media="screen and (max.witdh:768px)"> el atributo media me permite generar una condicción en donde si el maximo de la pantallas es de 768px, se traera esa hoja de estilos

 desde una misma hoja de estilos : @media screen and (max-width: 768px)

##Breakpoints estandarizados que debemos de tener en cuenta:

Móviles: entre 320 y 480 píxeles.
Tablets: entre 768 y 1024 píxeles.
Pantallas grandes: más de 1024 píxeles o más.

##CSS positions

como su nombre lo indica estas propiedades nos permitiran cambiar la posición a elemnto que se le asignemos:

###tipos de positions

    static: es la propiedad por defecto.
Con las otras opciones, se activan las propiedades de top, bottom, left, right y z-index.

    relative: el objeto se mueve en base al lugar donde se encuentra originalmente. para que este se mueva hay que aplicar las propiedades top, bottom, left, right y z-index 
  
    absolute: el objeto se ubica de manera absoluta con el elemento más cercano que tenga posición relativa o con el body.
    
    fixed: El elemento se muestra de manera fija en el viewport.
    
    
    sticky: El elemento se queda de manera fija una vez que aparece en pantalla.
    
##videos con html5 + poster
    video class="HTML-video" src="https://www.youtube.com/watch?v=LoKvxCSZw5w" width=" " height=" " controls autoplay **poster**="YOUR-IMAGE.jpg"> </video>
    
##insertar contendio anexo a nuestra pagina

Para ello se utiliza la etiqueta iframe: 
    
    iframe src="" frameborder="0"></iframe>
###calcurar la proporción de nuestro video

para que nuestro video este bien ajustado en nuestra pagina hay que realizar esa operación : 

    heigth * 100 / width = padding
    
 hacer esta operación nos permitira de la mejor forma insertar nuestro video sin que eres se estire o pierda su resolución
 
##Algunas intrucciones de JS

     document.querySelector : devuelve el primer elemento que coincide con un selector CSS especificado en el documento.
     ejmp:
	document.querySelector('.menu');
Eso quiere decir que estoy diciendo que traigan las etiquetas que tengan la clase menu

<b>Nota</b>: El método querySelector () solo devuelve el primer elemento que coincide con los selectores especificados. Para devolver todas las coincidencias, utilice el método querySelectorAll () en su lugar.	

    
    classList: La propiedad classList devuelve los nombres de clase de un elemento, como un objeto DOMTokenList.

Esta propiedad es útil para agregar, eliminar y alternar clases CSS en un elemento. ejm


    menu.classList.add('is-active');
    
En esta instrucción se le esta diciendo que me llame la variable menu y a este se agrere **is-active** que puede ser otra clase que me permita cambiar mi elemento.
    
    
    addEventListener:El método document.addEventListener () adjunta un controlador de eventos al documento, eso quiere decir, una acción.
    ejm:
    
     burgerBotton.addEventListener('click', hideShow)

Ahi se le da la instruccion de que a la variable burgerBotton, se le añada la funcion de hideShow cuando a esta se le de click 

	var/const/let: La declaración var declara una variable. Las variables son contenedores para almacenar información.

A pesar de que las tres son variables estas son diferentes

<b>CONST</b>: Es una constante la cual NO cambiara su valor en ningún momento en el futuro. <b>**VAR**</b>: Es una variable que SI puede cambiar su valor y su scope es local. <b>**LET**</b>: Es una variable que también podra cambiar su valor, pero solo funcionara en el bloque donde fue declarada.	

    
    Function: Una función de JavaScript se define con la palabra clave de función, seguida de un nombre, seguido de paréntesis ().

    Los nombres de funciones pueden contener letras, dígitos, subrayados y signos de dólar (las mismas reglas que las variables).

    Los paréntesis pueden incluir nombres de parámetros separados por comas: (parámetro1, parámetro2, ...);
    
    El código que se ejecutará, por la función, se coloca entre llaves: {}
    
## Media queries con JavaScript    

####Window.matchMedia
El método window.matchMedia () devuelve un objeto MediaQueryList que representa los resultados de la cadena de consulta de medios CSS especificada.

El valor del método matchMedia () puede ser cualquiera de las funciones multimedia de la regla CSS @media, como altura mínima, anchura mínima, orientación, etc.

##Creando un servidor de archivos estáticos con Node (Servidor local)	

.Install node.js

.Install npm package globally npm -g install static-server

.Go to the folder you want to serve

.Run the server static-server
	
 
    