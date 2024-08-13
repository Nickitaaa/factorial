El factorial de un número entero positivo se define como el producto de todos los números naturales anteriores o iguales a él.

¿Que es la funciòn factorial?

La función factorial se representa con un signo de exclamación “!” detrás de un número. Esta exclamación quiere decir que hay que multiplicar todos los números enteros positivos que hay entre ese número y el 1.

![image](https://github.com/user-attachments/assets/e0d585de-0a41-4b4f-a5a3-bc2ad36e4409)

Factorial en Kotlin:

fun factorial(n: Int): Long 

{

if (n <= 1)

{ return 1

} return n factorial(n-1)

} fun main()

{

val number 5

println("El factorial de numer es {factorial(number)}")

}

Este codigo en Kotlin calcula el factorial de un numero utilizando recursividad.

Funcion Factorial:

fun factorial(n: Int): Long{

Condicion Base: 

if (n <= 1) { return 1 }

Llamada recursiva:

return n * factorial(n-1)

Funcion Main:

fun main() {

val number - 5

println("El factorial de Snumber es {factorial(number)}")


Lenguajes Funcionales:

Los lenguajes funcionales priorizan el uso de recursividad y aplicación de funciones de orden superior para resolver problemas que en otros lenguajes se resolverían mediante estructuras de control.

Caracteristicas:

A lo largo de las implementaciones de los modelos anteriormente comentados, cada paradigma fue definiendo una serie de peculiaridades. Así las características que definen al paradigma funcional hoy por hoy son las siguientes:

    No hay estado global.
    Todas las funciones son puras: Dado un mismo input siempre devolvemos el mismo output.
    Todos los valores son inmutables: Lo único que podemos hacer es generar nuevos valores.
    No hay bucles: La iteración se realiza usando recursividad.

Como el modelo de cálculo lambda carecía de “cinta” para conservar el estado del programa, este se tenía que ir regenerando a través de la composición de funciones y la recursividad.

Un buen ejemplo de cómo podemos crear cualquier cosa usando funciones es la lógica combinatoria, una variante del cálculo lambda que provee un set limitado de funciones combinadoras
 
// funciones combinadoras

const I = x => x;
const K = x => y => x;
const V = x => y => z => z(x)(y);

// implementación de una tupla
const first = I;
const second = K(I);
const tuple = V;

const myTuple = tuple('Hello')('World');
myTuple(first); // 'Hello'
myTuple(second); // 'World'

Cumpliendo las características arriba comentadas hemos implementado una tupla básica usando solo funciones.

Los combinadores son excelentes ejemplos de programación funcional y están presentes hoy en día más de lo que creemos. Por ejemplo, la famosa aceleradora de startups de capital riesgo estadounidense Y combinator, toma el nombre el combinador ‘Y’ de lógica combinatoria.

Además, según la implementación, el paradigma de programación funcional también se suele asociar a lo que en teoría de programación se conoce como “lazy evaluation” o evaluación perezosa. Esta estrategia de evaluación que implementan lenguajes como Haskell consiste en no evaluar ninguna expresión hasta que el valor se necesite realmente. Así podemos definir estructuras de datos infinitas que por lo general hacen más sencilla la implementación de ciertos algoritmos.

Por ejemplo, si quisiéramos representar en una lista todo el conjunto de los números naturales usando Haskell, podríamos hacer esto:

n = [0..] -- lista infinita representando todos los numeros naturales
doubles = map (*2) n -- doblamos todos los numeros naturales






