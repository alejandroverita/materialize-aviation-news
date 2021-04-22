# CURSO DE MATERIALIZE

## INTRODUCCION A MATERIALIZE

### FRAMEWORKS ¿QUE SON?

**Materialize** es un framework de CSS

**Frameworks**: Son clases y estilos pre-definidos para construir paginas web de forma rápida


------------

### ¿QUE ES MATERIAL DESIGN?

Es un concepto de diseño que sacó Google con buenas prácticas para poder empezar a generar aplicaciones y páginas web. Ellos entendieron que hay cierta interacción con los usuarios y los dispositivos, las aplicaciones y las páginas.

Se trata de un diseño más limpio, en el que predominan animaciones y transiciones de respuesta, el relleno y los efectos de profundidad tales como la iluminación y las sombras que proporcionan significado sobre lo que se puede tocar y cómo se va a mover.

[Material Design](https://material.io/design "Material Design")


------------

### LOGICA DETRAS DEL GRID SYSTEM


Un Grid System trae 12 columnas y es como divides la posición de las etiquetas contenedoras entre cuantas columnas tenemos que utilizar para maquetar un diseño y luego poder reposicionar todos los elementos al momento de que estemos trabajando de forma responsive.


------------

### DOCUMENTACION Y CARACTERISTICAS DE MATERIALIZE

[Official Page](https://materializecss.com/ "Official Page")

Existen varias formas de poder trabajar con Materialize

- Trabajar con la versión Standard con CSS y JS
- Podemos trabajar proyectos en conjunto con Sass
- Usar CDN → Es recomendable trabajar con CDN ya que al ser Materialize un Framework OpenSource, hay probabilidades que los usuarios ya tengan en caché muchos elementos que ayuden a cargar mas rapido nuestro sitio web
- Usar NPM
- Templates



------------

[========]

## DESARROLLO DEL SITIO

### ELABORACION DEL HEADER

     <header>
            <nav class="container">
                <a href="#" class="brand-logo valign-wrapper"><!-- valing-wrapper centra verticalemnte el contenido -->
                    <img src="assets/img/Logo.jpg" class="responsive-img left" alt="Logo"> <!-- make responsive images -->
                </a>
    
                <ul class="right valign-wrapper">
                    <li><a href="">About us</a></li>
                    <li><a href="">Contact us</a></li>
                    <li><a class="btn" href="#">Register</a></li>
                </ul>
            </nav>
    
            <!-- Promotional image -->
    
            <section class="header-main-pic">
    
            </section>
        </header>


------------



### ESTILOS AL HEADER

    body {
        padding: 0;
        margin: 0;
        display: flex;
        min-height: 100vh;
        flex-direction: column;
    }
    
    header {
        height: 500px;
    }
    
    header nav {
        height: 100px;
        background: white;
        box-shadow: none;
    
    }
    
    nav .brand-logo {
        height: 100px;
        left: 15%;
    }
    
    nav .brand-logo img {
        width: 52px;
    }
    
    header nav ul {
        height: 100px;
    }
    
    header ul a {
        color: grey;
    }
    
    .header-main-pic {
        width: 100%;
        height: 400px;
        background-image: url('../assets/img/Banner.jpg');
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
      }

<img src="https://static.platzi.com/media/user_upload/header-25b2c363-1f42-48ff-ba48-e57ef73c1526.jpg" alt="19 de abril Ingenuitity First Flight on Mars">

------------

### CONSTRUCCION DEL MAIN HOMEPAGE

       <main class="container">
            <section>
                <div class="section">
                    <div class="row">
                        <div class="col m7 input-field input-container">
                            <i class="material-icons">search</i>
                            <input id="search" type="text" placeholder="Search">
                        </div>
                    </div>
                </div>
            </section>
            <section>
                <div class="row">
                    <article class="col s12 m6 l4">
                        <div class="card">
                            <div class="card-image waves-effect-waves-block waves-light"><img src="assets/img/card1.png" alt="Card One" class="activator"></div>
                        </div>
                    </article>
                </div>
            </section>
        </main>


------------

### FINALIZANDO CARDS EN EL HOMEPAGE

<img src="https://static.platzi.com/media/user_upload/cards-3d00a679-5be9-4669-8389-b3c8d75fc8b0.jpg" alt="cards">


------------

### TERMINANDO EL INDEX Y LOS ESTILOS HOMEPAGE

Clase para agregar sombras:
`z-depth-2`

Para aplicar la parte de cascade de css se deben colocar las clases
de la siguiente manera y así no hayan conflictos con los estilos.
`.input-field.input-container`

La herencia en css se hace de la siguiente forma:
`.input-field > #search`


------------

### DESARROLLO DE LA PAGINA DE ARTICULO

[Hide Content](https://materializecss.com/helpers.html)
`.hide` añadir a nuestro section del input search

Clase `.section` genera un espacio para marcar una seccion diferente para diferenciarla del contenido

[Cards](https://materializecss.com/cards.html)

[Pagina de imagenes random](https://picsum.photos/)


<img src="https://static.platzi.com/media/user_upload/post-0c02990e-6336-44de-99b4-f030d8c27da7.jpg" alt="post">


------------

### DESARROLLO DEL FORMULARIO DE REGISTRO

Don't repeat yourself: Es aconsejable tener dividido el codigo en componentes para no repetir el mismo codigo en las demas paginas. Por este momento, es válido porque solo se esta usando HTML y CSS

- Aplicar hide al section de la imagen principal para que no aparezca en nuestro `registro.html`

- class `container` delimitara la zona del contenido y se ajustara al tamaño del `nav`

- HTML




```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aviation News</title>
    <!--Import Google Icon Font-->
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
    <!-- Compiled and minified CSS -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/css/materialize.min.css">
    <link rel="stylesheet" href="css/main.css">
</head>
<body>

    <!-- HEADER -->
    <header>
        <nav class="container">
            <a href="#" class="brand-logo valign-wrapper"><!-- valing-wrapper centra verticalemnte el contenido -->
                <img src="assets/img/Logo.jpg" class="responsive-img left z-depth-2" alt="Logo"> <!-- make responsive images -->
            </a>

            <ul class="right valign-wrapper">
                <li><a href="">About us</a></li>
                <li><a href="">Contact us</a></li>
                <li><a class="btn" href="registro.html">Register</a></li>
            </ul>
        </nav>

        <!-- Promotional image -->

        <section class="header-main-pic z-depth-2 hide">

        </section>

        <!-- TITLE -->

        <section class="container">
            <div class="row registro-titulo">
                <div class="col s12">
                    <h1 class="center-align">Register in Aviation News</h1>
                </div>
            </div>
        </section>
    </header>

    <!-- END OF HEADER -->

    <!-- MAIN -->

    <main class="container">

       <div class="row">
           <div class="col s12">
               <div class="card-panel">
                   <form action="">

                       <div class="row section">
                           <div class="input-field col s12 m6">
                               <input type="text" id="first-name" class="activate">
                               <label for="first-name">Name</label>
                            </div>
                           <div class="input-field col s12 m6">
                               <input type="text" id="last-name" class="activate">
                               <label for="last-name">Last Name</label>
                            </div>
                       </div>

                       <div class="row">
                            <div class="input-field col s12 m6">
                                <input type="text" id="email" class="activate">
                                <label for="email">Email</label>
                            </div>
                            <div class="input-field col s12 m6">
                                <input type="password" id="password" class="activate">
                                <label for="password">Password</label>
                            </div>
                       </div>

                   </form>
               </div>
           </div>
       </div>


    </main>

    <!-- END OF MAIN -->

    <footer class="page-footer"></footer>


<!-- Compiled and minified JavaScript -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/js/materialize.min.js"></script>
</body>
</html>
```


------------

### DESARROLLO DE CHECKBOXES EN EL FORMULARIO

Materialize sugiere la siguiente estructura para los inputs tipo
checkbox:

	<label class=“col s12 m4”>
	<input type=“checkbox”>
	<span>Política</span>
	</label>

Sirven para dar diseño especial a los botones:

`waves-effect waves-light`


------------


