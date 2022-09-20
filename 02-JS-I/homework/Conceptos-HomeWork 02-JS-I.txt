HomeWork 02-JS-I Conceptos.txt
1. En un archivo de texto separado que debes crear, escribe explicaciones de los siguientes conceptos como si se lo estuvieras explicando a un niño de 12 años. Hacer esto te ayudará a descubrir rápidamente cualquier agujero en tu comprensión.

 * Variables:
Concepto Técnico: Es una zona en memoria de ordenador o PC donde se guarda un dato (a-z,0-9...)y que se identifica con un nombre; cuando un "dato" se guarda bajo un "nombre" se denomina "Pares nombre-valor". Las variables pueden se de diferentes tipos; Cadenas (Strings), Numérico (Enteros y Decimales), Fecha (Date) ...

Concepto Didáctico: Es como una Cajita en la que uno guarda un contenido; la cajita tendría un nombre o le ponemos un nombre ej. "Caj1" o "Variable1", y el contenido sería su valor al que podremos tener acceso.
La Cajita puede tener un contenido al que podríamos "agregar" otro valor o también se podría "cambiar" por otro contenido (valor); perdiéndose el contenido anterior.

 * Strings
Concepto Técnico: Es un "Tipo de Dato" denominado Cadena de caracteres o Literales. Este se identifica porque contiene más de un caracter o más de una letra o conjunto de letras; palabras, frases, oraciones... También pueden ser alfanúmerico (a-z, 0-9) y carácteres especiales pero con un atenuante que deben ir declarados entre comillas ("", '') todos.

Concepto Didáctico: Son aquellas palabras, o conjunto de palabras que pueden formar oraciones o información literal. Un String se denomina como "Cadenas de caracteres", mientras que un caracter puede ser un simbolo (@), una letra(a-z) o un número(0-9), los String están formados por un conjunto de ellos.

Para que el ordenador pueda diferenciar e identificar una cadena de caracteres(String) o literales, esta debe ir encerradas entre comillas dobles ("").
ej.
variable1 = "esto es una cadena de caracteres";
variable2 = "0, 1, 2 ...9";
variable3 = "@, /, # ...";

El ejemplo anterior nos muestra 3 Cajitas (variable1, variable2, variable3) ó nombre, y con su respectivo contenido (valores entre comillas dobles).

El signo igual (=) -denominado tambien de asignación- nos indica que podemos guardar el valor (String) en su respectiva cajita, a esto le llamamos asignar un valor a una variable; inicializar una variable de tipo String (en este caso).


 * Funciones (argumentos, `return`)
Concepto técnico: Es un conjunto de instrucciones o bloque que encierra instrucciones que cumplen una acción determinada. Puede ser llamada o invocada para ejecutar y resolver una acción. Esta también, se carga en memoria pero no es ejecutada hasta que sea invocada desde otra parte del código.
Al crear una función, se hace nombrando la palabra reservada "function"(JavaScript) seguida del nombreObjetivo de la función (formato eg. sumaValores) (Lo que hace la función).

En matemáticas recordaremos que la funcion f(x)= x+2, por ejemplo, espera un valor(argumento) x para poder resolver dentro la suma. Asi mismo, podemos entender una función en programación, en este caso solo tiene una linea de instruccion, pero podemos encontrar funciones con mucho mas lineas que se ejecutan para cumplir un objetivo, en este caso una suma (x+2).

Concepto Didáctico:
Una funcion lo puedes comparar a la cocina de tu casa. 
Ahora, todo depende de tu objetivo a comer (Desayuno, almuerzo, Cena).
Supongamos que quieres desayunar huevos fritos. La receta lleva: huevo, sal, aceite... dejemoslo hasta ahí, pues te gusta así.

Entras a tu casa y pides(invocas) este plato. Para que cumpla con tu deseo la cocina de tu casa debe tener estos ingredientes, en ese caso se los entregas. Una vez pasado cierto tiempo està listo, puesta en tu mesa. ¿Bien hasta aqui?

Ahora bien, llevemos esta analogía a una función. denominemos nuestra función "cocinarPlato" este sería el nombre de un area de la casa (mas exactamente en la cocina de la casa). La cocina "cocinarPlato" tiene dentro una alacena(serian los parentesís de apertura y cierre) con cajitas o recipientes (Son los argumentos: nombres de las Variables) a estas cajita las nombraremos: ing1, ing2, ing3. Asi quedaría declarada la función:

cocinarPlato(ing1, ing2, ing3...)

Ya que tenemos la cocina lista, ahora requiere que el entreguemos los ingredientes.
Dentro de estas cajitas guardaras o recibira los ingredientes como tal. 

En este caso los pasamoss estos igredientes  declarando anticipadamente lo que deseas desayunar. a este paso le denominamos "incializar las variables o argumentos" Esto valores  serían: El huevo, La sal, El aceite; como ingredientes.

ing1="Huevos", ing2="Tomate", ing3="Sal", ing4="Cebolla";

Lo que sería igual entregarlos a quien va a cocinar.

Asi ya la funcion "cocinarPlato" tiene lo necesarios para empezar a prepararlos.
ahora, cómo es la preparación?
A ella nos referiremos como un "bloque de código" que tendrá varias líneas donde se expresa como se va a preparar el desayuno. Este bloque de código debe ir encerrado entre llaves ({}). entonces nuestra función quedaría algo similar a esto:

function cocinarPlato(ing1, ing2, ing3){
//Bloque de codigo
//Linea 1 
//...
//n lineas
return huevosFritos;
}

El bloque de código vendría siendo todos los procesos que realiza el cocinero para prepararlos entre ellos:

-Prender estufa //linea1
-poner recipiente...
-agrear aceite y calentar lo suficiente...
-romper el huevo en recipiente...
-*Esperar 5 min a fuego lento...
-retirar huevo frito...
-Servir(retorna) Huevo frito con sal...//Linea8 
*

Todas estas lineas se dan para cumplir ese objetivo. Ahora, centrémonos en la última linea. En ella vemos otro punto importante de la función, lo cual se denomina "servir"; el resultado de preparar el desayuno. A este proceso le denominamos "return". ese proceso lo realiza el(la) cociner@ cuando saca de la cocina el plato terminado para ser entregado en la mesa o a la persona que lo requirió. Así que podríamos decir en vez de "Servir" retornar o "return".

En síntesis: La casa es el Software o Aplicación, dentro de esta una persona invoca, llama o pide a la cocina, denominada cocinarPlato, un huevo frito. A esta cocina le entrega los ingredientes o valores que retiene dentro de unos recipientes o argumentos mientras empieza a preparar o procesar un bloque de código con los paso a paso o lineas que preparan y cumplen el objetivo de entregar o retornar el plato pedido "huevo frito".

Notaciones importantes:
Una función en javascript puede no tener un nombre lo cual se denomina "Funciones Anónimas" pero si es preciso que se declare como function y al final llevar parentesís de apertura y cierre.
Una función puede llevar o no argumentos, pero si queremos acceder a su resultado debemos dictarle al final de su codigo un retorno de este por medio de la palabra reservada "return".
Una función en JavaScript cumple con cualidad propia de la función denominada "scope" o alcance del valor de las variables, esto es: Todo variable declarada dentro de la función solo es accesible dentro de ella. Si existiera una variable denominada igualmente fuera de ella, al ser requerida o usada solo mostrara su valor global mas no la que procede dentro del bloque de código de la función. A esta última solo accederemos a su valor mediante la palabra reservada "return".

 * Declaraciones `if`
 Concepto Técnico: Es una instrucción que evalua una o más condiciones y, en virtud de que resulten verdaderas o falsas, ejecuta distintos bloques de código.
 Esto es: Se comprueba primero si unacondición se cumple. En caso afirmativo o true, ejecuta su correspondiente código, pero si no se cumple pasará a otro bloque de código diferente.

 Concepto Didáctico: Cuando una persona quiere viajar a otra ciudad lo puede hacer por via terrestre o por via aerea.
 Todo depende del tiempo que quieras gastar; si es tienes tiempo suficiente irìas por tierra asi disfruta del paisaje mas de cerca.
 pero si por el contrario no tienes tiempo suficiente te iras por via aerea.
 
 De esta maner podríamos traducir un if con sus repectivas condiciones en este caso sería "El Tiempo de viaje"
Iniciamos la variable "transporte" en Blanco para poder guardar en ella la decisión final del transporte a tomar.
var transporte = " ";

Definiremos el tiempo que se tiene disponible y lo iniciamos en 2 horas
var tiempoDisponible= 2;

Definiremos e iniciamos una variable que nos dicte el tiempos que toma el transporte en llevarnos de una ciudad a otra.
var tiempoViaje=4; 

Ahora veremos en virtud del tiempo de viaje y el tiempo disponible que decisión tomar.
esto es: 
Si el tiempo disponible es mayor o igual que el tiempo de viaje...

if(tiempoDisponible >= tiempoViaje)

entonces... el if evalua si es cierto (true) o falso (false)
en caso de ser true ejecutaria el codigo adyacente entre corchetes así:

if(tiempoDisponible >= tiempoViaje){transporte = "Transporte Terrestre" console.log("Viajar por: "+transporte;}

Llegado a esta parte la decisión a tomar e viajar por via terrestre, por tanto la variable transporte tomará el valor correspondiente "Transporte terrestre",
Seguido el código entre corchetes al final se mostrará en consola la respuesta o el valor que contiene la variable transporte.

Si la condicion anterior no se cumple (si nó: else) se ejecutará otro bloque de código que mostrará el otro tipo de viaje "Aereo".

else {transporte = "Transporte Aereo" console.log("Viajar por: "+transporte;}


 * Valores booleanos (`true`, `false`)
Concepto técnico: Son variables que contiene valores que contiene un valor binario; que poseen dos posibles estados: verdadero(true) o falso (false)
Las variables booleanas se declaran o se inicializan de la misma forma que cualquier otra variable, con la diferencia que solo puden recibir uno de los dos valores mencionados anteriormente.

Así como las computadoras internamente se guían para poder identificar los datos a nivel electrónico  por las logitudes de onda de energia, donde pueden definirse en un rago de 0 a 1 donde toda energía entre 0 y 4,9 podría definirlo como cero (0) y toda energía que este en el rango 0.5 a 1 puede interpretarse como un uno (1) lógico.
de esta manera exisen sentencias en las que se define un true como un 1 lógico y u false como un cero(0).

Concepto Didáctico: Imagina que tienes un vaso medidor transparente rotulado por un costado y en sentido vertical de esta manera:
En su base tiene rotulado el número cero (0) a mitad del vaso con una linea horizontal el número 2.5 indicn la mitad de este y en su borde superior igualmente rotulado por un número 5.

Ahora empezamos a llenar el vaso con un liquido que hay contenido en una jarra. No sabemos que tanto tiene.
Una vez desocupamos en el vaso su contenido este llega mas de 2 pero un poco menos de 5.

Muy bien, ahora preguntamos: ¿Esta suficientemente lleno el vaso?
Podríamos decir que Sí. esa repuesta es afirmativa, Verdadera (true) pues está lejos de estar suficientemente vacio o casi sin contenido.
Caso contrario que no podría decir si el coontenido estuviera en 1 un poco por debajo de 1, en ese caso estaría suficientemente vacio, por ello la respuesta sería 
lo contrario; No, Negativo, Falso (false).

Se tendría que tomar una decisión de acuerdo a la circunstancia del vaso medidor.

Solo puede tomar un valor inclusive aún si estuviera exactamente en 1.5 porque ello representaria en 
determinar si la regla a ello aceptaria un true o false, pero siempre se tomará una decisión de acueerdo a la regla.


En arquitectura de ordenadores (Compuertas Lógicas) se toma como un 1 lógico, de acuerdo a la tecnológia, todo valor en un rnao que va desde 2v hasta 5v pues no hay ausencia de energía en ese punto y es mas probable que altere un código de bits.
Pero en cambio al ausencia de voltaje està dada por las reglas de acuerdo a las diferentes tecnologias de compuertas lógicas, por ello su rano va desde 0v o ausencia hasta 1v.



 ____________________________________________________
 * Solo se menciona algunas lineas de código, podrían ser más en detalle.
