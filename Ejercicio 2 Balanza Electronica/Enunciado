Ejercicio 2: Balanza Electrónica

En taller de programación programó (en Java) una balanza electrónica. Volveremos a programarla, ahora en Smalltalk, con algún requerimiento adicional. 
En términos generales, la Balanza electrónica recibe productos (uno a uno), y calcula dos totales: peso total y precio total. La balanza no guarda los productos. Luego emite un ticket que indica número de productos considerados, peso total, precio total. 
Implemente:
Cree un nuevo paquete Objetos1-BalanzaElectronica. 
En ese paquete programe las clases que se muestran a continuación. 

Observe que no se documentan en el diagrama los mensajes que nos permiten obtener y establecer los atributos de los objetos (accessors). Aunque no los incluimos, verá que los tests fallan si no los implementa. Consulte con el ayudante para identificar, a partir de los tests que fallan, cuales son los accessors necesarios (pista: todos menos los setters de balanza). 
Al programarlas en Pharo, todas son subclases de Object.
Probando su implementación:
Evalúe la siguiente expresión en un Playground.

 (IceRepositoryCreator new
  	url: 'https://bitbucket.org/lifia-oop/practicas-objetos-1.git';
  	createRepository) updatePackage: 'Objetos1-BalanzaElectronicaSkeleton'.

Esa expresión creará un paquete Objetos1-BalanzaElectronicaSkeleton y descargará en el mismo las pruebas (tests) que su código deberá pasar. 
Si todo salió bien, su implementación debería pasar las pruebas que definen las clases que estan el el tag "Tests" del paquete que instaló al principio de este ejercicio. El propósito de estas clases es ejercitar una instancia de la clase Balanza y verificar que se comporta correctamente. 

   En la figura se observa el detalle de las clases de prueba. Para ejecutar los tests simplemente haga click sobre la burbuja que se encuentra a la derecha del nombre de cada clase. Si la burbuja es de color gris, significa que el test no ha sido ejecutado todavía. Si es rojo significa que hubo errores. Si es amarillo significa que los resultados no son los esperados. Si es verde, su código ha pasado el test. . Siéntase libre de investigar la implementación de estas clases.
Interactuando directamente con los objetos
Las siguientes expresiones muestran cómo hacer pruebas en un Playground. Esto es útil cuando se quiere entender cómo funciona algún objeto o se quiere experimentar. Para probar que los objetos funcionan bien usamos los tests (que ya aprenderemos a escribir)

balanza := Balanza new.
producto := Producto new.
producto descripcion: 'Crema'.
producto precioPorKilo: 43.
producto peso: 0.25.
balanza agregarProducto: producto.
producto := Producto new.
producto descripcion: 'Queso'.
producto precioPorKilo: 10.
producto peso: 2.
balanza agregarProducto: producto.
balanza emitirTicket.

La interfaz gráfica de la balanza
Para darle una idea de como una interfaz gráfica trabajaría con esos objetos, se ofrece una implementación ejemplo (que se descargó junto con los tests. Si su implementación pasó los tests, puede utilizar la siguiente expresión para comenzar a la interfaz.

interfaz := BalanzaComposableModel new.
interfaz balanza: Balanza new.
interfaz openWithSpec

