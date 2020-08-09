# Maven_Basics
En este repositorio se exploran algunas caracteristicas de maven.

## Create a maven repository
  ![Creando proyecto](/Imagenes/Screenshot%20from%202020-08-08%2013-29-40.png)
  
  * La opcion "B" se usa para que maven corra en non-interactive mode lo cual hace que los logs sean mas faciles de leer.
  * La opcion "D" es una de las opciones mas usadas ya que se usa para definir propiedades del proyecto.
  * Las propiedad artifactId  identifica archivos del proyecto el cual es combinado con groupId identifican que un archivo (artifact) es parte cierto proyecto (group)
  * Dentro del directorio se crearon otros 2 en uno se guardara el codigo del cliente y en el otro las pruebas del proyecto, tambien se encuentra un archivo lamado POM.xml que basicamente describe el proyecto.
  
 ## POM.xml
  
  El POM (Project Object Model) contiene configuraciones,dependencias, version entre otras cosas necesarias para que maven pueda construir y compilar el proyecto.
  
  * SNAPSHOT es la version del proyecto en la linea de desarrollo y siempre sera mayor a la ultima version lanzada.
  * La etiqueta 'packaging' define como se empaquetara el proyecto si no se define una el defecto es '.jar'.
  * La etiqueta 'Dependencies' descargara otros proyectos de los que dependa el proyecto creado, dado el caso de que los proyectos descargados tambien neseciten de otros proyectos maven tambien se encargara de descargarlos.
 ## Dependency Management
  En el repositorio se puede ver que se copio la clase fileSpy que revisa un directorio hasta que un archivo es creado con .text.xsv y en la imagen se evidencia que se  modifico el POM para incluir el plugin y la libreria Tika.
  
  [tika+plugin](/Imagenes/Screenshot%20from%202020-08-09%2015-42-50.png)
  
 ## Lifecycles and Plugins
 ### lifecycles
 * Clean -> Limpia todos los archivos creados de la version anterior del proyecto.
 * Default -> Es el principal ciclo de vida y es el responsable de la version de depliegue.
 * Site -> Creacion de la documentacion del proyecto. 
 
### Phases
 * Compile -> Compila el codigo del proyecto
  [compile](/Imagenes/Screenshot%20from%202020-08-09%2016-15-48.png)
 * Package -> Compila el codigo del proyecto entre un formato que se pueda distribuir (Empaqueta,jar,war, etc.).
  [compile](/Imagenes/Screenshot%20from%202020-08-09%2016-21-11.png)
 * Install -> Instala el proyecto en un repositorio local.
  [compile](/Imagenes/Screenshot%20from%202020-08-09%2016-21-27.png)
 * Another-maven-Project
  [compile](/Imagenes/Screenshot%20from%202020-08-09%2016-28-54.png)
 * Usando mvn exec:java -Dexec.mainClass="edu.eci.FileSpy"
  [compile](/Imagenes/Screenshot%20from%202020-08-09%2016-30-43.png)
