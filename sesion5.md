<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 


<!-- Su documentación aquí -->
# Actividad 5: Ejercicios de bucles 
Resolver los siguientes ejercicios:

## Ejercicios - while
1. Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.
2. Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.

## Ejercicios - do while
1. Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.
2. Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.

## Ejercicios - for
1. Imprimir los números impares del 1 al 50.
2. Imprimir los números primos del 1 al 100.


# Solución 

## Ejercicios con While:
### Ejercicio 1

```java
import java.util.Scanner;
/**
 * Relizado por: Carlos Andrés Sánchez Correa
*/ 
public class Ejer1while{

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Ingrese un número entero: ");
        int num = input.nextInt();
        int i= 0;
        int mult;

        while (i <= 10) {
            mult = num * i;
            System.out.println(num+" X "+i+" = "+mult);
            i++;
        }

        input.close();
    }
}
```

### Ejercicio 2

```java
import java.util.Scanner;
/**
 * Relizado por: Carlos Andrés Sánchez Correa
*/ 
public class Ejer2while {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Ingrese un texto: ");
        String texto = input.nextLine();
        int i = 0;
        int cantNumeros = 0;

        while (i < texto.length()) {
            char caracter = texto.charAt(i);
            if (caracter == '1' || caracter == '2' || caracter == '3' || caracter == '4' || caracter == '5' || caracter == '6' || caracter == '7' || caracter == '8' || caracter == '9' || caracter == '0'  ) {
                cantNumeros++;
            }
            i++;
        }
        System.out.println("El texto ingresado contiene "+cantNumeros+" número(os)");

        input.close();
    }
}

```


## Ejercicios con Do-While:
### Ejercicio 1

```java
import java.util.Scanner;
/**
 * Relizado por: Carlos Andrés Sánchez Correa
*/ 
public class Ejer1dowhile {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        int num;

        do {
            System.out.print("Ingrese un número (ingrese un número negativo para detener): ");
            num = input.nextInt();

            while (num >=0 && num <= 99) {
                num +=1;
                System.out.println("Número: "+num);
            }
        } while (num >= 0);

        System.out.println("Finaliza el programa");

         input.close();
    }
}

```

### Ejercicio 2

```java
import java.util.Scanner;
/**
 * Relizado por: Carlos Andrés Sánchez Correa
*/ 
public class Ejer2dowhile {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        int num;
        int i =0;

        do {
            System.out.print("Ingrese un número entero (0 para detener): ");
            num = input.nextInt();

            if (num != 0) {
                System.out.println("Tabla de multiplicar del "+num+" : ");

                while(i <= 10){
                    int resultado = num * i;
                    System.out.println(num+" X "+i+" = "+resultado);
                    i++;
                }
                i=0;
            }

        } while (num != 0);
        System.out.println("Fin del programa");

        input.close();
    }
}

```


## Ejercicios con For:
### Ejercicio 1 

```java
/**
 * Relizado por: Carlos Andrés Sánchez Correa
*/ 

public class Ejer1for {
    public static void main(String[] args) {
        for (int num = 1; num <= 50; num+=2) {
            System.out.println(num);
        }
    }
}

```

### Ejercicio 2

```java
/**
 * Relizado por: Carlos Andrés Sánchez Correa
*/ 

public class Ejer2for {
    public static void main(String[] args) {
       
        boolean primo;
        System.out.println("Son números primos del 1 al 100:\n");
        
        for (int num = 2; num <= 100; num++) {
            primo = true;
            for (int i = num - 1; i > 1; i--) {
                if (num % i == 0) {
                    primo = false;
                    break;
                }
            }
            if (primo) {
                System.out.println(num);
            }
        }
    }
}

```







