Ejercicio 1: WallPost

Primera parte

Se está construyendo una red social como Facebook o twitter. Definimos una clase Wallpost con los siguientes atributos: un texto que se desea publicar, cantidad de likes (“me gusta”) y una marca que indica si es destacado o no. La clase Wallpost es subclase de Object.
Cree un nuevo paquete Objetos1-Wallpost-Model

Dentro de ese paquete defina la clase Wallpost en Smalltalk, para que entienda los siguientes mensajes:
#text 
"Retorna el texto descriptivo de la publicación"
#text: descriptionText 
"Setea el texto descriptivo de la publicación"
#likes 
"Retorna la cantidad de “me gusta”"
#like 
"Incrementa la cantidad de likes en uno"
#dislike 
"Decrementa la cantidad de likes en uno. Si ya es 0, no hace nada"
#isFeatured 
"Retorna true si el post está marcado como destacado, false en caso contrario"
#toggleFeatured 
"Cambia el post del estado destacado a no destacado y viceversa"
#initialize 
"Inicializa el estado de las variables de instancia del Wallpost. Luego de la invocación el Wallpost debe tener como texto: “Undefined post”, no debe estar marcado como destacado y la cantidad de “Me gusta” deben ser 0."

Segunda parte

Evalúe la siguiente expresión en un Playground.

    (IceRepositoryCreator new
      	url: 'https://bitbucket.org/lifia-oop/practicas-objetos-1.git';
      	createRepository) updatePackage: 'Objetos1-WallpostSkeleton'.

Esa expresión creará un paquete Objetos1-WallpostSkeleton y descargará en el mismo las pruebas (tests) que utilizaremos para verificar el código que ha escrito. 
Utilice los tests provistos por la cátedra para comprobar que su implementación de Wallpost es correcta. En la siguiente figura se observa el detalle de las clase de pruebas WallpostTest. Para ejecutar los tests simplemente haga click sobre la burbuja que se encuentra a la derecha del nombre de la clase. Si la burbuja es de color gris, significa que el test no ha sido ejecutado todavía. Si es rojo significa que hubo errores. Si es amarillo significa que los resultados no son los esperados. Si es verde, su código ha pasado el test.  Siéntase libre de investigar la implementación de la clase de test. Ya veremos en detalle cómo implementarlas. 

![Diagrama de Clases](https://github.com/sergiooscarfauez/Orientacion-a-Objetos-I-UNLP-Facultad-de-Informatica/blob/master/Ejercicio%201%20WallPost/Imagenes/1.png?raw=true)

Tercera parte

Una vez que su implementación pasa los tests de la primera parte puede utilizar la ventana que se muestra a continuación, la cual permite inspeccionar y manipular el post (definir su texto, hacer like y dislike, marcarlo como destacado).

![Ventana](https://github.com/sergiooscarfauez/Orientacion-a-Objetos-I-UNLP-Facultad-de-Informatica/blob/master/Ejercicio%201%20WallPost/Imagenes/2.png?raw=true)

Para abrir la ventana puede evaluar la siguiente expresión en el Playground:
WallpostUI on: (Wallpost new)

En la expresión que evaluó para abrir la ventana WallpostUI on: (Wallpost new) se instancian 2 objetos, el wallpost y la ventana. Discuta con un ayudante:
¿En qué difieren las instanciaciones?
En la primer parte de este ejercicio ud. implementó el método #initialize, pero, ¿quien lo invoca? 
Ayuda: coloque un breakpoint en el método initialize para ver quién lo invoca. 
Ayuda de la ayuda: para poner un breakpoint agregue la sentencia self halt. al código del método #initialize.
