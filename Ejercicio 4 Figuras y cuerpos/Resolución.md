**Ejercicio 4: Figuras y cuerpos**

Importar en Pharo el archivo Objetos1-FigurasYCuerpos.st, dicha implementación pasa todos los test.

Clase Circulo

    Object subclass: #Circulo
	    instanceVariableNames: 'radio'
	    classVariableNames: ''
	    poolDictionaries: ''
	    category: 'Objetos1-FigurasYCuerpos'!

---------------------------------------------------------------------------------

Métodos de la Clase Item:

---------------------------------------------------------------------------------
(accessing)

    perimetro

    "La fórmula matemática del perímetro de un círculo es: π * diámetro.
    Con self diametro se nos devuelve el diametro del perímetro (self es perímetro en este caso al que le enviamos el mensaje diametro) y lo multiplicamos por pi que es la respuesta de enviar el mensaje pi a la clase Float."
    
    ^Float pi * self diametro
    
(escribiendo)...
