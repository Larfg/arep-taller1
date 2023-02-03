# Taller 1: Aplicaciones Distribuidas (HTTP, Sockets, HTML, JS,MAVEN, GIT) 

## Diseño y descripción del diseño: 
Para este taller se realizaron distintas aplicaciones distribuidas con el objetivo de crear un servicio de consumo de un api de consulta de películas. 
en donde tenemos una aplicación fachada que nos consume el api y la expone a través de un web socket. 
Para el uso de este web socket programamos dos aplicaciones, una aplicación en JavaScript la cual nos da un cliente web en donde podemos colocar el titulo de la película que deseemos consultar y obtendremos un resultado, y otra aplicación en java la cual nos permite consultar una cantidad arbitraria de películas y probar el funcionamiento del servidor fachada. 
Para la realización de estas aplicaciones se tienen en cuenta los siguientes criterios. 

### Extensibilidad 
Para asegurar la extensibilidad se utilizaron clases claras en donde simplemente podremos agregar mas métodos o realizar herencias y polimorfismos para modificar el comportamiento o extenderlo de la manera que se requiera. 

### Uso de patrones 
Utilizamos un patrón **FACADE** que nos permite simplificar el consumo del api y se uso un **PROXY** para tener un cache y controlar el flujo hacia el api, evitando hacer consultas cuando ya se han realizado. 

### Modularidad 
Al tener las aplicaciones distribuidas, podemos cambiar cualquiera de los elementos y estos tiene poca cohesión o ninguna cohesión entre los elementos (módulos), por ejemplo podemos cambiar el cliente web por otro cliente, igual con el servidor de pruebas, también podríamos cambiar la api que se consume. 

## Componentes del taller: 
- Servidor https://github.com/Larfg/arep-taller1-wbserver 
- Cliente web https://github.com/Larfg/arep-taller1-JsWsClient 
- Servidor prueba https://github.com/Larfg/arep-taller1-testserver 

## Prerrequisitos: 
Debe tener java, Maven y un navegador web, preferiblemente Firefox.

## Instalación: 
Clone los tres repositorios listados en componentes del taller.

## Realizando pruebas: 
Para probar el funcionamiento del servidor creamos un servidor de pruebas dedicado en donde 
el servidor de prueba acepta un input para la cantidad de consultas que desee probar. 
  
## Despliegue: 
- Para poder iniciar el servidor y el servidor de prueba se puede iniciar por Maven, con el siguiente comando "mvn compile exec:java" o puede iniciarlo directamente con la clase ejecutiva de cada proyecto. 
- Para probar el cliente web descargue el repositorio y abra el .HTML, ahí podrá realizar la consulta correspondiente 
  
## Construido con: 
[Maven](https://maven.apache.org/) - Dependency Management   

## Autores: 
- Luis Felipe Andres Giraldo Rodriguez 
