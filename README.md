# Programa Radia

Este documento forma parte de un proyecto de voluntariado, del programa Radia.

https://www.radia.university/

# Introduccion a Flask Python Microframework

El objetivo de esta formación es conocer de forma introductoria como se estructura una aplicación web, que ventajas e inconvenientes nos aporta un framework o microframework y ver algunos ejemplos con Flask y Python, centrándonos en la parte backend de la aplicación web.

## Estructura de una aplicación web.

Las aplicaciones web se desarrollan siguiendo la arquitectura cliente / servidor donde el cliente realiza peticiones al servidor, quien le da respuesta.

![Representación arquitectura cliente servidor](/img/client-server.jpg)

Tradicionalmente (  anterior a 2010 ) cuando desarrollabamos una aplicación web no separabamos los lenguajes de servidor como php o python de lenguages de cliente como html, css, etc. Surgiendo problemas de múltiple índole como la escalabilidad o la mantenibilidad al tener "código espagueti".

Para solucionar estos problemas se comienzan a utilizar patrones de diseño como MVC, donde tenemos tres niveles de abstracción: Modelo, Vista y Controlador.

![Representación arquitectura cliente servidor](/img/mvc-modelo-vista-controlador.png)

## Desarrollo mediante Frameworks

Los frameworks más populares open source nos proponen la forma de estructurar nuestro proyecto utilizando varios patrones de diseño como: MVC, Fachada, Singleton, Factory, Decorator, Inyección de dependencias. 

![Patrones de diseño](/img/gof.png)

Mediante la documentación del framework se indica como utilizar el framework para resolver los problemas más comunes: como estructurar nuestros proyectos, como integrar librerias, como crear modulos o servicios, manejar errores, etc.
Siguiendo las bases que indica el framework será más fácil escalar nuestra aplicación web, ya que otros desarrolladores podrán conocer el framework y evolucionar el desarrollo.

## Frameworks vs Microframeworks

De forma general los microframeworks, se enfocan el manejo de solicitudes HTTP. Están centrados en el Kernel, core del framework con todo lo necesario para su funcionamiento.
Middleware: capa que nos va a permitir añadir funciones a nivel de aplicación, routing, control de errores, etc. Routing: capa para manejar el protocolo HTTP, el viaje de la petición hasta la respuesta.

![Ejemplos frameworks y microframeworks en varios lenguajes](/img/microvsframeworks.png)

Frameworks (full-stack), además de lo anterior suelen incorporar el manejo de más funcionalidades: como la autenticación, base de datos, validación, cache, motor de plantillas, etc.

## Ventajas del uso de frameworks en ciberseguridad

Los frameworks opensource con gran comunidad, al ser de código abierto, aportan mayor seguridad, las posibles vulnerabilidades cuando sean descubiertas serán corregidas por los desarrolladores que mantienen el framework.

La otra ventaja, es la integración de la capa de manejo de datos que incorporan ( ORM, DBAL) que nos evitan ataques sql injection.

![sql injection](/img/injection.png)

## Code review

Analizemos dos proyectos de ejemplo:

https://github.com/ardinusawan/Flask-VueJS-CRUD-Sample

https://github.com/briancappello/flask-unchained

