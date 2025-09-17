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
 * Programa que determina si una edad es menor o mayor de edad
 * @author prorix
 * @version 1.0.0
 */
 
  	$numeroPositivo = 1;
    $numeroNegativo = -1;
    $cero = 0;
    
    positivoNegativoCero($numeroPositivo);
    positivoNegativoCero($numeroNegativo);
    positivoNegativoCero($cero);

 /**
 * Metodo que determina si una edad dada es menor o mayor de edad
 */
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
 * Función que determina la calificacion segun la nota
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
 * Programa que muestra todos los números del 1 al 100
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
 * Programa que muestra todos los números pares entre 1 y 50
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
 * Función que calcula el factorial de un numero
 * @param int $numero del que se quiere calcular el factorial
 * @return factorial del número
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
