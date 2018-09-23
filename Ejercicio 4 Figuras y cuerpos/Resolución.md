**Ejercicio 4: Figuras y cuerpos**

Importar en Pharo el archivo Objetos1-FigurasYCuerpos.st, dicha implementación pasa todos los test.

Clase Circulo

    Object subclass: #Circulo
	    instanceVariableNames: 'radio'
	    classVariableNames: ''
	    poolDictionaries: ''
	    category: 'Objetos1-FigurasYCuerpos'

---------------------------------------------------------------------------------

Métodos de la Clase Item:

---------------------------------------------------------------------------------
(accessing)

    perimetro

    "La fórmula matemática del perímetro de un círculo es: π * diámetro.
    Con self diametro se nos devuelve el diametro del perímetro (self es perímetro en este caso al que le enviamos el mensaje diametro) y lo multiplicamos por pi que es la respuesta de enviar el mensaje pi a la clase Float.
    Recordar la precedencia de los mensajes en Smalltalk, primero los mensajes unarios, luegos los binarios y por último los keyword. Y que los mensajes son evaluados de izquierda a derecha.
    
    En esta resolución los mensajes unarios son:
    Float pi
    self diametro
    
    Y el mensaje binario esta compuesto por el selector * y el argumento ("Los mensajes binarios son mensajes que requieren exactamente un argumento y cuyo selector consiste en una secuencia de uno o más caracteres del conjunto: +,-,*,/,&,=,>,|,<,∼, y @. Pharo por Ejemplo."
    
    Finalmente, hay que notar que ^ va a retornar el resultado, que es un objeto, de haber realizado todas las operaciones anteriores.)
    
    ^Float pi * self diametro
 
-------------------------------------------------------------------------------------------

    diametro

    "La fórmula matemática del diametro de un círculo es: 2 * radio.
    En este caso también es un mensaje binario, cuyo resultado devolvemos con ^."
    
    ^2 * radio
    
-------------------------------------------------------------------------------------------

    radio

    "Devuelvo el radio.".
    
    ^radio

-------------------------------------------------------------------------------------------

    radio: aDouble

    radio := aDouble

-------------------------------------------------------------------------------------------

    area
    
    "La fórmula matematica del area es: π * radio²."
    
    ^Float pi * radio squared
