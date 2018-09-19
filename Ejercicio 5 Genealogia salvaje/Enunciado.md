Ejercicio 5: Genealogía salvaje

En una reserva de vida salvaje (como la estación de cría ECAS, en el camino Centenario), los cuidadores quieren llevar registro detallado de los animales que cuidan y sus familias. Para ello nos han pedido ayuda. Debemos: 

a) Modelar en objetos y programar en Pharo la clase Mamífero (como subclase de Object). El siguiente diagrama de clases (incompleto) nos da una idea de los mensaje que un mamífero entiende. Deje #tieneAncestro para el final y discuta su solución con el ayudante. 

**(Imagen)**

b) En un playground, instancie los objetos que se aprecian en el siguiente diagrama. Todos son de la misma especie, "Panthera leo". 
Utilice el inspector para confirmar que lo que instanció es lo que se pide. 
En el diagrama se puede apreciar el nombre/identificador de cada uno de ellos (por ejemplo Nala, Mufasa, Alexa, etc). 
Para crear una fecha, envíe a la clase Date el mensaje #newDay:month:year: - Solo preste atención a que las fechas de nacimiento sean anteriores a las de sus crías.
 
**(Imagen)**

c) Complete el diagrama de clases para reflejar los atributos y relaciones requeridos. 
d) Evalúe la siguiente expresión para instalar casos de prueba que hemos preparado para usted. Luego ejecute los tests como lo hizo en ejercicios anteriores. Si alguno falla, consulte con el ayudante. 
 
     (IceRepositoryCreator new
      	url: 'https://bitbucket.org/lifia-oop/practicas-objetos-1.git';
      	createRepository) updatePackage: 'Objetos1-GenealogiaAnimalSkeleton'.
