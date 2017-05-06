# loginphp_PTF

Charla de Xampp + PHP Basica
Lección para Programá tu Futuro, Usuaria
Escrita por César Dutten
Proposito.
Acercar al alumno a la utilización de Php con la ayuda de Xampp para desarrollar sus proyectos de formas más simples. 
MATERIALS NECESARIOS.
Xampp
Template Initializr 
Café
TEMAS A TRATAR.
Instalación de Xampp
Uso de Xampp (Carpeta htdocs)
Crear un Hola Mundo que se pueda ver desde la URL localhost/prueba/index.html
Descargar Initializr para tener un template simple con Bootstrap
Mostrar Initializr desde la URL localhost/initializr/index.html
Dividir el Header, el body  y el footer en 3 archivos PHP e incluirlos de forma dinámica.
Usar la sentencia include() para agregar dinámicamente el Header y footer.
Duplicar el Index.php y renombrarlo a Pagina2.php
Usar este codigo en la NavBAr :





          <nav class="navbar navbar-inverse navbar-fixed-top">
          <div class="container-fluid">
            <!-- Brand and toggle get grouped for better mobile display -->
            <div class="navbar-header">
              <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
                <span class="sr-only">Toggle navigation</span>
                <span class="icon-bar"></span>
                <span class="icon-bar"></span>
                <span class="icon-bar"></span>
              </button>
              <a class="navbar-brand" href="#">Brand</a>
            </div>

            <!-- Collect the nav links, forms, and other content for toggling -->
            <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
              <ul class="nav navbar-nav">
                <li class="active"><a href="index.php"> Inicio<span class="sr-only">(current)</span></a></li>
                <li><a href="pagina2.php"> Pagina2 </a></li>
                <li class="dropdown">
                  <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Dropdown <span class="caret"></span></a>
                  <ul class="dropdown-menu">
                    <li><a href="#">Action</a></li>
                    <li><a href="#">Another action</a></li>
                    <li><a href="#">Something else here</a></li>
                    <li role="separator" class="divider"></li>
                    <li><a href="#">Separated link</a></li>
                    <li role="separator" class="divider"></li>
                    <li><a href="#">One more separated link</a></li>
                  </ul>
                </li>
              </ul>
              <form class="navbar-form navbar-left">
                <div class="form-group">
                  <input type="text" class="form-control" placeholder="Search">
                </div>
                <button type="submit" class="btn btn-default">Submit</button>
              </form>
              <ul class="nav navbar-nav navbar-right">
                <li><a href="#">Link</a></li>
                <li class="dropdown">
                  <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Dropdown <span class="caret"></span></a>
                  <ul class="dropdown-menu">
                    <li><a href="#">Action</a></li>
                    <li><a href="#">Another action</a></li>
                    <li><a href="#">Something else here</a></li>
                    <li role="separator" class="divider"></li>
                    <li><a href="#">Separated link</a></li>
                  </ul>
                </li>
              </ul>
            </div><!-- /.navbar-collapse -->
          </div><!-- /.container-fluid -->
        </nav>


Setear Variables $active_page y $title. 
¡Importante debe ser antes del Include del header para que funcione!
Crear If para setear la clase Active en la página correspondiente. 
Segunda Parte:
“Sistema de Login y Registro con PHP”
Base de datos 

/* Create Database */
CREATE DATABASE userlitdb;
 
/* Create Table */
 CREATE TABLE `usertbl` (
 `id` int(11) NOT NULL auto_increment,
 `full_name` varchar(32) collate utf8_unicode_ci NOT NULL default '',
 `email` varchar(32) collate utf8_unicode_ci NOT NULL default '',
 `username` varchar(20) collate utf8_unicode_ci NOT NULL default '',
 `password` varchar(32) collate utf8_unicode_ci NOT NULL default '',
 PRIMARY KEY (`id`),
 UNIQUE KEY `username` (`username`)
) ENGINE=MyISAM DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;
