## Intro Sass

### Instalacion

para windows instalar ruby https://rubyinstaller.org

https://sass-lang.com/install

termianl(MAC):  brew install sass/sass/sass

sass --version

Ejemplo

::

crear carpeta css
    archivo estilos.css
crear carpeta sass
    archivo scss
terminal

enlazar carpetas-> sass --watch sass:css
y crea en css estilos.map para parar terminal ctl + c

* tambien agrega archivos a css si se crean en scss


tradicional vs sass

footer {
    background: red;
}
footer h4 {
    color: yellow;
}

footer h4 a {
    color: green;
}
----------
footer {
    background: tomato;
    h4 {
        color: yellow;
        a {
            color: green;
        }
    }
}

Variables 
---------
$colorUno: cadetblue; 
$colorDos: teal; 
$colorTres: darkgreen;

section {
  background: cadetblue;
}
section h1 {
  background: darkgreen;
}
section h2 {
  background: cadetblue;
}
section p {
  background: maroon;
}


Organizacion
--------------
Crear archivos en la carpeta scss
ejemplo
_variables.scss

y se tiene que inportar al archivo en el que se ocupa como:
@import "vatiables";


Mixin
---------
Es como una funcion;
Se agrega el mixin:
@mixin cuadrado {
    background: #444;
    width: 200px;
    height: 200px;
    margin-top: 5px;
    padding: 10px;
}

Se manda a llamar el mixin:

.cuadrado-1 {
    @include cuadrado;
}

Parametros

@mixin cuadrado ($fondo) {
    background: $fondo;
}

.cuadrado-1 {
    @include cuadrado(#666);
}

---
@mixin cuadrado($fondo, $ancho:200px) {
    background: $fondo;
    width: $ancho;
}

.cuadrado-1 {
    @include cuadrado(#333, 500px);
}
.cuadrado-2 {
    @include cuadrado(#555);
}
