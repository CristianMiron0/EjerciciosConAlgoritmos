# 						**Ejercicios con algoritmos**



## 	**Ejercicio 1**

*Calcular la letra del DNI Espanol*

__Paso 1__: Definir el problema

A partir de un numero de DNI hemos de calcular la letra.

​	Como se calcula la letra del DNI?

​	Numero de DNI debe tener 8 digitos, este DNI hay que dividirlo en 23 y el resto sera el resultadoResto.

​	El valor contenido en```resultadoResto``` lo compararemos con la lista de codigos de la siguente tabl de letras ```tablaLetrasDNI```

| numero | letra |
| --------- | ----- |
| 0         | T     |
| 1         | R     |
| 2         | W     |
| 3         | A     |
| 4         | G     |
| 5         | M     |
| 6         | Y     |
| 7         | F     |
| 8         | P     |
| 9         | D     |
| 10        | X     |
| 11        | B     |
| 12        | N     |
| 13        | J     |
| 14        | Z     |
| 15        | S     |
| 16        | Q     |
| 17        | V     |
| 18        | H     |
| 19        | L     |
| 20        | C     |
| 21        | K     |
| 22        | E     |

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada: ```DNI```, ```tablaLetrasDni```, ```resultado```

Proceso: 

- Validar que el ```DNI``` tenga 8 digitos, y que sen todos numericos
  - Si es erronea asigne a la variable ```resultado``` "DNI Invalido"

- Dividimos ```DNI``` en 23 y el resto lo asignamos a ```resultadoResto```
- Comparar el ```resultadoResto``` con los valores de la tabla ```tablaLetrasDNI``` y asignar a ```resultado``` el valor equivalente en la tabla.

Salida:

- Escribir ```resultado```

__Paso 3__: Escribir el pseudocodigo

``` Algoritmo CalculoDNI
Algoritmo CalculoDNI
	# Entrada
	DNI<-leer()
	tablaLetrasDNI<-"TRWAGMYFPDXBNJZSQVHLCKE"
	tablaLetrasDNI[0]<-T
	tablaLetrasDNI[1]<-R
	tablaLetrasDNI[2]<-W
	tablaLetrasDNI[3]<-A
	tablaLetrasDNI[4]<-G
	tablaLetrasDNI[5]<-M
	tablaLetrasDNI[6]<-Y
	tablaLetrasDNI[7]<-F
	tablaLetrasDNI[8]<-P
	tablaLetrasDNI[9]<-D
	tablaLetrasDNI[10]<-X
	tablaLetrasDNI[11]<-B
	tablaLetrasDNI[12]<-N
	tablaLetrasDNI[13]<-J
	tablaLetrasDNI[14]<-Z
	tablaLetrasDNI[15]<-S
	tablaLetrasDNI[16]<-Q
	tablaLetrasDNI[17]<-V
	tablaLetrasDNI[18]<-H
	tablaLetrasDNI[19]<-L
	tablaLetrasDNI[20]<-C
	tablaLetrasDNI[21]<-K
	tablaLetrasDNI[22]<-E
	resultado<-""
	# Proceso
	Si DNI menor o igual que 99999999 Entonces # 8 Digitos y que sean todos numericos
		 resultadoRest<-DNI mod 23 #mod es el resto de dividir
		 # resultado<-recuperarLetra apartir de la tablaLetrasDNI y resultadoResto
		# Para i<-0 Hasta 22 Con paso 1 Hacer
			# Si resultadoResto Igual i Entonces
				# resultado<-tablaLetrasDNI[i]
				# i<-23 #break
			# Fin si
		# Fin Para
			resultado<-tablaLetrasDNI[resultadoResto]
	Sino
		 resultado<-"DNI Invalido"	
	Fin Si
	# Salida
	Escribir(resultado)
Fin Algoritmo
```

## 	**Ejercicio 2**

*Calcular el salario de un empleado*

__Paso 1__: Definir el problema

​	El salario en Espana se calcula a partir del salario bruto anual, que ancluye todas las percepciones economicas que recibe un trabajador durante el ano, incluyendo salario base, paga extras, complementos y otros conceptos retributivos.

A partir del salario bruto se deducen las cotizaciones a la Seguridad Social y el Impuesto sobre la Renta de las Personas Fisicas (IRPF), que varian en funcion del nivel salarial y la situacion personal del trabajador.

El salario neto anual se obtiene restando al salario bruto anual las cotizaciones y el IRPF correspondiente. El resultado final es el salario que percibe el trabajador despues de impuestos y cotizaciones.

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada: ```salarioBase```, ```pagasExtras, complementos```, ```otrosConceptosRetributivos``` 

```IRP```, ```Seguridad Social```

Proceso: 

- Sumar ```salarioBase```, ```pagasExtras, complementos```, ```otrosConceptosRetributivos``` y asigno a ```salarioBruto```
- Sumar ```IRP```, ```Seguridad Social``` y lo asigno a ```deducciones```
- ```salarioNeto``` asigna ```salarioBruto``` - ```deducciones```

Salida:

Escribir (```salarioNeto```, ```salarioBruto```)

__Paso 3__: Escribir el pseudocodigo

```Algoritmo CalculoDNI
Algoritmo CalcularSalario
# Entrada
  ## Escribimos los valores necesarios de un salario
	  salarioBase<-Leer()
	  pagasExtras<-Leer()
	  complementos<-Leer()
	  otrosConceptosRetributivos<-Leer()
	  IRP<-Leer()
	  Seguridad Social<-Leer()
# Proceso
  ## Calculamos el salario usando las formulas
	  salarioBruto<-salarioBase+pagasExtras+complementos+otrosConceptosRetributivos
	  deducciones<-IRP+Seguridad Social
	  salarioNeto<-salarioBruto-deducciones
# Salida
  ## Recibimos resultado visual de los calculos
	  Escribir(salarioNeto,salarioBruto)
Fin Algoritmo
```

## 	**Ejercicio 3**

*Determinar la ruta para llegar a una ciudad por avion*

__Paso 1__: Definir el problema

​	Necesitamos crear un programa que calcule una ruta del punto a al punto b.

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada: ```camposDeOrigen```, ```destino```, ```direcciones```

Proceso: 

- Ingrese las coordenadas del punto A (latitud y longitud) 

- Ingrese las coordenadas del punto B (latitud y longitud) 

- Calcule la distancia entre el punto A y el punto B utilizando la fórmula de la distancia entre dos puntos en un plano cartesiano. ```formula```:
  $$
  d=√((x_2-x_1)²+(y_2-y_1)²)
  $$

-  Muestre al usuario la distancia y dirección entre el punto A y el punto B

Salida: Escribir ```direcciones```

__Paso 3__: Escribir el pseudocodigo

```Algoritmo CalculoDNI
Algoritmo CalculeRuta
# Entrada
  ## Escribimos coordenadas del punto A y del punto B 
 	  camposDeOrigen<-leer()
	   x1<-camposDeOrigen ["latitud"]
 	   x2<-camposDeOrigen ["longitud"]
 	  destino<-leer()
	   y1<-destino ["latitud"]
 	   y2<-destino ["longitud"]
# Proceso
  ## Calcular la distancia entre puncto A y puncto B utilizando la formula
 	  formula<-d=√((x_2-x_1)²+(y_2-y_1)²)
 	  direcciones<-formula
# Salida
  ## Muestre al usuario la distancia y dirección entre el punto A y el punto B ##
 	  Escribir(direcciones)
Fin Algoritmo
```

## 	**Ejercicio 4**

*Calcula el área y perímetro de un círculo dado su radio*

__Paso 1__: Definir el problema

​	Para calcular el area y el perímetro de un círculo dado su radio, podemos utilizar las siguientes fórmulas:

Área = π × r² 

Perímetro = 2 × π × r

Donde "r" es el radio del circulo y "π" (pi) es una constante matematica aproximada a 3.14159.

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada: ```area```, ```perimetro```, ```pi```, ```radioDelCirculo```

Proceso:

- Crea el valor estatico para pi (π) <- 3.14159

- Crear formula para el ```area```
- Crear formula para el ```perimetro```

Salida: Escribir resultado de formula para ```Area``` y ```Perimetro```

__Paso 3__: Escribir el pseudocodigo

```Algoritmo CalculoDNI
Algoritmo CalcularArea y CalcularPerimetro 
# Entrada
  ## Escribimos radio de un circulo
 	  radioDelCírculo<-Recuperar En Puncto Flotante(leer("Radio del circulo: "))
# Proceso
  ## Creamos el valor de pi y calculamos el area y el perimetro con las formulas
      pi<-3.14159
      area<-pi multiplicado por radioDelCirculo elevado a la 2
	  perimetro<-2 multiplicado por pi multiplicado por radioDelCirculo
# Salida
  ## Imprimimos el resultado del area del circulo y el perimetro
	  Escribir("Area:", area)
	  Escribir("Perimetro:", perimetro)
Fin Algoritmo
```

## 	**Ejercicio 5**

*Dada una lista de numeros enteros, determina cual es el mayor y cual es el menor*

__Paso 1__: Definir el problema

​	Es decir, los numeros enteros son aquellos números positivos y negativos, incluido el cero, que no tienen parte decimal dentro de su estructura (3,28, por ejemplo, no es un número entero).

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada: ```listaDeNumeros```, ```mayor```, ```menor```

Proceso:

- Seleccionamos una ```listaDeNumeros``` o escribir una nueva.
- Inicializamos dos variables: numero ```mayor``` y numero ```menor```, con el primer valor de la lista.
- Si encontramos un numero mayor que el valor actual de la variable del numero ```mayor```, actualizamos la variable.
- Si encontramos un numero menor que el valor actual de la variable del numero ```menor```, actualizamos la variable.

Salida: Al final del recorrido de la lista, escribir las variables del numero ```mayor``` y ```menor``` .

__Paso 3__: Escribir el pseudocodigo

```Algoritmo CalculoDNI
Algoritmo NumerosMayor y NumerosMenor
# Entrada
  ## Insertamos la lista y la aplicamos a nuestras categorias de mayor y menor
	  listaDeNumeros<-()
	  mayor<-listaDeNumeros()
	  menor<-listaDeNumeros()
# Proceso
  ## Separamos los numeros de la lista en listas mayor y menor
	  for numero in listaDeNumeros:
		if numero > mayor:
			mayor<-numero
	  	if numero < menor:
			menor<-numero
	   	End if
# Salida
  ## Recibimos resultado visual de la separacion de los numeros de la lista
	  print("Numero mayor:", mayor)
	  print("Numero menor:", menor)
Fin Algoritmo
```

## 	**Ejercicio 6**

*Crea un algoritmo que convierta grados Celsius a Fahrenheit*

__Paso 1__: Definir el problema

​	Creamos un código que cambia el valor de temperatura de celsius en fahrenheit.

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada: ```celsius```, ```fahrenheit```

Proceso:

- Leer el valor de la temperatura en grados Celsius
-  Convertir la temperatura de Celsius a Fahrenheit usando la fórmula: F = (C * 1.8) + 32 

Salida: Mostrar el resultado en grados ```fahrenheit```

__Paso 3__: Escribir el pseudocodigo

```Algoritmo CalculoDNI
Algoritmo Cambia TemperaturaCelsius en TemperaturaFahrenheit
# Entrada
  ## Escribimos temperatura celsius
	  celsius<-Recuperar En Puncto Flotante(input("Temperatura:"))
# Proceso
  ## Cambiamos el valor usando la formula
	  fahrenheit<-(celsius x 1.8) + 32
# Salida
  ## Recibimos el resultado del calculo
	  Escribir("La temperatura en Fahrenheit es:", fahrenheit)
Fin Algoritmo
```

## 	**Ejercicio 7**

*Dado un numero entero, crea un algoritmo que determine si es par o impar*

__Paso 1__: Definir el problema

​	Los números pares son aquéllos que pueden dividirse entre dos, y los impares los que no pueden dividirse entre dos. Es decir, los números pares corresponden a una cantidad que permite agruparse de dos en dos y los impares no.

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada: ```par```, ```impar```, ```numero```

Proceso: 

- Necesitas verificar si el residuo de dividir ese número por dos es cero. Si es cero, entonces el número es par, de lo contrario es impar.

Salida: Escribir el resultado "el numero es:" ```par``` o ```impar```

__Paso 3__: Escribir el pseudocodigo

```Algoritmo CalculoDNI
Algoritmo NumeroPar o NumeroImpar
# Entrada
  ## Esribimos el numero de determinar es para o impara
	  numero<-leer()
# Proceso
  ## Necesitamos verificar si el residuo de dividir ese número por dos es cero
	  If (numero % 2 = 0) then
	  	Print "El número es par"
	  Else
	  	Print "El número es impar"
	  End if
# Salida
  ## Recibimos el resultado del proceso
Fin Algoritmo
```

## 	**Ejercicio 8**

*Crea un algoritmo que determine si un año es bisiesto o no*

__Paso 1__: Definir el problema

​	Un año bisiesto es aquel que tiene 366 días, en lugar de 365 que tiene el resto de años. ¿Por qué cada 4 años tenemos año bisiesto? El motivo por el que cada cuatro años hay un año bisiesto es que la duración del año solar es de 365,25 días aproximadamente, no 365 días justos.

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada: ```anoBisiesto```, ```ano```, ```resultado```

Proceso: 

- Año divisible entre 4, 100 y 400. La regla establece que un año es bisiesto cuando se cumple cualquiera de las dos reglas siguientes: Que el año sea divisible entre 400. Que el año sea divisible entre 4 pero que no sea divisible entre 100.

Salida: Print el resultado

__Paso 3__: Escribir el pseudocodigo

```Algoritmo CalculoDNI
Algoritmo AñoBisiesto
# Entrada
  ## Escribimos el año que queremos probar
	  anoBisiesto:leer()
# Proceso
  ## Dividimos el año entre 4, 100 y 400
	  if anoBisiesto % 4 != 0:
		return resultado<-False
	  elif anoBisiesto % 100 != 0:
		return resultado<-True
	  elif anoBisiesto % 400 != 0:
		return resultado<-False
	  else:
		return resultado<-True
# Salida
  ## Recibimos del año es bisento con falso o verdadero
	  print(resultado)
Fin Algoritmo
```

## 	**Ejercicio 9**

*Crea un algoritmo que determine si una cadena de texto es un palindromo o no*

__Paso 1__: Definir el problema

Un palíndromo es una palabra, frase o secuencia de caracteres que se lee igual de izquierda a derecha y de derecha a izquierda. Un ejemplo común de un palíndromo es la palabra "reconocer".

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada: ```palindrome```, ```cadena```

Proceso: 

- Eliminamos los espacios en blanco de la cadena de testo y convertimos todo a minusculas para que la comparacion sea insensible a mayusculas y minusculas
- Comparamos la cadena de testo original con su version invertida
- Si la cadena original es igual a su version invertida, entonces el resultado es "Si es palindromo", indicando que la cadena de texto es un palindromo
- Caso contrario el resultado es "No es palindrome"

Salida: Imprimir el palindrome o no palindrome (resultado)

__Paso 3__: Escribir el pseudocodigo

```Algoritmo CalculoDNI
Algoritmo PalindromoPalabra
# Entrada
  ## Insertamos la palabra que sera probada
	  cadena<-leer()
# Proceso
  ## Comparamos la palabra con su espejo
	  cadena<-convertir a minusculas y eliminar espacios en blanco
	  reversa<-depuracionCadena
	  Si cadena es igual a reversa entonces
		resultado<-"La cadena es un palindromo"
	  Sino:
		resultado<-"La cadena no es un palindromo"
	  FinSi
# Salida
  ## Recibimos resultado visual del proceso
	  Escribir(resultado)
Fin Algoritmo
```

## 	**Ejercicio 10**

*Dada una lista de nombres, crea un algoritmo que ordene la lista alfabeticamente*

__Paso 1__: Definir el problema

Ordenar una lista en forma alfabeticamente.

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada: ```listaNombres```, ```j```, ```i```

Proceso: 

- Definimos una lista de ejemplo.
- Utilizamos un bucle `para` anidado para recorrer la lista y comparar los elementos adyacentes
- Si el elemento `j` es mayor que el elemento `j+1`, intercambiamos los elementos
- Repetimos los pasos 2 y 3 hasta que la lista este completamente ordenada
- Imprimimos la lista ordenada

Salida: Escribir lista ordenada

__Paso 3__: Escribir el pseudocodigo

```Algoritmo CalculoDNI
Algoritmo OrdenarLista
# Entrada
  ## Insertamos una lista para ordenar
listaNombres<-()
# Proceso
  ## Utilizamos el algoritmo de ordenamiento burbuja para ordenar la lista y Intercambiamos los elementos
	  Para i de 0 a longitud(listaNombres) - 1 hacer:
	  	Para j de 0 a longitud(listaNombres) - 1 - i hacer:
			Si listaNombres(j) > listaNombres(j+1) entonces:
				j y j+1 de la listaNombres
				temp<-listaNombres(j)
				listaNombres(j)<-listaNombres(j+1)
				listaNombres(j+1)<-temp
# Salida
  ## Imprimimos la lista ordenada
	Escribir(listaNombres)
Fin Algoritmo
```

## 	**Ejercicio 11**

*Crea un algoritmo que calcule el factorial de un numero entero*

__Paso 1__: Definir el problema

El factorial de un numero entero se define como el producto de todos los numeros enteros desde 1 hasta el numero en cuestión. Por ejemplo, el factorial de 5  es igual a 5 x 4 x 3 x 2 x 1, que es igual a 120.

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada: ```factorial```, ```numero```, 

Proceso:

- Definir una variable ```factorial``` con un valor inicial de 1
- Escribir un numero y guardarlo en una variable llamada ```numero```
- Empezar un bucle "para" que vaya desde 1 hasta ```numero``` 
- En cada iteracion del bucle, multiplicar ```factorial``` por el numero actual del bucle
- Despues imprimir el valor de ```factorial```

Salida: Escribir "El factorial de numero es "

__Paso 3__: Escribir el pseudocodigo

```
Algoritmo FactorialNumero
# Entrada
  ## Insertamos el número que queremos calcular
	  numero<-Recuperar Integer(leer("Numero entero: "))
	  factorial<-1
# Proceso
  ##  Crear un bucle y multiplicar factorial por el numero de bucle actual
	  Para i desde 1 hasta n hacer
    	factorial<-factorial x i
# Salida
  ## Recibimos el numero factorial del numero que insertamos
	  print("El factorial de", numero, "es", factorial)
Fin Algoritmo
```

## 	**Ejercicio 12**

*Dado un numero entero, crea un algoritmo que determine si es primo o no*

__Paso 1__: Definir el problema

Un numero primo es aquel que solo es divisible por 1 y por sí mismo.

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada: ```numero```, ```resultado```, ```i```, ```divisores```, ```raizCuadrada```

Proceso:

- Definimos el numero que queremos evaluar.
- Inicializamos un contador de divisores en 0
- Utilizamos un bucle `para` para recorrer todos los numeros entre 2 y la raiz cuadrada del numero, y comprobamos si el numero es divisible por cada uno de ellos. Si es asi, aumentamos el contador de divisores en 1
- Si el contador de divisores es mayor que 0, el numero no es primo, ya que tiene mas de un divisor ademas de 1 y el mismo. De lo contrario, el numero es primo
- Imprimimos un mensaje indicando si el numero es primo o no

Salida: Escribir "primo" o "no primo".

__Paso 3__: Escribir el pseudocodigo

```
Algoritmo NumeroPrimo
# Entrada
  ## Escribimos el numero y establecemos los demas valores
	  numero<-()
	  divisores<-1
# Proceso
  ## Utilizamos un bucle for para comprobar si el numero es divisible por algun numero entre 2 y la raiz cuadrada del numero
	  Para i de 2 a raizCuadrada(numero) hacer:
		Si numero % i<-0 entonces:
			divisores = divisores + 1
# Salida
  ## Si el nUmero tiene mas de 0 divisores, no es primo. De lo contrario, es primo
	  Si divisores > 0 entonces:
		Escribir<-"El número no es primo."
	  Sino:
		Escribir<-"El número es primo."
Fin Algoritmo
```

## 	**Ejercicio 13**

*Crea un algoritmo que calcule el area y volumen de un cubo dado su lado*

__Paso 1__: Definir el problema

El volumen de un cubo es igual a la medida de su lado al cubo.

Volumen = lado x lado x lado = lado3

Area total = 6 x lado x lado = 6 x 2lado

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada: ```lado```, ```area```, ```volumen```

Proceso:

- Escribir el lado del cubo
- Crear formula para el ```area```
- Crear formula para el ```volumen```

Salida: Escribir resultado para ```area``` y ```volumen```

__Paso 3__: Escribir el pseudocodigo

```
Algoritmo VolumeCubo y AreaCubo
# Entrada
  ## Escribimos el lado del cubo
	  lado<-Recuperar En Puncto Flotante(leer("lado del cubo: "))
# Proceso
  ## Calculamos area y volumen con las formulas
	  area<-6 x lado x lado
	  volumen<-lado x lado x lado
# Salida
  ## Obtenemos el resultado de las ecuaciones
	  print("Area del cubo:", area)
	  print("Volumen del cubo:", volumen)
Fin Algoritmo
```

## 	**Ejercicio 14**

*Dada una lista de numeros enteros, crea un algoritmo que calcule la suma de todos los numeros pares de la lista*

__Paso 1__: Definir el problema

Calcular la suma de todos los numeros pares de una lista de numeros.

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada:```lista```, ```numero```, ```sumaPara```

Proceso:

- Escribir ```lista``` con numeros
- Través de cada ```numero``` de la ```lista```, y utiliza el operador modulo ```mod``` para determinar si el numero es par
- Si el numero es par, se agrega a la ```sumaPara```

Salida: Escribir "la suma de los numeros de la lista"

__Paso 3__: Escribir el pseudocodigo

```
Algoritmo SumaNumerosPares
# Entrada
  ## Escribimos la lista que queremos calcular
	  lista<-()
	  sumaPara<-0
# Proceso
  ## Dividimos el numero para probar si es par y luego calculamos la suma de los numeros pares
	  Para numero en lista:
		Si numero mod 2<-0:
		  sumaPara<-sumaPara+numero
# Salida
  ## Obtenemos el resultado de la suma de todos los numeros pares
	  print("La suma de los numeros de la lista:", sumaPara)
Fin Algoritmo
```

## 	**Ejercicio 15**

*Crea un algoritmo que determine si un numero es positivo, negativo o cero*

__Paso 1__: Definir el problema

Determina si un numero es positivo, negativo o cero

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada:```numero```

Proceso:

- Leer el numero a verificar 
- Si el numero es mayor que cero, imprimir "El numero es positivo" 
- Si el numero es menor que cero, imprimir "El numero es negativo" 
- Si el numero es igual a cero, imprimir "El numero es cero"

Salida:

__Paso 3__: Escribir el pseudocodigo

```
Algoritmo Numero positivo,Negativo o Cero
# Entrada
  ## Escribimos el nUmero que queremos probar
	  numero<-Recuperar Integer(leer("Numero:"))
# Proceso
  ## Probamos el numero en diferentes situaciones
	  if numero > 0
		print("El número es positivo")
	  elif numero < 0
		print("El número es negativo")
	  else:
		print("El número es cero")
# Salida
  ## Obtenemos la respuesta del proceso de probar el numero
Fin Algoritmo
```

## 	**Ejercicio 16**

*Crea un algoritmo que calcule la media de la lista*

__Paso 1__: Definir el problema

Calcula la media de una lista de números enteros.

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada:```suma```,```contador```,```lista```

Proceso:

- Inicializar una variable 'suma' en cero.
- Inicializar una variable 'contador' en cero.
- Iterar a traves de cada numero en la lista.
- Agregar cada numero a la variable 'suma' y aumentar el contador en 1.
- Despues de iterar a traves de todos los numeros en la lista, dividir la variable 'suma' por el 'contador' para obtener la media.

Salida: Escribir la media de la lista.

__Paso 3__: Escribir el pseudocodigo

```
Algoritmo MediaLista
# Entrada
  ## Escribimos la lista y los primeros valores
	  lista<-()
	  suma<-0
	  contador<-0
# Proceso
  ## Calcular la media dividiendo "suma" entre "contador" 
	  para cada numero en la lista:
		suma<-suma + numero
		contador<-contador + 1
		media<-suma / contador
# Salida
  ## Obtenemos el resultado visual de la ecuacion
	  print("La media de la lista es:", media)
Fin Algoritmo
```

## 	**Ejercicio 17**

*Crea un algoritmo que genere un numero aleatorio entre 1 y 100, y le pida al usuario adivinarlo*

__Paso 1__: Definir el problema

Un algoritmo que genere un número aleatorio entre 1 y 100, y le pida al usuario adivinarlo

Formula de generar un número aleatorio:
$$
{\displaystyle X_{i}=\left(aX_{i-1}+c\right){\bmod {m}}}
$$
__Paso 2__: Poner la entrada, el proceso y la salida

Entrada:```numeroAlea```, ```numeroUser```, ```intento```

Proceso:

- Genera un número aleatorio entre 1 y 100
- introduzca un numero
- Comprueba si el numero introducido es igual al otro numero
- Comprueba si el numero introducido es menor que el otro numero
- Comprueba si el numero introducido es mayor que el otro numero

Salida: Escribir un mensaje de felicitacion y un contador con el numero de intentos

__Paso 3__: Escribir el pseudocodigo

```
Algoritmo GeneratorNumeroAleatorio
# Entrada
  ## Generamos un numero aleatorio y comenzamos el conteo del numero de intentos 
	  numeroAlea<-valor entre 1 y 100
	  intento<-0
# Proceso
  ## Repetimos el proceso del usuario tratando de encontrar el numero con indicaciones
	  Repetir
		numeroUser<-leer()
		intento<-intento+1
			si numeroUser<numeroAlea
				Escribe<-("Es mas grande. Prueba de nuevo")
			si numeroUser>numeroAlea
				Escribe<-("Es mas pequeno. Pruena de nuevo")
			si numeroUser=numeroAlea
				resultado<-("Felicidades. Encontraste el número correcto")
	  	Hasta que resultado<-("Felicidades. Encontraste el número correcto")
# Salida
  ## El usuario recibe un mensaje de felicitacion y un contador con el numero de intentos
	  Escribir(resultado+"Estos han sido tus intentos"+intentos)
Fin Algoritmo
```

## 	**Ejercicio 18**

*Crea un algoritmo que determine si una cadena de texto es un anagrama de otra cadena de texto*

__Paso 1__: Definir el problema

​	Los anagramas son cambios en el orden de las letras de una palabra que dan lugar a otra palabra diferente.

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada: ```cadena1```, ```cadena2```, ```ordenar```, ```convertirLista```, ```ordenarLista```, ```convertirCadena```, ```lista```, ```listaAgregar```

Proceso:

- Definimos las dos cadenas de texto que queremos comparar.
- Convertimos ambas cadenas a minusculas y las ordenamos alfabeticamente utilizando una funcion auxiliar `ordenar`.
- Comparamos las dos cadenas ordenadas para determinar si son iguales (es decir, si son anagramas).
- Imprimimos un mensaje indicando si las cadenas son anagramas o no.
- Las funciones auxiliares `convertirLista`, `ordenarLista` y `convertirCadena` se utilizan para convertir la cadena de texto a una lista de caracteres, ordenar la lista alfabeticamente y convertirla de nuevo en una cadena de texto, respectivamente.

Salida: Imprimimos que la palabra es un anegrama

__Paso 3__: Escribir el pseudocodigo

```
Algoritmo PruebaAnegrama
# Entrada
  ## Escribir la palabras
	  cadena1<-()
	  cadena2<-()
	  cadena1<-ordenar(cadena1.minusculas())
	  cadena2<-ordenar(cadena2.minusculas())
# Proceso
  ## Comparamos las dos cadenas para determinar si son iguales (es decir, si son anagramas)
	  Si cadena1<-cadena2 entonces:
		Escribir<-"Las cadenas son anagramas."
	  Sino:
		Escribir<-"Las cadenas no son anagramas."
  ### Funcion auxiliar para ordenar una cadena de texto
	   funcion ordenar(cadena):
		lista<-convertirLista(cadena)
	  	listaOrdenada<-ordenarLista(lista)
	  	cadenaOrdenada<-convertirCadena(listaOrdenada)
	  	retornar cadenaOrdenada
  ### Funcion auxiliar para convertir una cadena de texto en una lista de caracteres
	   funcion convertirLista(cadena):
	  	lista = []
		Para caracter en cadena hacer:
			listaAgregar(caracter)
		retornar lista
  ### Funcion auxiliar para ordenar una lista de caracteres alfabeticamente
	   funcion ordenarLista(lista):
		Para i de 0 a longitud(lista) - 1 hacer:
			Para j de 0 a longitud(lista) - 1 - i hacer:
				Si lista[j] > lista[j+1] entonces:
					temp = lista[j]
					lista[j] = lista[j+1]
					lista[j+1] = temp
	  retornar lista
  ### Funcion auxiliar para convertir una lista de caracteres en una cadena de texto
	   funcion convertirCadena(lista):
		cadena<-""
		Para caracter en lista hacer:
			cadena<-cadena+caracter
	  retornar cadena
# Salida
  ## Obtenemos la respuesta del proceso de determinar es un cadena o no
Fin Algoritmo
```

## 	**Ejercicio 19**

*Dada una lista de numeros enteros, crea un algoritmo que elimine los numeros duplicados de la lista*

__Paso 1__: Definir el problema

Crea un algoritmo que elimine los numeros duplicados de la una lista

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada:```resultados```, ```lista```

Proceso:

- Crear una ```lista``` y una lista de`resultados`.
- Recorrer la lista original de numeros enteros y agregar cada numero a la lista `resultados` solo si aun no estu en ella.
- Devolver la lista `resultados` sin los numeros duplicados.

Salida: Escribir la ```resultados``` finale sin numeros duplicados

__Paso 3__: Escribir el pseudocodigo

```
Algoritmo ListaNoNumerosDuplicados
# Entrada
  ## Insertamos una lista con numeros y creamos una lista negra para resultados
	  lista<-()
	  resultados<-()
# Proceso
  ## Recorrer la lista original de numeros enteros y agregar cada numero a la lista resultados solo si aun no estu en ella
	  Para cada elemento en lista hacer
		Si el elemento no esta en resultados Entonces
			agregar el elemento a resultados
		FinSi
	  FinPara
# Salida
  ## Recibimos una nueva lista sin numeros duplicados
	  Escribir(resultados)
Fin Algoritmo
```

## 	**Ejercicio 20**

*Crea un algoritmo que determine si un numero es capicua o no*

__Paso 1__: Definir el problema

Un numero es capicua si se lee igual de izquierda a derecha que de derecha a izquierda

__Paso 2__: Poner la entrada, el proceso y la salida

Entrada: ```numero```,```numeroInvertido```, ```numeroOriginal```

Proceso:

- Este algoritmo primero toma el numero que se desea verificar si es capicua y lo guarda en la variable `numeroOriginal`. Luego, usa un ciclo `mientras` para invertir el numero, almacenando el resultado en la variable `numeroInvertido`. El ciclo `mientras` toma el ultimo digito del numero original usando la operacion modulo (`mod`), lo agrega al numero invertido y luego elimina ese ultimo digito dividiendo el numero original por 10.

Salida: Escribir "Este numero es" o "no es" "una capicua"

__Paso 3__: Escribir el pseudocodigo

```
Algoritmo NumeroCapicua
# Entrada
  ## Insertamos el numero que queremos probar y establecemos los valores de los otros componentes
	  numero<-()
	  numeroInvertido<-0
	  numeroOriginal<-numero
# Proceso
  ## Invertimos el numero original y poco a poco le sumamos el numero invertido hasta obtener un espejo o el mismo numero de elementos
	  Mientras numero > 0 hacer
		digito<-numero MOD 10
		numeroInvertido<-numeroInvertido x 10 + digito
		numero<-Entero(numero / 10)
	  FinMientras
# Salida
  ## Obtenemos el resultado del proceso
	  Si numeroOriginal=numeroInvertido entonces
		Escribir("El número es capicua")
	  Sino
		Escribir("El número no es capicua")
	  FinSi
Fin Algoritmo
```

