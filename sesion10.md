<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


<!-- Su documentación aquí -->
# Actividad: Prueba y ejecución de ejercicios de lógica de programación.
Prueba y ejecución de ejercicios de lógica de programación para mejorar las habilidades de resolución de problemas y pensamiento crítico.

## Ejercicios de Lógica de Programación
En esta actividad el profesor dejó unos ejercicios en la Sesión 10  y se eligió uno para explicar el funcionamiento del algoritmo. En mi caso se eligió el siguiente ejercicio: 

## 5. Calcular el movimiento rectilíneo uniforme
El movimiento rectilíneo uniforme (MRU) es un tipo de movimiento en el cual un objeto se mueve en línea recta y a velocidad constante, es decir, su velocidad no cambia en el tiempo. En este tipo de movimiento, la trayectoria del objeto es una línea recta, por lo que su aceleración es cero.

Un ejemplo común de MRU es un automóvil que se desplaza en una carretera recta y mantiene una velocidad constante durante todo el trayecto. Otro ejemplo es una pelota que cae verticalmente al suelo sin ser afectada por la resistencia del aire.

El MRU es un movimiento importante en la física, ya que permite entender conceptos básicos como la velocidad, la distancia recorrida y el tiempo de desplazamiento. Además, es utilizado como base para otros tipos de movimiento más complejos, como el movimiento rectilíneo uniformemente acelerado (MRUA) y el movimiento circular uniforme (MCU).

Ejemplo en Java de cómo calcular el movimiento rectilíneo uniforme:

```java
import java.util.Scanner;

public class MRU {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      double velocidad, tiempo, distancia;
      
      // Solicita la velocidad y el tiempo
      System.out.print("Ingrese la velocidad en metros por segundo: ");
      velocidad = input.nextDouble();
      System.out.print("Ingrese el tiempo en segundos: ");
      tiempo = input.nextDouble();

      // Calcula la distancia recorrida
      distancia = velocidad * tiempo;

      // Muestra el resultado en la consola
      System.out.printf("La distancia recorrida es de %.2f metros.", distancia);
   }
}
```

# Solución
La respuesta al analisis del algoritmo es la siguiente:

Primero se declaran las variables: velocidad, tiempo y distancia.
Luego el programa solicita al usuario que ingrese la velocidad en metros por segundo y el tiempo en segundos por consola y se guardan en sus respectivas variables (velocidad y tiempo) . Estos son los dos valores necesarios para calcular la distancia recorrida en un MRU.

Luego, el programa realiza el cálculo de la distancia recorrida multiplicando la velocidad ingresada por el tiempo ingresado. Ya que la formula es d = v * t

Finalmente, el programa muestra el resultado en la consola, formateando la distancia con dos decimales y mostrando el mensaje 

En resumen, este algoritmo permite calcular y mostrar la distancia recorrida por un objeto en un movimiento rectilíneo uniforme dado un valor de velocidad y un tiempo.






