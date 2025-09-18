# Acceso a datos
## Tarea: Creacion y uso de elementos basicos en php
## Alumno: Romen Gilberto Garcia Gomez (PRORIX)

## BLOQUE 1: Conceptos basicos
### EJERCICIO 1: Mayor de dos numeros
#### Pide dos numeros y muestra cual es mayor o si son iguales.

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que pide dos numeros y muestra cual es mayor
 * o si son iguales
 * @author prorix
 * @version 1.0.0
 */
 
    $numero1 = 10;
    $numero2 = 20;

    echo "el numero 1 es: $numero1 <br>";
    echo "el numero 2 es: $numero2 <br>";

    if ( $numero1>$numero2 ) {
        echo "$numero1 es mayor que $numero2";
    }else if ( $numero1<$numero2 ) {
        echo "$numero2 es mayor que $numero1";
    }else{
        echo 'Ambos numeros son iguales';
    }

?>

</body>
</html>

```

Output:

```

el numero 1 es: 10
el numero 2 es: 20
20 es mayor que 10

```


### EJERCICIO 2: Edad permitida
#### Pide la edad de una persona y muestra un mensaje de si es menor de edad, u otro si es mayor de edad.

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que determina si una edad es menor o mayor de edad
 * @author prorix
 * @version 1.0.0
 */
 
  	$edadMenorDeEdad = 15;
    $edadMayorDeEdadJusto = 18;
    $edadMayorDeEdad = 20;
    
    determinarMayoriaDeEdad($edadMenorDeEdad);
    determinarMayoriaDeEdad($edadMayorDeEdadJusto);
    determinarMayoriaDeEdad($edadMayorDeEdad);

 /**
 * Metodo que determina si una edad dada es menor o mayor de edad
 */
 function determinarMayoriaDeEdad($edad){
 	if ( $edad < 18 ) {
    	echo "Tienes $edad años, eres menor de edad. <br>";
    } else {
    	echo "Tienes $edad años, eres mayor de edad. <br>";
    }
 }
 
?>

</body>
</html>

```

Output:

```

Tienes 15 años, eres menor de edad.
Tienes 18 años, eres mayor de edad.
Tienes 20 años, eres mayor de edad.

```


### EJERCICIO 3: Positivo, negativo o cero
#### Comprueba si un numero almacenado en una variable es positivo, negativo o cero.

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que determina si un numero es positivo, negativo o cero
 * @author prorix
 * @version 1.0.0
 */
 
  	$numeroPositivo = 1;
    $numeroNegativo = -1;
    $cero = 0;
    
    positivoNegativoCero($numeroPositivo);
    positivoNegativoCero($numeroNegativo);
    positivoNegativoCero($cero);


 function positivoNegativoCero($numero){
 	$resultado = "El numero $numero es positivo <br>";
    
 	if ( $numero < 0 ) {
    	$resultado = "El numero $numero es negativo <br>";
    } else if ($numero == 0){
    	$resultado = "El numero es 0 <br>";
    }
    
    echo $resultado;
    
 }
 
?>

</body>
</html>

```

Output:

```

El numero 1 es positivo
El numero -1 es negativo
El numero es 0

```


### EJERCICIO 4: Nota final
#### Pide la nota de un alumno y muestra un mensaje segun su puntuacion.

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que determina la calificacion de una nota
 * @author prorix
 * @version 1.0.0
 */
 
    $notaSuspenso = 1;
    $notaAprobado = 5;
    $notaNotable = 8;
    $notaSobresaliente = 10;
    $notaNoValida1 = -1;
    $notaNoValida2 = 11;
    
    calcularNota($notaSuspenso);
    calcularNota($notaAprobado);
    calcularNota($notaNotable);
    calcularNota($notaSobresaliente);
    calcularNota($notaNoValida1);
    calcularNota($notaNoValida2);

/**
 * Funcion que determina la calificacion segun la nota
 */
function calcularNota($nota){
    if ($nota < 0 || $nota > 10) {
        $resultado = "$nota no es una nota válida (0-10) <br>";
    } else if ($nota < 5) {
        $resultado = "Un $nota es un suspenso <br>";
    } else if ($nota < 7) {
        $resultado = "Un $nota es un aprobado <br>";
    } else if ($nota < 9) {
        $resultado = "Un $nota es un notable <br>";
    } else {
        $resultado = "Un $nota es un sobresaliente <br>";
    }
    
    echo $resultado;
}
 
?>

</body>
</html>

```

Output:

```

Un 1 es un suspenso
Un 5 es un aprobado
Un 8 es un notable
Un 10 es un sobresaliente
-1 no es una nota válida (0-10)
11 no es una nota válida (0-10)

```


## BLOQUE 2: Bucles
### EJERCICIO 5: Contar del 1 al 100
### Muestra los numeros del 1 al 100 en pantalla.

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que muestra todos los numeros del 1 al 100
 * @author prorix
 * @version 1.0.0
 */

for ($i = 1; $i <= 100; $i++) {
    echo $i . "<br>";
}

?>

</body>
</html>

```

Output:

```

1
2
3
4
5
...
100

```


### EJERCICIO 6: Suma acomulada
#### Calcula la suma de los numeros del 1 al 50 usando un bucle.

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que suma todos los numeros del 1 al 50
 * @author prorix
 * @version 1.0.0
 */

$resultado = 0;

for ($i = 1; $i <= 50; $i++) {
    $resultado += $i;
}

echo $resultado;

?>

</body>
</html>

```

Output:

```

1275

```


### EJERCICIO 7: Tabla de multiplicar
#### Pide un numero y genera su tabla de multiplicar del 1 al 10.

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que pide un numero y genera su tabla de multiplicar del 1 al 10
 * @author prorix
 * @version 1.0.0
 */

$numeroEjemplo = 9;

generarTablasMultiplicar($numeroEjemplo);

function generarTablasMultiplicar($numero){
for ($i = 1; $i <= 10; $i++) {
	$producto = $numero * $i;
    echo "$numero * $i = $producto <br>";
}
}

?>

</body>
</html>

```

Output:

```

9 * 1 = 9
9 * 2 = 18
9 * 3 = 27
9 * 4 = 36
9 * 5 = 45
9 * 6 = 54
9 * 7 = 63
9 * 8 = 72
9 * 9 = 81
9 * 10 = 90

```


### EJERCICIO 8: Numeros pares
#### Muestra todos los numeros pares entre 1 y 50.

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que muestra todos los numeros pares entre 1 y 50
 * @author prorix
 * @version 1.0.0
 */

mostrarNumerosPares();

function mostrarNumerosPares(){
    for ($i = 1; $i <= 50; $i++) {
        if ($i % 2 == 0) {
            echo "$i <br>";
}
}
}

?>

</body>
</html>

```

Output:

```

2
4
6
8
10
...
50

```


### EJERCICIO 9: Cuenta atras
### Haz un bucle que cuente de 10 a 1 y despues muestre ```¡Fin!```

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que hace una cuenta atras
 * @author prorix
 * @version 1.0.0
 */

cuentaAtras();

function cuentaAtras(){
    for ($i = 10; $i > 0; $i--) {
            echo "$i <br>";
}
	echo "¡Fin!";
}

?>

</body>
</html>

```

Output:

```

10
9
8
7
6
5
4
3
2
1
¡Fin!

```


### EJERCICIO 10: Factorial
#### Calcula el factorial de un numero introducido

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que calcula el factorial de un numero
 * @author prorix
 * @version 1.0.0
 */

$numeroEjemplo = 5;

echo "El factorial de $numeroEjemplo es " . calcularFactorial($numeroEjemplo);

/**
 * Funcion que calcula el factorial de un numero
 */
function calcularFactorial($numero){
    $factorial = 1;

    for ($i = 1; $i <= $numero; $i++) {
        $factorial *= $i;
    }

    return $factorial;
}

?>

</body>
</html>

```

Output:

```

El factorial de 5 es 120

```


## BLOQUE 3: Combinando condicionales y Bucles
### EJERCICIO 11: Numeros primos
#### Escribe un algoritmo que muestre los numeros primos entre 1 y 50.

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que muestra los numeros primos entre 1 y 50
 * @author prorix
 * @version 1.0.0
 */

function mostrarPrimos() {

    for ($i = 2; $i <= 50; $i++) {
        $esPrimo = true;

        for ($j = 2; $j <= sqrt($i); $j++) {
            if ($i % $j == 0) {
                $esPrimo = false;
                break;
            }
        }

        if ($esPrimo) {
            echo $i . " ";
        }
    }
}

mostrarPrimos();

?>

</body>
</html>

```

Output:

```

 2 3 5 7 11 13 17 19 23 29 31 37 41 43 47 

```


### EJERCICIO 12: Fibonacci
#### Genera los primeros 20 terminos de la secuencia de Fibonacci.

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que muestra los primeros 20 numeros de la secuencia de Fibonacci
 * @author prorix
 * @version 1.0.0
 */

function primerosVeinteFibonacci() {
    $numero1 = 0;
    $numero2 = 1;
    echo "$numero1, $numero2";

    for ($i = 3; $i <= 20; $i++) {
        $numeroResultado = $numero1 + $numero2;
        echo ", $numeroResultado";
        $numero1 = $numero2;
        $numero2 = $numeroResultado;
    }
}

primerosVeinteFibonacci();

?>

</body>
</html>

```

Output:

```

 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377, 610, 987, 1597, 2584, 4181

```


### EJERCICIO 13: Multiplos de un numero
#### Pide un numero n y muestra sus multiplos hasta 100

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que dado un numero muestra sus multiplos hasta 100
 * @author prorix
 * @version 1.0.0
 */

function mostrarMultiplos($numero) {
	$resultado = 0;
    $multiplo = 1;
    
    while ($resultado < 100) {
        $resultado = $numero * $multiplo;
        echo "$resultado <br>";
        $multiplo++;
    }
}

$numeroEjemplo = 10;
mostrarMultiplos($numeroEjemplo);

?>

</body>
</html>

```

Output:

```

10
20
30
40
50
60
70
80
90
100 

```


### EJERCICIO 14: Suma de pares e impares
#### Calcula la suma de los numeros pares e impares entre 1 y 100 por separado.

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que suma por separado los pares e impares entre 1 y 100
 * @author prorix
 * @version 1.0.0
 */

function sumaParesImpares() {
	$resultadoPares = 0;
    $resultadoImpares = 0;
    
    for ($i = 1 ; $i <= 100 ; $i++) {
        if ( $i % 2 == 0 ) {
        	$resultadoPares += $i;
        } else {
        	$resultadoImpares += $i;
        }
    }
    echo "Pares: $resultadoPares <br>";
    echo "Impares: $resultadoImpares";
}

sumaParesImpares();

?>

</body>
</html>

```

Output:

```

Pares: 2550
Impares: 2500 

```


### EJERCICIO 15: Adivinar numero
#### Genera un numero aleatorio entre 1 y 20 y pide al usuario que adivine.

Code:

```php

TODO

```

Output:

```

TODO

```


## BLOQUE 4: Construccion de algoritmos
### EJERCICIO 16: Numero perfecto
#### Comprueba si un numero es perfecto

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que comprueba si un numero es perfecto
 * @author prorix
 * @version 1.0.0
 */

function numeroPerfecto($numero) {
	$suma = 0;
    
    
    for ($i = 1 ; $i < $numero ; $i++) {
        if ( $numero % $i == 0 ) {
        	$suma += $i;
        }
    }
    
    if ($suma == $numero){
    	echo "$numero es un numero perfecto <br>";
    } else{
    	echo "$numero no es un numero perfecto <br>";
    }

}

$numeroPerfecto = 6;
$numeroNoPerfecto = 5;
numeroPerfecto($numeroPerfecto);
numeroPerfecto($numeroNoPerfecto);

?>

</body>
</html>

```

Output:

```

6 es un numero perfecto
5 no es un numero perfecto 

```


### EJERCICIO 17: Invertir numero
#### Escribe un algoritmo que invierta los digitos de un numero

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que invierte un numero
 * @author prorix
 * @version 1.0.0
 */

function invertirNumero($numero) {
    
$numeroInvertido = strrev($numero);
echo "$numero invertido es $numeroInvertido";

}

$numeroEjemplo = 123;
invertirNumero($numeroEjemplo);

?>

</body>
</html>

```

Output:

```

 123 invertido es 321 

```


### EJERCICIO 18: Palindromo
#### Comprueba si una palabra almacenada en una variable es palindroma.

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que comprueba si una palabra es palindroma
 * @author prorix
 * @version 1.0.0
 */

function comprobarPalindroma($palabra) {
    
$palabraInvertida = strrev($palabra);
if ($palabraInvertida == $palabra){
	echo "$palabra es un palindromo <br>";
} else {
	echo "$palabra no es un palindromo <br>";
}
}

$palabraPalindroma = "reconocer";
$palabraNoPalindroma = "melocoton";
comprobarPalindroma($palabraPalindroma);
comprobarPalindroma($palabraNoPalindroma);


?>

</body>
</html>

```

Output:

```

reconocer es un palindromo
melocoton no es un palindromo 

```


### EJERCICIO 19: Maximo comun divisor
#### Escribe un alogirtmo que calcule el MCD de dos numeros

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que calcula el MCD de dos numeros
 * @author prorix
 * @version 1.0.0
 */

function calcularMCD($numero1, $numero2) {
    $numeroMenor = min($numero1, $numero2);
    $mcd = 1;

    for ($i = $numeroMenor; $i > 0; $i--) {
        if ($numero1 % $i == 0 && $numero2 % $i == 0) {
            $mcd = $i;
            break;
        }
    }
    echo "El MCD de $numero1 y $numero2 es $mcd.";
}

$numero1ejemplo = 10;
$numero2ejemplo = 5;

calcularMCD($numero1ejemplo, $numero2ejemplo);

?>

</body>
</html>

```

Output:

```

 El MCD de 10 y 5 es 5. 

```


### EJERCICIO 20: Triangulo de asteriscos
#### Muestra en pantalla un triangulo de altura ```n``` usando ```*```.

Code:

```php

<!DOCTYPE html>
<html>
<body>

<?php

/**
 * Programa que dibuja un triangulo de tamano n dado
 * @author prorix
 * @version 1.0.0
 */

function dibujarTriangulo($tamano) {
    for ($i = 1; $i <= $tamano; $i++) {
        for ($j = 0; $j < $i; $j++) {
            echo "*";
        }
        echo "<br>";
    }
}

$tamanoPrueba = 10;

dibujarTriangulo($tamanoPrueba);

?>

</body>
</html>

```

Output:

```

*
**
***
****
*****
******
*******
********
*********
**********

```
