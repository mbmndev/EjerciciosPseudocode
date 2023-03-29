# PRIMEROS EJERCICIOS PSEUDOCÓDIGO

### Miguel Benítez Montesinos

### Ejercicio 1

*CALCULAR LA LETRA DEL DNI ESPAÑOL*

// Definir las variables
dni = ""
letra = ""
tablaLetras = "TRWAGMYFPDXBNJZSQVHLCKE" // Tabla de letras correspondientes a cada número del DNI

// Definir las funciones
function calcularLetraDNI(dni)
    // Calcular la letra correspondiente a un número de DNI
    // La fórmula para calcular la letra es dividir el número del DNI entre 23 y obtener el resto
    // Luego, la letra correspondiente a ese resto se busca en una tabla predefinida
    numero = dni % 23
    letra = tablaLetras[numero]
    return letra

// Pedir al usuario el número del DNI
escribir("Ingrese el número del DNI: ")
leer(dni)

// Calcular la letra correspondiente al número del DNI
letra = calcularLetraDNI(dni)

// Mostrar el resultado al usuario
escribir("La letra correspondiente al DNI ", dni, " es: ", letra)

### Ejercicio 2

*CALCULAR SALARIO DE UN EMPLEADO EN ESPAÑA*


// Definir las variables
salarioBase = 0
salarioBruto = 0
retencionIRPF = 0
salarioNeto = 0

// Definir las funciones
function calcularSalarioBruto(salarioBase)
    // Calcular el salario bruto de un empleado en España
    // El salario bruto se calcula sumando el salario base más las pagas extra
    salarioBruto = salarioBase + salarioBase * 2/12 // 2 pagas extras al año
    return salarioBruto

function calcularRetencionIRPF(salarioBruto)
    // Calcular la retención del IRPF para el salario bruto de un empleado en España
    // La retención del IRPF depende del salario bruto anual y de la situación personal y familiar del empleado
    // En este pseudocódigo se utiliza una tabla predefinida para calcular la retención
    if salarioBruto <= 12450 then retencionIRPF = 0.19 // Hasta 12.450€
    else if salarioBruto <= 20200 then retencionIRPF = 0.24 // De 12.451€ a 20.200€
    else if salarioBruto <= 35200 then retencionIRPF = 0.3 // De 20.201€ a 35.200€
    else if salarioBruto <= 60000 then retencionIRPF = 0.37 // De 35.201€ a 60.000€
    else retencionIRPF = 0.45 // Más de 60.000€
    return retencionIRPF

function calcularSalarioNeto(salarioBruto, retencionIRPF)
    // Calcular el salario neto de un empleado en España
    // El salario neto se calcula restando al salario bruto la retención del IRPF
    salarioNeto = salarioBruto - salarioBruto * retencionIRPF
    return salarioNeto

// Pedir al usuario el salario base del empleado
escribir("Ingrese el salario base del empleado: ")
leer(salarioBase)

// Calcular el salario bruto, la retención del IRPF y el salario neto
salarioBruto = calcularSalarioBruto(salarioBase)
retencionIRPF = calcularRetencionIRPF(salarioBruto)
salarioNeto = calcularSalarioNeto(salarioBruto, retencionIRPF)

// Mostrar los resultados al usuario
escribir("El salario bruto del empleado es: ", salarioBruto)
escribir("La retención del IRPF es: ", retencionIRPF)
escribir("El salario neto del empleado es: ", salarioNeto)

### Ejercicio 3

*DETERMINAR LA RUTA PARA LLEGAR A UNA CIUDAD POR AVIÓN.*

// Definir las variables
ciudadOrigen = ""
ciudadDestino = ""
aerolinea = ""
ruta = ""
distancia = 0
duracion = 0

// Definir las funciones
function buscarRuta(ciudadOrigen, ciudadDestino, aerolinea)
    // Usar una base de datos o una API para buscar la mejor ruta entre las dos ciudades
    // según la aerolínea especificada
    // La función debería devolver la ruta encontrada, la distancia en kilómetros y la duración en minutos

// Pedir al usuario las ciudades de origen y destino y la aerolínea
escribir("Ingrese la ciudad de origen: ")
leer(ciudadOrigen)

escribir("Ingrese la ciudad de destino: ")
leer(ciudadDestino)

escribir("Ingrese la aerolínea: ")
leer(aerolinea)

// Buscar la ruta
ruta, distancia, duracion = buscarRuta(ciudadOrigen, ciudadDestino, aerolinea)

// Mostrar los resultados al usuario
escribir("La mejor ruta para llegar de ", ciudadOrigen, " a ", ciudadDestino, " por ", aerolinea, " es: ", ruta)
escribir("La distancia es de ", distancia, " kilómetros y la duración estimada es de ", duracion, " minutos.")

### Ejercicio 4

*CALCULA EL ÁREA Y PERÍMETRO DE UN CÍRCULO DADO SU RADIO.*

// Definir las variables
radio = 0
area = 0
perimetro = 0

// Definir las funciones
function calcularArea(radio)
    // Calcular el área de un círculo dado su radio
    // La fórmula para el área es pi x radio al cuadrado
    area = pi *radio* radio
    return area

function calcularPerimetro(radio)
    // Calcular el perímetro de un círculo dado su radio
    // La fórmula para el perímetro es 2 x pi x radio
    perimetro = 2 *pi* radio
    return perimetro

// Pedir al usuario el radio del círculo
escribir("Ingrese el radio del círculo: ")
leer(radio)

// Calcular el área y el perímetro
area = calcularArea(radio)
perimetro = calcularPerimetro(radio)

// Mostrar los resultados al usuario
escribir("El área del círculo es: ", area)
escribir("El perímetro del círculo es: ", perimetro)

### Ejercicio 5

*DADA UNA LISTA DE NÚMEROS ENTEROS DETERMINA CUAL ES MAYOR Y CUÁL ES MENOR.*

// Definir la lista de números enteros
numeros = []

// Definir las funciones
function encontrarMaximo(lista)
    // Encontrar el número máximo en una lista de números enteros
    maximo = lista[0]
    para cada numero en lista
        si numero > maximo entonces maximo = numero
    fin para
    devolver maximo

function encontrarMinimo(lista)
    // Encontrar el número mínimo en una lista de números enteros
    minimo = lista[0]
    para cada numero en lista
        si numero < minimo entonces minimo = numero
    fin para
    devolver minimo

// Encontrar el número máximo y el número mínimo en la lista de números enteros
maximo = encontrarMaximo(numeros)
minimo = encontrarMinimo(numeros)

// Mostrar los resultados al usuario
escribir("El número máximo en la lista es: ", maximo)
escribir("El número mínimo en la lista es: ", minimo)

### Ejercicio 6

*CREA UN ALGORITMO QUE CONVIERTA GRADOS CELSIUS A FAHRENHEIT.*

// Definir la temperatura en grados Celsius
celsius = 25

// Definir la función para convertir Celsius a Fahrenheit
function convertirCelsiusAFahrenheit(celsius)
    fahrenheit = (celsius * 9/5) + 32
    devolver fahrenheit

// Convertir la temperatura de Celsius a Fahrenheit
fahrenheit = convertirCelsiusAFahrenheit(celsius)

// Mostrar el resultado al usuario
escribir("La temperatura en grados Fahrenheit es: ", fahrenheit)

### Ejercicio 7

*DADO UN NÚMERO ENTERO, CREA UN ALGORITMO DETERMINE ES PAR O IMPAR.*

// Definir el número entero
numero =

// Definir la función para determinar si un número es par o impar
function determinarParidad(numero)
    si numero % 2 == 0 entonces
        devolver "par"
    sino
        devolver "impar"
    fin si

// Determinar si el número es par o impar
paridad = determinarParidad(numero)

// Mostrar el resultado al usuario
escribir("El número ", numero, " es ", paridad)

### Ejercicio 8

*CREA UN ALGORITMO QUE DETERMINE SI UN AÑO ES BISIESTO O NO.*

// Definir el año
año =

// Definir la función para determinar si un año es bisiesto o no
function esBisiesto(año)
    si (año % 4 == 0 y año % 100 != 0) o año % 400 == 0 entonces
        devolver verdadero
    sino
        devolver falso
    fin si

// Determinar si el año es bisiesto o no
si esBisiesto(año) entonces
    escribir(año, " es un año bisiesto")
sino
    escribir(año, " no es un año bisiesto")
fin si

### Ejercicio 9

*CREA UN ALGORITMO QUE DETERMINE SI UNA CADENA DE TEXTO ES PALÍNDROMO O NO.*

// Definir la cadena de texto
cadena = ""

// Definir la función para determinar si una cadena es palíndromo o no
function esPalindromo(cadena)
    // Convertir la cadena a minúsculas y eliminar los espacios en blanco
    cadena = cadena.toLowerCase().replace(/\s+/g, '')

    // Crear una variable para almacenar la cadena invertida
    cadenaInvertida = ""
    
    // Recorrer la cadena de texto de atrás hacia adelante y concatenarla en la variable cadenaInvertida
    para i desde cadena.longitud - 1 hasta 0 hacer
        cadenaInvertida = cadenaInvertida + cadena[i]
    fin para
    
    // Comparar la cadena original con la cadena invertida
    si cadena == cadenaInvertida entonces
        devolver verdadero
    sino
        devolver falso
    fin si

// Determinar si la cadena es palíndromo o no
si esPalindromo(cadena) entonces
    escribir(cadena, " es un palíndromo")
sino
    escribir(cadena, " no es un palíndromo")
fin si


### Ejercicio 10

*DADA UNA LISTA DE NOMBRES, CREA UN ALGORITMO QUE ORDENE LA LISTA ALFABÉTICAMENTE.*

// Definimos la lista de nombres
listaNombres = ["Juan", "María", "Ana", "Pedro", "Luisa", "Jorge"]

// Función para ordenar alfabéticamente una lista de nombres
funcion ordenarNombres(lista) {
  // Utilizamos el método sort para ordenar alfabéticamente la lista
  lista.sort()

  // Retornamos la lista ordenada
  retornar lista
}

// Llamamos a la función ordenarNombres y guardamos el resultado en la variable listaNombresOrdenada
listaNombresOrdenada = ordenarNombres(listaNombres)

// Imprimimos por consola la lista ordenada
imprimir(listaNombresOrdenada)


### Ejercicio 11

*Crea un algoritmo que calcule el factorial de un número entero.*

//Definir una función factorial que reciba como parámetro un número entero n:
    si n es igual a 0 o 1 entonces
        retornar 1
    fin si
    
//Definir una variable resultado e inicializarla en 1
//Definir una variable i e inicializarla en 2
    
    mientras i sea menor o igual a n hacer
        resultado = resultado * i
        i = i + 1
    fin mientras
    
    retornar resultado
Fin función

### Ejercicio 12

*Dado un número entero, crea un algoritmo que determine si es primo o no.*

// Función para determinar si un número entero es primo o no
funcion esPrimo(numero) {
  // Si el número es igual a 1, no es primo
  si (numero == 1) {
    retornar falso
  }

  // Verificamos si el número es divisible por algún número entre 2 y su mitad
  para (i = 2; i <= numero/2; i++) {
    si (numero % i == 0) {
      // Si el número es divisible, no es primo
      retornar falso
    }
  }

  // Si el número no fue divisible por ningún número entre 2 y su mitad, es primo
  retornar verdadero
}

// Ejemplo de uso
numero = 17
si (esPrimo(numero)) {
  imprimir(numero + " es primo")
} sino {
  imprimir(numero + " no es primo")
}

### Ejercicio 13

*Crea un algoritmo que calcule el área y volumen de un cubo dado su lado.*

// Función para calcular el área de un cubo dado su lado
funcion calcularArea(lado) {
  area = 6 * lado * lado
  retornar area
}

// Función para calcular el volumen de un cubo dado su lado
funcion calcularVolumen(lado) {
  volumen = lado * lado * lado
  retornar volumen
}

// Ejemplo de uso
lado = 5
area = calcularArea(lado)
volumen = calcularVolumen(lado)
imprimir("El área del cubo es: " + area)
imprimir("El volumen del cubo es: " + volumen)

### Ejercicio 14

*Dada una lista de números enteros, crea un algoritmo que calcule la suma de todos los números pares de la lista.*

// Función para calcular la suma de todos los números pares de una lista de números enteros
funcion sumaNumerosPares(lista) {
  suma = 0
  para cada numero en lista {
    si (numero % 2 == 0) {
      suma = suma + numero
    }
  }
  retornar suma
}

// Ejemplo de uso
lista = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
suma = sumaNumerosPares(lista)
imprimir("La suma de todos los números pares de la lista es: " + suma)


### Ejercicio 15

*Crea un algoritmo que determine si un número es positivo, negativo o cero.*

// Función para determinar si un número es positivo, negativo o cero
funcion determinarSigno(numero) {
  si (numero > 0) {
    retornar "positivo"
  } sino si (numero < 0) {
    retornar "negativo"
  } sino {
    retornar "cero"
  }
}

// Ejemplo de uso
numero = 5
signo = determinarSigno(numero)
imprimir("El número es " + signo)


### Ejercicio 16

*Dada una lista de números enteros, crea un algoritmo que calcule la media de la lista.*

// Función para calcular la media de una lista de números enteros
funcion calcularMedia(lista) {
  suma = 0
  para cada numero en lista {
    suma = suma + numero
  }
  media = suma / longitud(lista)
  retornar media
}

// Ejemplo de uso
lista = [2, 4, 6, 8, 10]
media = calcularMedia(lista)
imprimir("La media de la lista es: " + media)


### Ejercicio 17

*Crea un algoritmo que genere un número aleatorio entre 1 y 100, y le pida al usuario adivinarlo.*
*El algoritmo deberá indicar si el número introducido es mayor o menor que el número aleatorio, hasta que el usuario adivine el número correcto.*

// Función para generar un número aleatorio entre 1 y 100
funcion generarNumeroAleatorio() {
  numero = aleatorio(1, 100) // la función aleatorio() genera un número aleatorio entre los valores dados (1 y 100)
  retornar numero
}

// Función para pedir al usuario que adivine el número aleatorio y comprobar si es correcto
funcion adivinarNumero() {
  numeroAleatorio = generarNumeroAleatorio()
  adivinado = falso
  mientras (adivinado == falso) {
    numero = leerNumero()
    si (numero == numeroAleatorio) {
      imprimir("¡Adivinaste el número!")
      adivinado = verdadero
    } sino si (numero < numeroAleatorio) {
      imprimir("El número introducido es menor que el número aleatorio.")
    } sino {
      imprimir("El número introducido es mayor que el número aleatorio.")
    }
  }
}

// Ejemplo de uso
adivinarNumero()

### Ejercicio 18

*Crea un algoritmo que determine si una cadena de texto es un anagrama de otra cadena de texto.*

// Función para determinar si dos cadenas son anagramas
funcion esAnagrama(cadena1, cadena2) {
  // Si las cadenas tienen diferente longitud, no pueden ser anagramas
  si (longitud(cadena1) != longitud(cadena2)) {
    retornar falso
  }

  // Convertir las cadenas a minúsculas y ordenar sus caracteres
  cadena1 = ordenar(cadena1.toLowerCase())
  cadena2 = ordenar(cadena2.toLowerCase())

  // Comparar las cadenas ordenadas
  si (cadena1 == cadena2) {
    retornar verdadero
  } sino {
    retornar falso
  }
}

// Ejemplo de uso
cadena1 = "roma"
cadena2 = "amor"
si (esAnagrama(cadena1, cadena2)) {
  imprimir("Las cadenas son anagramas.")
} sino {
  imprimir("Las cadenas no son anagramas.")
}

### Ejercicio 19

*Dada una lista de números enteros, crea un algoritmo que elimine los números duplicados de la lista.*

// Función para eliminar los números duplicados de una lista
funcion eliminarDuplicados(lista) {
  // Crear un conjunto vacío para almacenar los números únicos
  conjunto = conjuntoVacio()

  // Recorrer la lista
  para cada numero en lista {
    // Si el número no está en el conjunto, agregarlo
    si (numero no está en conjunto) {
      agregar(numero, conjunto)
    }
  }

  // Convertir el conjunto en una lista y retornarla
  retornar listaDesdeConjunto(conjunto)
}

// Ejemplo de uso
lista = [1, 2, 3, 2, 4, 5, 1, 3]
listaSinDuplicados = eliminarDuplicados(lista)
imprimir(listaSinDuplicados)

### Ejercicio 20

*Crea un algoritmo que determine si un número es capicúa o no.*

// Función para determinar si un número es capicúa
funcion esCapicua(numero) {
  // Convertir el número en una cadena de texto
  cadena = convertirCadena(numero)

  // Obtener la longitud de la cadena
  longitud = longitudCadena(cadena)

  // Recorrer la mitad de la cadena
  para i desde 0 hasta (longitud / 2) redondeadoHaciaAbajo {
    // Comparar los caracteres de las extremidades
    si (caracterEn(cadena, i) != caracterEn(cadena, longitud - i - 1)) {
      // Si los caracteres son diferentes, el número no es capicúa
      retornar falso
    }
  }

  // Si llegamos hasta aquí, el número es capicúa
  retornar verdadero
}

// Ejemplo de uso
numero = 12321
si (esCapicua(numero)) {
  imprimir("El número " + numero + " es capicúa")
} else {
  imprimir("El número " + numero + " no es capicúa")
}




