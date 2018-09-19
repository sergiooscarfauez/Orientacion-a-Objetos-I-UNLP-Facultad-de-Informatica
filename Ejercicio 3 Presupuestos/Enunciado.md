Ejercicio 3: Presupuestos
Defina un paquete Objetos1-Presupuesto-Model y dentro de él Implemente las clases que se observan en el siguiente diagrama. Ambas son subclases de Object. Preste atención a los siguientes aspectos:

¿Cuáles son las variables de instancias de cada clase?
¿Qué variables inicializa y cómo?

Probando su código: 
Evalúe la siguiente expresión en un Playground.

**(Insertar imagen de las clases)**

 (IceRepositoryCreator new
  	url: 'https://bitbucket.org/lifia-oop/practicas-objetos-1.git';
  	createRepository) updatePackage: 'Objetos1-PresupuestoSkeleton'.

Encontrará un paquete Objetos1-PresupuestoSkeleton. En el mismo existe un tag "Tests" en el que hay dos clases que implementan los tests que su implementación deberá pasar. 

Utilice los tests provistos para confirmar que su implementación ofrece la funcionalidad esperada. Siéntase libre de explorar las clases de test para intentar entender qué es lo que hacen.  

En un playground instancie un presupuesto y agregue dos items al mismo. Luego calcule el costo total del presupuesto.
