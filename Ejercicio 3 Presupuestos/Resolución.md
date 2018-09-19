**Ejercicio 3: Presupuesto**

Importar en Pharo el archivo Objetos1-Presupuesto.st, dicha implementación pasa todos los test.

Clase Item:

    Object subclass: #Item
        instanceVariableNames: 'costoUnitario item costo cantidad'
	classVariableNames: ''
	poolDictionaries: ''
    	category: 'Objetos1-Presupuesto'

-----------------------------------------------------------------------------------------

Métodos de la Clase Item:

-----------------------------------------------------------------------------------------
(accessing)

    detalle: aString

    detalle := aString

-----------------------------------------------------------------------------------------

    cantidad

    ^cantidad

-----------------------------------------------------------------------------------------

    costo

    ^costoUnitario * cantidad

-----------------------------------------------------------------------------------------

    costoUnitario: aReal

    costoUnitario := aReal
    
-----------------------------------------------------------------------------------------

    cantidad: aInteger

    cantidad := aInteger

-----------------------------------------------------------------------------------------

    detalle

    ^detalle

-----------------------------------------------------------------------------------------

    costoUnitario

    ^costoUnitario

====================================================================================

Clase Presupuesto:

    Object subclass: #Presupuesto
     	instanceVariableNames: 'agregarItem calcularTotal items cantidad cliente fecha detalle costo'
	classVariableNames: ''
	poolDictionaries: ''
	category: 'Objetos1-Presupuesto'!

-----------------------------------------------------------------------------------------

Métodos de la Clase Presupuesto:

-----------------------------------------------------------------------------------------
(initialization)

    initialize

    items := OrderedCollection new.

-----------------------------------------------------------------------------------------

(accessing)

    fecha

    ^fecha

-----------------------------------------------------------------------------------------

    cantidadDeProductos: cantidad

    ^items select: [ :item | item cantidad > cantidad ]

-----------------------------------------------------------------------------------------

    calcularTotal

    ^items inject: 0 into: [ :total :item | total + item costo ]

-----------------------------------------------------------------------------------------

    cliente

    ^cliente

-----------------------------------------------------------------------------------------

    agregarItem: item

    items add: item.

-----------------------------------------------------------------------------------------

    cliente: aString

    cliente := aString

-----------------------------------------------------------------------------------------

    fecha: aString

    fecha := DateAndTime now



