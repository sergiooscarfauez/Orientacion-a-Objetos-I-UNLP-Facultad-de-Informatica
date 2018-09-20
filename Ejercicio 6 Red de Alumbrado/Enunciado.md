Ejercicio 6: Red de Alumbrado

Imagine una red de alumbrado donde cada farola está conectada a una o varias vecinas formando un grafo conexo1. Cada una de las farolas tiene un interruptor. Es suficiente con encender o apagar una farola cualquiera para que se enciendan o apaguen todas las demás. Sin embargo, si se intenta apagar una farola apagada (o si se intenta encender una farola encendida) no habrá ningún efecto, ya que no se propagará esta acción hacia las vecinas.
La funcionalidad a proveer permite:
1. crear farolas (inicialmente están apagadas)
2. conectar farolas a tantas vecinas como uno quiera (las conexiones son bi-direccionales) 
3. encender una farola (y obtener el efecto antes descrito)
4. apagar una farola (y obtener el efecto antes descrito)

Tareas:

1. Realice el diagrama UML de clases de la solución al problema. 
2. Implemente en Pharo, la clase Farola, como subclase de Object, con los siguientes métodos:

#initialize
"Inicializa a la farola como apagada"

#pairWithNeighbor: otraFarola
"Crea la relación de vecinos entre las farolas. La relación de vecinos entre las farolas es recíproca, es decir el receptor del mensaje será vecino de otraFarola, al igual que otraFarola también se convertirá en vecina del receptor del mensaje."

#turnOn
"Si la farola no está encendida, la enciende y propaga la acción."

#turnOff
"Si la farola no está apagada, la apaga y propaga la acción."

#isOn
"Retorna true si la farola está encendida."
3. Utilice los tests provistos por la cátedra para probar las implementaciones del punto 3.
Para instalar los tests, evalúe la siguiente expresión:

     (IceRepositoryCreator new
      	url: 'https://bitbucket.org/lifia-oop/practicas-objetos-1.git';
  	    createRepository) updatePackage: 'Objetos1-FarolasSkeleton'.
