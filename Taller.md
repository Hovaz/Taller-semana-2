# Taller-semana-2
desarrollo del taller semana 2

preguntas

P1: Hablando del IDE para desarrollar aplicaciones en C# (Xamarin o Visual Studio) ¿Cuál es la diferencia entre una solución, un proyecto y un ensamble?
Una solución es quien contiene los proyectos necesarios que se relacionan según se necesite, un proyecto es donde se desarrolla el programa y un ensamble es el .exe o .dll que sale del proyecto.

P2: Explique para qué sirve la línea using System en un programa en C#
Para definirle al compilador cuales bibliotecas va a utilizar.

P3: ¿Qué son y cuáles son los tipos de datos primitivos (o Built in) en C#?
Tipos de datos q se declaran para el uso o almacenamiento de datos

P4: ¿Cuál es la diferencia entre un tipo de datos unsigned / signed?
Los unsigned no almacenan datos negativos y sus rangos son más amplios en los positivos.
P5: Considere el siguiente código. ¿Funciona, no funciona? Explique
No porque el valor de la operación no se encuentra en el rango del sbyte

P6: ¿Cuál es la diferencia entre un tipo int y un tipo short? ¿Cuándo utilizar el uno o el otro?
P7: ¿Es posible hacer la siguiente asignación? explique su respuesta
ushort variable = 59485;

P8: En las siguientes expresiones, ¿Qué significan las letras al final de los literales?
double pi = 3.14159265358979323846;
float anotherPi = 3.1415926f;
long aBigNumber = 39358593258529L;
ulong bigOne = 2985825802805280508UL;
decimal number = 1.495m;

P10: ¿Para qué sirve la clase Convert?


P11: Indique la línea de código necesaria para escribir en la consola la cadena: 
Console.WriteLine("C:\\Users\\juanfh\\Desktop\\MiArchivo.txt");

12. la suma provoca que se desborde la variable y por eso no da el correcto

P15: ¿Una vez termine de ejecutarse la línea 12 cómo se determina que debe continuar en la línea 14?
En la 12 lee las instrucciones que se le dan, salta de línea para ejecutar la función, pero antes de saltar deja una nota o instrucción que le hace volver a la línea 12 una vez ejecuta la función
P16: El método addFive requiere un parámetro. Así mismo addFive devuelve un resultado. ¿En qué zona de memoria ocurre ese intercambio de información?
En el stack.

17. como es información que no necesita, el garbage collector limpia el heap

P18: en la siguiente línea de código, en relación con el heap y el stack:
string message = "Hello!";
¿En dónde queda la variable message?
En el stack.
¿En dónde queda la cadena “hello”?
En el heap.

P19: y en este caso, ¿En dónde queda almacenada cada cosa?
string[] messages = new string[3] { "Hello", "World", "!" };
messages en el stack, y el hello world ¡ se almacena en un arreglo que contiene todas sus direcciones en el heap.

P20: Y en este caso: 
int[] numbers = new int[3] { 2, 3, 4 };
El arreglo junto con sus valores se encuentra en el heap y el entero numbers en el stack.

P21: Muestre mediante dibujos del stack y el heap las siguientes variables:
string message = null;
int[] numbers = new int[] { 2, 4, 6, 8 };
numbers = null;

P22: ¿Qué valores tienen a y b luego de ejecutar este código?
int a = 3;
int b = a;
b++;
a = 3  y b = 4

23. 17, porque el cuándo el arreglo de b se iguala con a, lo que hace es guardar las mismas direcciones de a que ya tiene sus valores definidos, luego se cambia el primer valor utilizando la dirección de b y como es la misma que a cambia el primer valor de 1 por 17 y por ende imprime el ultimo.

24. 

25. para obtener acceso a los atributos de la case siempre que se necesiten

26. 
