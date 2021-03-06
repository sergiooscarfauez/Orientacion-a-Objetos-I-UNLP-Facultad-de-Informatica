**Ejercicio 2: Balanza Electrónica**

Importar en Pharo el archivo Objetos1-BalanzaElectronica.st, dicha implementación pasa todos los test.

Clase Balanza:

    Object subclass: #Balanza
	instanceVariableNames: 'cantidadDeProductos precioTotal pesoTotal'
	classVariableNames: ''
	poolDictionaries: ''
	category: 'Objetos1-BalanzaElectronica'
  
****************************  
Métodos de la Clase Balanza:
****************************
(Accessing)

    agregarProducto: producto

	"Para agregar un producto sumo uno a la cantidadDeProductos que tengo, a precioTotal, le sumo al valor que tengo más
	precio del prodcuto, lo mismo con el pesoTotal, le sumo al valor que tengo el peso del producto."

	cantidadDeProductos := cantidadDeProductos +1.
	precioTotal := self precioTotal + producto precio.
	pesoTotal := self pesoTotal + producto peso.

------------------------------------------------------------------------------------

    emitirTicket

    "Creo la variable temporal ticket."

    | ticket |

    ticket := Ticket new.
    
    ticket pesoTotal: self pesoTotal.
    
    ticket precioTotal: self precioTotal.
    
    ticket cantidadDeProductos: self cantidadDeProductos.
    
    ticket impuesto.
    
    ticket fecha: Date today.
    
    "Devuelvo el ticket. Recordar: Es importante devolverlo una vez realizada las operaciones."
    
    ^ ticket.
    
------------------------------------------------------------------------------------

	ponerEnCero: producto

	"Recibo el producto, pongo en 0 el pesoTotal, el precioTotal y la cantidadDeProductos y lo devuelvo."

	pesoTotal := 0.
	precioTotal := 0.
	cantidadDeProductos := 0.
	^producto.

------------------------------------------------------------------------------------

	precioTotal: aReal

	"Setea el precioTotal"

	precioTotal := aReal.

------------------------------------------------------------------------------------

	pesoTotal

	"Retorna el pesoTotal"

	^pesoTotal

------------------------------------------------------------------------------------

	precioTotal

	"Retorna el precioTotal."

	^precioTotal

------------------------------------------------------------------------------------

	cantidadDeProductos: aInteger

	"Setea la cantidadDeProductos."

	cantidadDeProductos := aInteger.

------------------------------------------------------------------------------------

	pesoTotal: aReal

	"Setea el pesoTotal."

	pesoTotal := aReal.

------------------------------------------------------------------------------------

	cantidadDeProductos

	"Retorna la cantidadDeProductos"

	^cantidadDeProductos.

------------------------------------------------------------------------------------

(initialization)

	initialize

	"Realizo la inicialización poniendo en cero el pesoTotal, el precioTotal y la cantidadDeProductos."

	self 
	pesoTotal: 0;
	precioTotal: 0;
	cantidadDeProductos: 0.	
	
====================================================================================

Clase Producto:

	Object subclass: #Producto
		instanceVariableNames: 'peso precioPorKilo descripcion precio'
		classVariableNames: ''
		poolDictionaries: ''
		category: 'Objetos1-BalanzaElectronica'
  
*****************************  
Métodos de la Clase Producto:
*****************************
(Accessing)
	
	peso: aInteger

	"Setea el peso."

	peso := aInteger

------------------------------------------------------------------------------------

	precioPorKilo: aInteger

	"Setea el precioPorKilo."

	precioPorKilo := aInteger

------------------------------------------------------------------------------------

	descripcion: aString

	"Setea la descripción"

	descripcion := aString

------------------------------------------------------------------------------------

	precio

	"Retorna el precio. ¿Cuál es el precio de un producto? El precio de un producto es el valor que obtenemos luego de
	multiplicar su peso por el precioPorKilo. Ejemplo: El precio de un kilogramo de avellanas es de cien pesos, y tengo
	un paquete con tres kilos de avellanas, entonces el precio del paquete es de trescientos pesos. No es necesario crear una 
	variable temploral solamente devuelvo el valor que resulta de esta sencilla cuenta."

	^peso * precioPorKilo.

------------------------------------------------------------------------------------

	precioPorKilo

	"Retorno el precioPorKilo."

	^precioPorKilo

------------------------------------------------------------------------------------

	peso

	"Retorno el peso."

	^peso

------------------------------------------------------------------------------------

	descripcion

	"Retorno la descripción."

	^descripcion

====================================================================================

Clase Ticket:

	Object subclass: #Ticket
		instanceVariableNames: 'precioTotal impuesto cantidadDeProductos pesoTotal fecha'
		classVariableNames: ''
		poolDictionaries: ''
		category: 'Objetos1-BalanzaElectronica'
  
***************************
Métodos de la Clase Ticket:
***************************
(Accessing)

	fecha 

	"Retorno la fecha."

	^fecha

------------------------------------------------------------------------------------

	precioTotal: aReal

	"Retorno el precioTotal."

	precioTotal := aReal.

------------------------------------------------------------------------------------

	pesoTotal

	"Retorno el pesoTotal."

	^pesoTotal

------------------------------------------------------------------------------------

	impuesto

	"Retorno el precio del impuesto que obtengo una vez que calculo el precio total por 0.21.
	Ejemplo: Un producto tiene un precio de cien pesos, ¿cuál es el impuesto que le corresponde?, siguiendo
	la cuenta escrita anteriormente, tenemos que calcular 100 * 0.21 = 21 pesos, es decir el valor del
	impuesto devuelto sería 21. No es necesario crear una variable temploral solamente devuelvo el valor que 
	resulta de esta sencilla cuenta. Como es una sola línea de código no es necesario escribir el punto al final."

	    ^precioTotal  * 0.21
    
------------------------------------------------------------------------------------

	precioTotal

	"Retorno el precioTotal."

	^precioTotal

------------------------------------------------------------------------------------

	cantidadDeProductos: aInteger

	"Setea la cantidadDeProductos."

	cantidadDeProductos := aInteger.

------------------------------------------------------------------------------------

	pesoTotal: aReal

	"Setea el pesoTotal."

	pesoTotal := aReal.

------------------------------------------------------------------------------------

	impuesto: aDouble

	"Setea el impuesto."

	impuesto := aDouble

------------------------------------------------------------------------------------

	fecha: aString

	"Setea la fecha."

	fecha := aString

------------------------------------------------------------------------------------

	cantidadDeProductos

	"Retorno la cantidadDeProductos."

	^cantidadDeProductos

