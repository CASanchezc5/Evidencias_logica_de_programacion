<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 3 


<!-- Su documentación aquí -->
# Actividad 3: Ejercicios de operaciones básicas en Java.  
1. Suma y multiplicación: Escribe un programa que solicite al usuario dos números enteros y luego imprima la suma y multiplicación de esos números.

2. Resta y división: Escribe un programa que tome dos números enteros ingresados por el usuario y calcule la resta y división de esos números.

3. Operaciones combinadas: Escribe un programa que solicite al usuario tres números enteros y realice las siguientes operaciones: suma de los tres números, multiplicación del primer número por el segundo y división del resultado entre el tercer número.

4. Operaciones con decimales: Escribe un programa que solicite al usuario dos números decimales y realice las siguientes operaciones: suma, resta, multiplicación y división.

5. Incremento y decremento: Escribe un programa que declare una variable entera y la inicialice con un valor. Luego, incrementa su valor en 1 y muestra el resultado. Después, decrementa su valor en 1 y muestra el resultado nuevamente.

6. Operador de asignación compuesta: Escribe un programa que declare una variable entera y la inicialice con un valor. Utiliza el operador de asignación compuesta para sumar 5 a la variable y luego mostrar su valor.

7. Operadores lógicos: Escribe un programa que tome dos valores booleanos ingresados por el usuario y muestre el resultado de las operaciones lógicas AND, OR y NOT entre esos valores.

8. Operador ternario: Escribe un programa que tome un número entero ingresado por el usuario y utilice el operador ternario para determinar si el número es positivo o negativo. Luego, muestra el resultado en la salida.



# Solución 

## Ejercicio 1:
```java
import java.util.Scanner;

public class Ejercicio1{
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Ingrese un número entero: ");
        int num1 = input.nextInt();

        System.out.print("Ingrese otro número entero: ");
        int num2 = input.nextInt();

        int suma = num1 + num2;
        int mult =  num1 * num2;

        System.out.println("El resultado de la suma es: "+suma);
        System.out.println("El resultado de la multiplicación es: "+mult);

        input.close();
    }
}
```

## Ejercicio 2:
```java
import java.util.Scanner;

public class Ejercicio2 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Ingrese un número entero: ");
        int num1 = input.nextInt();

        System.out.print("Ingrese otro número entero: ");
        int num2 = input.nextInt();

        int resta = num1 - num2;
        double division = (double) num1 / num2;

        System.out.println("El resultado de la resta es: "+resta);
        System.out.println("El resultado de la división es: "+division);

        input.close();  
        
    }
}

```

## Ejercicio 3:
```java
import java.util.Scanner;

public class Ejercicio3 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Ingrese el 1er número entero: ");
        int num1 = input.nextInt();

        System.out.print("Ingrese el 2do número entero: ");
        int num2 = input.nextInt();

        System.out.print("Ingrese el 3er número entero: ");
        int num3 = input.nextInt();

        int suma = num1 + num2 + num3;
        int mult = num1 * num2;
        double division = (double) mult / num3;

        System.out.println("El resultado de la suma es: "+suma);
        System.out.println("El resultado de la multiplicación es: "+mult);
        System.out.println("El resultado de la división es: "+division);

        input.close();
    }
}

```

## Ejercicio 4:
```java
import java.util.Scanner;

public class Ejercicio4 {
   public static void main(String[] args) {
    Scanner input = new Scanner(System.in);

    System.out.print("Ingrese el 1er número entero: ");
    float num1 = input.nextFloat();

    System.out.print("Ingrese 2do número entero: ");
    float num2 = input.nextFloat();

    float suma = num1 + num2;
    float resta = num1 - num2;
    float mult = num1 * num2;
    float division =  num1 / num2;

    System.out.println("El resultado de la suma es: "+suma);
    System.out.println("El resultado de la resta es: "+resta);
    System.out.println("El resultado de la multiplicación es: "+mult);
    System.out.println("El resultado de la división es: "+division);

    input.close();   
    
   } 
}

```

## Ejercicio 5:
```java
public class Ejercicio5 {
    public static void main(String[] args) {
        
        int numero = 5;

        numero += 1;
        System.out.println("Incremento: "+numero);

        numero -= 1;
        System.out.println("Decremento: "+numero);
    }
}

```

## Ejercicio 6:
```java
public class Ejercicio6 {
    public static void main(String[] args) {
        
        int numero = 10;

        numero += 5;
        System.out.println(numero);
    }
}

```

## Ejercicio 7:

```java
import java.util.Scanner;

public class Ejercicio7 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Ingrese un valor booleano (true o false): ");
        boolean valor1 = input.nextBoolean();

        System.out.print("Ingrese otro valor booleano (true o false): ");
        boolean valor2 = input.nextBoolean();

        boolean resultado1 = valor1 && valor2;
        boolean resultado2 = valor1 || valor2;
        boolean resultado3 = !valor1;
        boolean resultado4 = !valor2;
        boolean resultado5 = (valor1 && valor2) || (!valor1 && valor2);

        System.out.println("Esta es la respuesta del resultado 1 con AND: "+resultado1);
        System.out.println("Esta es la respuesta del resultado 2 con OR: "+resultado2);
        System.out.println("Esta es la respuesta del resultado 3 con NOT: "+resultado3);
        System.out.println("Esta es la respuesta del resultado 4 con NOT: "+resultado4);
        System.out.println("Esta es la respuesta del resultado 5, combinados: "+resultado5);

        input.close();

    }
}

```

## Ejercicio 8:
```java
import java.util.Scanner;

public class Ejercicio8 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Ingrese un número entero: ");
        int num = input.nextInt();

        String tipoNumero = (num >= 0) ? "Es positivo" : "Es negativo";//aqui incluyo el 0 como positivo pero es un número neutro

        System.out.println(tipoNumero);

        input.close();
    }
}

```






