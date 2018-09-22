Ejercicio 4: Figuras y cuerpos

Figuras en 2D

Defina un nuevo paquete Objetos1-FigurasYCuerpos-Model
En taller de programación definió clases para representar figuras geométricas. Retomaremos ese ejercicio para implementarlo en Smalltalk (ahora vamos a trabajar con Cuadrados y Círculos).
El siguiente diagrama de clases documenta los mensajes que estos objetos deben entender. Decida usted qué variables de instancia son necesarias. Ambas clases son subclases de Object. Puede agregar mensajes adicionales si lo cree necesario.

Fórmulas y mensajes útiles:

Diámetro del círculo: radio * 2
Perímetro del círculo: π * diámetro
Área del círculo: π * radio 2
π se obtiene enviando el mensaje #pi a la clase Float (Float pi)
Para elevar un numero al cuadrado, le enviamos el mensaje #squared (8 squared)
Cuerpos en 3D
Ahora que tenemos Círculos y Cuadrados, podemos usarlos para construir cuerpos (en 3D) y calcular su volumen y área exterior. Vamos a pensar a un cilindro como "un cuerpo que tiene un círculo como su cara basal y que tiene una altura (vea la siguiente imágen)" .

Si reemplazamos la cara basal por un rectángulo, tendremos un prisma (una caja de zapatos).
El siguiente diagrama de clases documenta los mensajes que entiende un cuerpo. Decida usted qué variables de instancia son necesarias. Cuerpo es subclase de Object.

Fórmulas útiles:

La superficie exterior de un cuerpo es: 
2* area-cara-basal + perimetro-cara-basal * altura-del-cuerpo
El volumen de un cuerpo es: area-cara-basal * altura

Más info interesante: A la figura que da forma al cuerpo (el círculo o el cuadrado en nuestro caso) se le llama directriz. Y a la recta en la que se mueve se llama generatriz. En wikipedia (Cilindro)1 se puede aprender un poco mas al respecto.
Pruebas automatizadas
Evalúe la siguiente expresión en un Playground.

    (IceRepositoryCreator new
      	url: 'https://bitbucket.org/lifia-oop/practicas-objetos-1.git';
      	createRepository) updatePackage: 'Objetos1-FigurasYCuerposSkeleton'.

Esa expresión creará un paquete Objetos1-FigurasYCuerposSkeleton y descargará en el mismo las pruebas (tests) que su código deberá pasar. 

Siguiendo los ejemplos de ejercicios anteriores, ejecute las pruebas automatizadas provistas. Si algún test no pasa, consulte al ayudante. 

Discuta y reflexione

Discuta con el ayudante sus elecciones de variables de instancia y métodos adicionales. ¿Es necesario todo lo que definió?
