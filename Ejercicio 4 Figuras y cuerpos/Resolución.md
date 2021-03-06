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
    
==================================================================================================

Clase Cuadrado


    Object subclass: #Cuadrado
    	    instanceVariableNames: 'lado perimetro area'
	    classVariableNames: ''
	    poolDictionaries: ''
	    category: 'Objetos1-FigurasYCuerpos'

---------------------------------------------------------------------------------

Métodos de la Clase Cuadrado:

---------------------------------------------------------------------------------
(accessing)

    perimetro: aDouble

    perimetro := aDouble
    
---------------------------------------------------------------------------------

    lado

    ^lado

---------------------------------------------------------------------------------

    area: aDouble

    area := aDouble

---------------------------------------------------------------------------------

    perimetro

    "La fórmula matemática del perimetro de un cuadrado es lado * 4 , que es cuatro veces la longitud del lado.
    En este caso es un mensaje binario, cuyo resultado devolvemos con ^."
    
    ^4 * lado

---------------------------------------------------------------------------------

    area

    "La fórmula matemática del area de un cuadrado es lado². En este caso es un mensaje unario, cuyo resultado
    devolvemos con ^."
    
    ^lado squared

---------------------------------------------------------------------------------

    lado: aDouble

    lado := aDouble

==================================================================================================

---------------------------------------------------------------------------------

Métodos de la Clase Cuerpo:

---------------------------------------------------------------------------------
(accessing)

    Object subclass: #Cuerpo
	    instanceVariableNames: 'altura volumen caraBasal areaExterior cuerpo superficieExterior'
	    classVariableNames: ''
	    poolDictionaries: ''
	    category: 'Objetos1-FigurasYCuerpos'

---------------------------------------------------------------------------------

    altura

    ^altura

---------------------------------------------------------------------------------

    superficieExterior

    "La fórmula matematica de la superficie exterior de un cuerpo es: 2 * area de la cara basal + perimetro de la cara basal * altura del cuerpo.
    Nota: Es importante agregar los paréntisis para modificar el orden en que se envían los mensajes, puesto que los 
    mensajes que estan encerrados entre paréntesis se envían primero. Finalmente devolvemos el resultado con ^."
    
    ^(caraBasal area * 2) + ((caraBasal perimetro) * altura)

---------------------------------------------------------------------------------

    caraBasal

    ^caraBasal
    
---------------------------------------------------------------------------------

    superficieExterior: aDouble

    superficieExterior := aDouble

---------------------------------------------------------------------------------

    caraBasal: aDouble

    caraBasal := aDouble

---------------------------------------------------------------------------------

    volumen

    "La fórmula matematica del volumen de un cuerpo es: area de la cara basal * altura.
    Recordar la precedencia de los mensajes en Smalltalk, primero los mensajes unarios, luegos los binarios y por último los keyword. Y que los mensajes son evaluados de izquierda a derecha.
    
    Primero se envia el mensaje unario area a caraBasal y luego se resuelve el mensaje binario multiplicando la altura por el resultado del envío del mensaje unario anterior. Finalmente devolvemos el resultado con ^."
    
    ^caraBasal area * altura

---------------------------------------------------------------------------------

    volumen: aDouble

    volumen := aDouble

---------------------------------------------------------------------------------

    altura: aDouble

    altura := aDouble
