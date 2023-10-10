<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 11 


<!-- Su documentación aquí -->
# Actividad: Ejercicios de Lógica de Programación
1. Basándose en el algoritmo 1 de la sesión 11, aplicar la siguiente variante: Dado un conjunto de números enteros, se debe determinar si existe algún número que aparezca más de una vez. Si es así, se deben imprimir todos los números que aparezcan más de una vez.

Ejercicio 1 (original).
```java
public class EjercicioFinal {

    public static void main(String[] args) {
        // Declaramos un conjunto de números enteros
        int[] numeros = {1, 2, 3, 4, 5, 2};

        // Creamos una variable para almacenar el número que aparece más de una vez
        int numeroRepetido = 0;

        // Recorremos el conjunto de números
        for (int i = 0; i < numeros.length; i++) {
            // Comprobamos si el número actual ya ha aparecido
            for (int j = 0; j < i; j++) {
                if (numeros[i] == numeros[j]) {
                    // El número actual ya ha aparecido
                    numeroRepetido = numeros[i];
                    break;
                }
            }
        }

        // Si el número repetido es distinto de 0, lo imprimimos
        if (numeroRepetido != 0) {
            System.out.println("El número repetido es: " + numeroRepetido);
        } else {
            // No hay ningún número repetido
            System.out.println("No hay ningún número repetido");
        }
    }
}
```

1. Desarrollar un algoritmo que realice la conversión de binario a decimal.

Ejercicio 2 (original).
```java
public class DecimalABinario {

    public static void main(String[] args) {
        // Declaramos la variable para almacenar el número decimal
        int numeroDecimal = 10;

        // Declaramos la variable para almacenar el resultado
        String numeroBinario = "";

        // Inicializamos el bucle
        for (int i = numeroDecimal; i > 0; i /= 2) {

            // Calculamos el resto de la división
            int resto = i % 2;

            // Añadimos el resto a la cadena
            numeroBinario = resto + numeroBinario;
        }

        // Imprimimos el resultado
        System.out.println("El número binario es: " + numeroBinario);
    }
}
```

# Solución

Ejercicio 1 (variante)

El siguiente algoritmo si permite que me muestre si hay dos o más números repetidos, ya que el original solo permitía mostrar solo un número repetido (el ultimo que se ingresaba)

```java
import java.util.Set;
import java.util.HashSet;

public class EjercicioFinal {

    public static void main(String[] args) {
        // Declaramos un conjunto de números enteros
        int[] numeros = { 1, 2, 3, 4, 5, 2, 3 };

        // Creamos un conjunto para almacenar los números repetidos
        Set<Integer> numerosRepetidos = new HashSet<>();
        Set<Integer> numerosUnicos = new HashSet<>();

        // Recorremos el conjunto de números
        for (int numero : numeros) {
            if (!numerosUnicos.add(numero)) {
                // El número ya está en el conjunto de números únicos, por lo tanto es repetido
                numerosRepetidos.add(numero);
            }
        }

        // Si hay números repetidos, los imprimimos
        if (!numerosRepetidos.isEmpty()) {
            System.out.println("Los números repetidos son: " + numerosRepetidos);
        } else {
            // No hay ningún número repetido
            System.out.println("No hay ningún número repetido");
        }
    }
}
```

Ejercicio 2 (variante)

El siguiente ejercicio me perimite con vertir un número binario a un decimal, ya que el original solo lo hacia al contrario (decimal a binario)

```java
public class EjercicioBinarioaDecimal {

    public static void main(String[] args) {
        // Declaramos la variable para almacenar el número binario
        String numeroBinario = "1010";

        // Declaramos la variable para almacenar el resultado
        int numeroDecimal = 0;

        // Inicializamos el bucle
        for (int i = 0; i < numeroBinario.length(); i++) {
            // Obtenemos el dígito en la posición i
            int digito = Character.getNumericValue(numeroBinario.charAt(i));

            // Calculamos el valor correspondiente al dígito en la posición i
            int valor = digito * (int) Math.pow(2, numeroBinario.length() - 1 - i);

            // Sumamos el valor al número decimal
            numeroDecimal += valor;
        }

        // Imprimimos el resultado
        System.out.println("El número decimal es: " + numeroDecimal);
    }
}
```






