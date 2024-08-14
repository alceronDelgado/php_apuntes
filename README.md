# php_apuntes
apuntes del ADSO 2843610 - Competencia ALGORITMIA

---

```PHP

<html>
  <body>
  <?php
    echo 'hello world';
  ?>
  </body>
</html>

```

## variables

--

```PHP

$nombre = "alejandro";
$apellido = "ceron";
$edad = 45;

```

### Tipos de variables

> Locales

se definen dentro de una función y son usadas exclusivamente por esas últimas.

> Globales

pueden ser accedidas dentro de cualquier parte de un programa.

> SuperGlobales

especiales sumistradas por PHP que contienen datos importantes para su codificación.

> Constantes

son valores que no cambian a lo largo del programa.

```PHP

define("nombre de la constante","valor");

```

### Datos escalares

aquellos que contienen solo una magnitud ya de un valor numérico, texto, flotante, etc.

### Concatenar

usamos el punto apra concatenar

```PHP

$nombre = "alejandro";
$apellido = " ceron";
$nombreCompleto = $nombre.$apellido;

echo $nombreCompleto;

```

### DATOS COMPUESTOS

son 2, arreglos y compuestos.

## Arreglos

para crear arreglos lo hacemos de la siguiente forma:

```PHP

$arreglo = array("llave1" => "valor1","llave3" => "valor2",);

# Otra forma

$arreglo =["llave1" => "valor1", "llave2" => "valor2"];

```

La **clave** puede ser de cualquie tipo.

```PHP

<?php
$arreglo = [
 "Nombre" => "Pedro",
 "Apellido" => "Perez",
];
echo “Buenos días". $arreglo["Nombre"] . " " .
$arreglo["Apellido"] ;
?>

```

Se pueden crear arreglos sin especificar llaves pero estas quedan definidas por la posición del elemento

```PHP

$arreglo = ["alejandro","ceron","delgado"];

echo $arreglo[2];

```

## Funciones de los arreglos.

proporsiona php una serie de funciones que nos sirve para interactuar con los arreglos.

count = retorna la dimensión del arreglo.
is_array = devuelve un boolean dependiendo si el tipo de dato que se le mando es arreglo o no.
in_array = returna 1 o true si el elemento está en el arreglo.
array_keys = retorna otro arreglo con los nombres de las llaves o con los indices del arreglo.

Ejemplo:

```PHP

$arreglo= [10,2030,20,10,100,10000];

count($arreglo) // Debe devolver la dimensión.

is_array($arreglo) //Retorna True porque si es un arreglo.

in_array($elemento,$arreglo) = //busca el elemento que le mandamos, si lo encuentra retorna ese dato, sino, retorna un 1

array_keys($arreglo) = //retorna los valores de las posiciones.

```

## Operadores lógicos

&& AND = Verdadero si ambos son verdadero.

|| or = verdadero si solo 1 de las variables es verdadera.

! NOT = Invierte el valor operado

and = Verdadero si ambos son verdadero.

or = verdadero si solo 1 de las variables es verdadera.

xor = verdadero si valor1 y valor2 son diferentes.

## Ciclo for each

con el ciclo for each podemos ciclar de una forma Más sencilla el arreglo, para esto le pasamos el arreglo y una variable adicional que es la que va a guardar los datos recorridos del arreglo.

```PHP
$j = 0;
$arreglo = [ "Jacinto", "Jose", "Pepita", "Mendieta" ];
foreach($nombreArreglo as $variable_auxiliar){
  echo $variable_auxiliar;
}

```

### Ciclo Foreach

esta forma nos sirve para recorrer arreglos asociativos, es decir ,que cada elemento tenga una clave y un valor o diccionarios.

```PHP

$arreglo = array("nombre" => "alejandro", "apellido" => "ceron");

foreach($arreglo as <'nombre'> => <$auxiliarVariable>){
  echo "$llave: $elemento \n";
}

```

## Funciones

son usadas para evitar la repetición de código y hacer los programas más entendibles.

sintaxis:

```PHP

function nombreFuncion(parametro){
  //Bloque de código.
  return valorDeseado;

}



```

```PHP

function nombreDia($dia){
  switch($dia){
    case 1: return "Domingo";
    case 2: return "Domingo";
    case 3: return "Domingo";
    default: return "Solo se de domingo o martes";
  }
}

echo nombreDia(3);

```


## Librerías.

para importar librerías usamos la sentencia include_once "nombre biblioteca.php;

también existe la palabra reservada include pero si importamos algo con include lo que hace es repetir el código.

### Obtener información del tipo de variable.

```PHP

is_array($variable)//
is_bool($variable)// Devuelve verdadero si el tipo de dato es CUMPLE CON LA SENTENCIA
is_float($variable)// Devuelve verdadero si el tipo de dato es CUMPLE CON LA SENTENCIA
is_double($variable)// Devuelve verdadero si el tipo de dato esCUMPLE CON LA SENTENCIA
is_real($variable)// Devuelve verdadero si el tipo de dato es CUMPLE CON LA SENTENCIA
is_int($variable)// Devuelve verdadero si el tipo de dato es true
is_integer($variable)// Devuelve verdadero si el tipo de dato eCUMPLE CON LA SENTENCIAe
is_long($variable)// Devuelve verdadero si el tipo de dato es CUMPLE CON LA SENTENCIA
gettype($variable) //

```

## variables globales

son variables que se pueden acceder en cualquier momento de la aplicación.

```PHP

$GLOBALS //variables globales definidas x el programa
$_SERVER //información acerca de headers, paths o ubicación de scrips o programas PHP
$_GET = variables que pasan por el programa PHP a traves del Método GET del protocolo HTTP.
$_POST = variables que pasan por el programa PHP a traves del Método POST del protocolo HTTP.
$_FILES = items cargados al programa por el método PSOT del protocolo HTTP.
$_SESSION = Son variables que están disponibles a todos los programas que se ejecutan en una sesión dependiendo del usuario.
$_COOKIE = varialbes que pasan al programa PHP a través de las cookies del protocolo HTTP.

```