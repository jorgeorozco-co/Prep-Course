# HomeWork 03-JS-II Conceptos
1. En un archivo de texto separado que debes crear, escribe explicaciones de los siguientes conceptos como si se lo estuvieras explicando a un niño de 12 años. Hacer esto te ayudará a descubrir rápidamente cualquier agujero en tu comprensión.

## * `for`
Es una estructura de control de flujo(secuencia de ejecución de instrucciones) denominados BUCLES. Es un procedimiento por el cual la ejecución de un fragmento de código itera o se repite de forma controlada un número determinado o indeterminado de veces.

El formato de esta estructura es el Siguiente:
Empieza con la palabra reservada `for`.
Seguido y entre paréntesis se determina 2 pasos separados por `;` el primero inicializa el indice que recorrerá las iteraciones del for, en segundo lugar se evalua este indice, luego un tercer paso que ejecuta el bloque de código entre corchetes, a continuación pasa a un cuarto (4) paso al final de las instrucciones que estan entre paréntesis y que incrementara el ciclo asignando dos signos plus (++):

### PASOS:

1. Incialización de la variables índice.
2. Condición que permite detener el bucle.
3. Ejecuta Bloque de Código entre Corchetes.
4. Incremento de la variable índice.
    
### for (Paso 1  ; Paso 2  ; Paso 4)  
### { Paso 3   Bloque de Código    
            Inicio del bloque...
            ...            
            si el indice cumple la condicion ir al
                paso 4 e incrementa su valor. Luego
                va al paso 2 y se evalua nuevamente.

            si no sale del bucle.
            ...
            final del bloque...
### }


## for( Inicia índice; Condicional; Incremento){ Bloque de Código }


Una vez establecido estas etapas del bucle entre paréntesis seguiremos detallando entre Corchetes `{}` las instrucciones que queremos, que se repitan.

Para poder explicar como funciona el for veamos un ejemplo sencillo:

* Supongamos que deseamos imprimir en pantalla la suma de los números del  0 al 5. entonces serán 6 entradas si empezamos a contar desde 0 hasta el 5   (0,1,2,3,4,5).

Primero vamos a usar una variable donde acumularemos la suma de i a medida que entra en el bucle.

```javascript
//Iniciamos la variable `acumIndice` a cero fuera del for

var acumIndice = 0; 

```


Nos debe acumular un total de 15 en 6 entradas al bucle, pero se presentarán casos en los que seràn muchos más, así que por el momento veamos este:

Si seguimos la instrucción, nos dice que debemos empezar con la palabra reservada `for` seguido de paréntesis de apertura y cierre, y seguido a este corchetes de apertura y cierre `{}`.

```javascript

for(i=0;...;...) {}

//1er Paso: iniciamos la variable "i" a cero. Ya 
//veremos mas adelante las instrucciónes que usaremos
//donde estan los puntos suspensivos.

```
Al iniciar la variable indice `i` con valor a cero (0) le estamos indicando al bucle for, que sus instrucciones dentro de los corchetes`{}` empiezan con este valor.
Acto seguido, el for evaluará bien sea el indice u otra variable bajo una condición dada en el segundo paso, y que permite controlar las repeticiones de ejecución, y con ello salir del bucle.

```javascript

for(i=0; i<=5;...){}

//2 Paso: Se evalua si el valor que contiene el
//indice 'i' (0) es menor que 5. Una vez llegue a 5
//saldrá del bucle o repetición de código, que para
//este caso se le ha indicado seguir en el bucle 
//mientras sea menor o igual a 5.

```
Ya estando en esta instancia, el ciclo (bucle) `for` entra a realizar las instrucciones que se encuentren dentro del corchete en su primer vez con un valor en el indice, de cero (0), y la variable `acumIndice` en cero (0) también...

```javascript

var acumIndice=0;
for(i=0; i<=5;...){
    //La primer instrucción imprime en pantalla el
    // valor de entrada i
    console.log("Entrada No."+i+" al Bloque entre corchetes ")

    //La segunda Instrucción acumula el valor que
    //contiene i en su primera iteración al bloque,
    //asi que su primer valor es cero

    acumIndice = acumIndice+i; // 1er entrada aqui (0 = 0 + 0;)

    //Esta vez se imprime en pantalla el acumulado
    // sumado de i en su 1er entrada y así se irá 
    //sumando sucesivamente hasta salir del bucle o 
    //repeticiónes.

    console.log(" Valor Suma de indice: "+acumIndice);

}
```

Ya vamos en la primer iteración o primer ciclo de 6; recuerde que las entradas van desde 0 hasta 5, eso nos da un total de 6 entradas.

Ahora, ¿Cómo hace posible `for`volver a ingresar? El siguiente paso(PASO 4) lo hace posible, pues la instrucción del cuarto paso, indica al `for` que incrementará en uno la variable `í` (i++).

Una vez Incrementada `i` en 1 su valor actual ya no será cero (0) sino uno (1). ahora `i` vale 1.

Bien hasta aqui? La instrucción `for` no se queda solamente en el incremento (PASO 4), ahora lleva el valor de `i` al PASO 2 para volver a ser evaluada nuevamente, entonces la instrucción de condición vuelve a preguntar:

si `i`es menor o igual a 5 ...for (...;i<=5;...).

Ahora volverá a ingresar al bloque si esta condición se cumple, que para este caso lógicamente así es, pues i ya valdria 1 y es menor que 5. 

Volverá a acumular el valor de i en la variable `acumIndice` que antes tenía un valor de cero, ahora se le sumará el indice con valor 1 dejando a `acumIndice` acumulando asi la suma de `i`.

Así sucesivamente se repite este ciclo mientras i sea menor o igual a 5.

Para poder ver el codigo en ejecución, deberemos ingresar estas instrucciones dentro de una función y luego llamarla.

El códio completo "mejorado" quedaría asi:

```javascript

//Llamaremos a la función sumIndice sin argumentos...

function sumIndice(){

    var acumIndice=0;
    for(i=0;i<=5;i++){

        console.log("============ENTRADA(i) :  "+i+"   ==============");
        console.log("acumIndice = "+acumIndice+" +  "+i);

        acumIndice=acumIndice+i; 

        console.log("ACUMINDICE ACUMULA: "+acumIndice);

        if (i===5){console.log(" (i) Ya no incremta: Sale del Bucle");}
        else {console.log("despuès de este paso se incrementará (i) en 1.");}
    }
    return "TOTAL ACUMULADO: "+acumIndice;
}

```
Un `for` lo podemos referenciar para realizar operaciones con `cadenas de caràcteres` o conjunto de datos entre comillas.  

Las Cadenas de carácteres se pueden recorrer en cada posición o `Columna` unica, definida por cada carácter. Ejemplo:

//La siguiente instrucción agrupa Carácteres entre 
//comillas en un Variable de tipo Cadena denominado 'miCadena'.

miCadena="Mi cadena";


Note que la frase entre comillas agrupa varias letras (carácteres) en una sola linea y cada letra o carácter representa una columna.

Sabemos que está contenida en una sola linea, si tuvieramos que recorrer esta frase, carácter por carácter, nos referiríamos a ella como carácter en la posición (i); posición(0) para el primer carácter, o primer columna. Para ello la recorremos con un indice (eg. i) que apunte a esta posición.

Asi, la palabra "miCadena" tendría la dirección cero; miCadena[0] para la primer letra ("M") de esta frase; miCadena[1], para la segunda letra ("i") y así sucesivamente hasta terminar la frase, "Mi cadena".

* Tome en cuenta que el espacio entre "Mi" y "cadena" también hace referencia a una columna.

```javascript

//La siguiente función muestra en consola cada 
//posición de la cadena "Mi cadena"

function verCadena(cadena){

//Creamos un nuevo objeto de tipo STRING(cadena).
var miCadena= new String(cadena); 

//El indice 'i' se utilizará para identificar la 
//posición de columna de la letra.

// Mostramos la longitud de la cadena 'miCadena' con LA PROPIEDAD length. el valor resultado es : 9
console.log("total length: "+miCadena.length);

//Recorremos con indice 'i' la posición de cada carácter 

for(i=0;i<=miCadena.length;i++){

//Mostramos en consola la posicion de cada carácter
console.log("posicion ["+i+"] Carácter ["+miCadena[i]+"]");
}

}

```
La salida en consola es como se muestra a continuación:

```
posicion [0] Carácter [M]
posicion [1] Carácter [i]
posicion [2] Carácter [ ]
posicion [3] Carácter [c]
posicion [4] Carácter [a]
posicion [5] Carácter [d]
posicion [6] Carácter [e]
posicion [7] Carácter [n]
posicion [8] Carácter [a]
posicion [9] Carácter [undefined]
```

Preste atención a la última columna "posicion[9]". Esto es así porque aunque la propiedad `length` nos mostró 9 posiciones, el for inicia en cero (0). Así que, si `for` cuenta desde cero (0) hasta 9, nos daría un total de 10 posiciones ya que el condicional evalua menor o IGUAL QUE, lo que lleva el recorrido a esta última posición. por ello la propiedad `length` nos deja una posicion de más, denominada `undefined`, pero en realidad es una posición en donde no encontró nada definido. En otros lenguajes se denomina NULL como "NADA" o fin de la cadena.

Por ello, en programación se determina que se debe declarar las posiciones reales de una longitud de cadena dada. Sabiendo esto, en la instrucción condicional del for restamos a esa longitud una posición, pero tambien podriamos, por el contrario solo evaluar en el paso de condición, solo con el signo MENOR QUE (<) y no habría neesidad de restar 1 a length.

### for(i=0 ; i<= `arreglo.length-1` ; i++)
###  o en su defecto...
### for(i=0 ; i< `arreglo.length` ; i++)



Ahora veamos como quedaría el codigo y su respectiva salida.

```javascript
function verCadena(cadena){

var miCadena= new String(cadena);
//El indice 'i' se utilizará para identificar la posición de columna de la letra.

//Primero mostramos la longitud
console.log("Total Length: "+miCadena.length);

//Recorremos la cadena (miCadena) con una posicion 
// menos (-1) que le restamos a la longitud.

for(i=0;i<=miCadena.length-1;i++){

//Ahora mostramos por consola el resultado

console.log("posicion ["+i+"] Carácter ["+miCadena[i]+"]");
}

}

verCadena("Mi cadena") //Llamamos la funcion
```

La salida:

```

Total Length: 9
posicion [0] Carácter [M]
posicion [1] Carácter [i]
posicion [2] Carácter [ ]
posicion [3] Carácter [c]
posicion [4] Carácter [a]
posicion [5] Carácter [d]
posicion [6] Carácter [e]
posicion [7] Carácter [n]
posicion [8] Carácter [a]

```




## * OPERADORES LOGICOS: `&&`, `||`, `!`

Son `Operadores Lógicos`; síntaxis que representan compuertas lógicas: `&&(AND), ||(OR), !(NOT).` 

Estas compuertas lógicas nos ayudan a determinar, en sentencias de condicionales compuestas (de dos o mas valores) `if(valor1===true && valor2 === true )` si se cumple como verdadereo o falso  cierta lógica. Estos valores pueden constituirse de dos o mas valores, y de diferentes tipos; cadena, númerico o Booleanos.

Ejemplo:

* Podemos crear una condicion para saber si estamos en verano, para ello determinaremos el mes en que estamos (expresado en números) y evaluaremos si està comprendido entre junio y septiembre(mes seis y nueve, respectivamente).

En realida tendremos que evaluar si el mes es mayor que 5, y ademas menor que 10. Dicho de otro modo, para que la condición resulte ser verdadera, deberá cumplirse: `(mes > 5) y (mes<10)`. Para ello uniremos varias condiciones mediante el operador lógico && (lease AND). Con esto se cumple una condición compuesta, si las dos se evaluan como verdaderas , es decir, si el mes es mayor que 5 y (AND) menor que 10.

Veamos como quedaría un trozo de código:

```javascript

// Denominemos la funcion 'esVerano', que a su vez recibe como 
// argumento un número del mes.

function esVerano(mes){

    // Evaluamos con if el número recibido...

    if(mes >  5 && mes < 10){//Si el mes está entre 6 Y 9...
        return "Es verano."; //retorna "Es verano"
    }
    else{return "No es Verano.";} //Si NO, retorna "No es verano"
}

```

