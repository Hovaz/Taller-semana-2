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
Int puede almacenar un rango más alto de datos q el short, se utiliza según el rango de datos que se necesite almacenar

P7: ¿Es posible hacer la siguiente asignación? explique su respuesta
ushort variable = 59485;
si porque no exede el rango de datos.

P8: En las siguientes expresiones, ¿Qué significan las letras al final de los literales?
double pi = 3.14159265358979323846;
float anotherPi = 3.1415926f;
long aBigNumber = 39358593258529L;
ulong bigOne = 2985825802805280508UL;
decimal number = 1.495m;
Esa letra en la última parte de los números indica al compilador que el numero anterior será tratado como un long, ulong, float, etc.

P9: ¿Cuál es la razón por la cual al ejecutar la siguiente línea el programa se detiene?
string whatTheUserTyped = Console.ReadLine();
Por que espera el ingreso del usuario.

P10: ¿Para qué sirve la clase Convert?
Convierte un tipo base en otro.

P11: Indique la línea de código necesaria para escribir en la consola la cadena: 
Console.WriteLine("C:\\Users\\juanfh\\Desktop\\MiArchivo.txt");

P12: explique el comportamiento del siguiente programa
la suma provoca que se desborde la variable y por eso no da el correcto

P13: ¿Cuál es la diferencia entre las siguientes líneas de código?
línea 1: int[] scores
línea 2: int[] scores = new int[10];
En la primera se declara un arreglo y en la segunda se le asigna un tamaño.

P14: ¿Qué hace la siguiente línea de código?
int[] scores = new int[10] { 100, 95, 92, 87, 55, 50, 48, 40, 35, 10 };
Se declara un arreglo se le asigna un tamaño y se le asignan valores.

P15: ¿Una vez termine de ejecutarse la línea 12 cómo se determina que debe continuar en la línea 14?
En la 12 lee las instrucciones que se le dan, salta de línea para ejecutar la función, pero antes de saltar deja una nota o instrucción que le hace volver a la línea 12 una vez ejecuta la función

P16: El método addFive requiere un parámetro. Así mismo addFive devuelve un resultado. ¿En qué zona de memoria ocurre ese intercambio de información?
En el stack.

P17: ¿Qué pasa con el espacio creado en el HEAP? ¿Cómo se libera?
Como es información que no necesita el garbage collector limpia el heap

P18: en la siguiente línea de código, en relación con el heap y el stack:
string message = "Hello!";
¿En dónde queda la variable message?
En el stack.
¿En dónde queda la cadena “hello”?
En el heap.

P19: y en este caso, ¿En dónde queda almacenada cada cosa?
string[] messages = new string[3] { "Hello", "World", "!" };
etodas sus direcciones en el heap.

P20: Y en este caso: 
int[] numbers = new int[3] { 2, 3, 4 };
El arreglo junto con sus valores se encuentra en el heap y el entero numbers en el stack.

P21: Muestre mediante dibujos del stack y el heap las siguientes variables:
string message = null;
int[] numbers = new int[] { 2, 4, 6, 8 };
numbers = null;
stack
Mesage = null
Int[]
null
heap
{2,4,6,8}

P22: ¿Qué valores tienen a y b luego de ejecutar este código?
int a = 3;
int b = a;
b++;
a = 3  y b = 4

P23: Y en este caso
int[] a = new int[] { 1, 2, 3 };
int[] b = a;
b[0] = 17;
Console.WriteLine(a[0]);
¿Qué valor se imprime? explique

17 porque el cuándo el arreglo de b se iguala con a, lo que hace es guardar las mismas direcciones de a que ya tiene sus valores definidos, luego se cambia el primer valor utilizando la dirección de b y como es la misma que a cambia el primer valor de 1 por 17 y por ende imprime el ultimo.

P24: considere el siguiente código. Explique el resultado que se obtiene al ejecutarlo.
Myvalue y myvalue2 tiran un resultado de 4 ambos, lo que ocurre es que dentro de cada clase se llama la función y se le asigan a x y y la misma dirección por tanto al inicio en ambos casos el resultado es 3 pero cuando a y se le iguala a 4 se cambia ya que tanto y como x guardan la misma dirección en es stack.

P25: ¿Por qué razón el constructor es público? ¿El constructor debe tener el mismo nombre de la clase?
Para obtener acceso a los atributos de la case siempre que se necesiten.

P26: ¿El código que se muestra funciona?
No, porque X = -5 está fuera de contexto, es decir, x es una variable que se declara y usa dentro del ciclo for y por tanto al no estar dentro del for el compilador no entiende el x = -5 y no permite ejecutar el programa.


Retos

C1: Escriba un programa que le informe al usuario el volumen y el área de un cilindro rectangular recto luego de solicitar el radio y la altura del cilindro.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace holi
{
    class Program
    {
        static void Main(string[] args)
        {
            double a, r, area, volumen;
            string altura, radio;
            Console.WriteLine("porfavor ingrese el radio del cilindro");
            radio = Console.ReadLine();
            Console.WriteLine("porfavor ingrese la altura del cilindro");
            altura = Console.ReadLine();

            if ((double.TryParse(radio, out r)) && (double.TryParse(altura, out a))) 
            {
                area = (2 * Math.PI * r) * (a + r);
                volumen = (Math.PI)*(r*r)*(a);
                Console.WriteLine("el area del cilindro es = " + area);
                Console.WriteLine("el volumen del cilindro es = " + volumen);
                Console.ReadKey();

                //Console.WriteLine("C:\\Users\\juanfh\\Desktop\\MiArchivo.txt");
(prueba p11)

            }

        }
    }
}


C2: escriba un programa que imprima en consola las siguientes operaciones:
int a = 7;
int b = 2;
float c = 4;
float d = 3;
float result = a / b + c / d;

¿El resultado es el que usted esperaba? en caso contrario, ¿Qué correcciones debe realizar al programa para que funcione como es de esperar (sin cambiar las declaraciones de a,b,c y d)?

el resultado es 4.3 cuando debería ser 4.8, para que funcione es necesario que los int sean considerados como float en la suma así:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace c2
{
    class Program
    {
        static void Main(string[] args)
        {
            int a = 7;
            int b = 2;
            float c = 4;
            float d = 3;
            float result = (float)a / (float)b + c / d;

            Console.WriteLine(result);
            Console.ReadKey();
        }
    }
}

C3: Realice un programa que encuentre los valores máximo y mínimos del arreglo { 4, 51, -7, 13, -99, 15, -8, 45, 90 }; utilizando Foreach loop.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace c3
{
    class Program
    {
        static void Main(string[] args)
        {
            int[] numero = new int[]{ 4, 51, -7, 13, -99, 15, -8, 45, 90 };
            int Mayor = 0, Menor = 0, n = 0;

            foreach (int element in numero)
            {
                if (element < Menor)
                {
                    Menor = element;
                }
                if (element > Mayor)
                {
                    Mayor = element;
                }
            }
            Console.WriteLine("El mayor es = "+ Mayor);
            Console.WriteLine("El menor es = "+ Menor);
            Console.ReadKey();


        }
    }
}

