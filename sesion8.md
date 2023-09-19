<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


<!-- Su documentación aquí -->

# Actividad: Ejecicios de métodos en Java
Implementar los siguientes métodos:

1. Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.
2. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.
3. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.
4. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.
5. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.


# Solución

**Ejercicio 1:**

```java
import java.util.Scanner;

public class EjerMetodos1{
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Ingrese un Número: ");
        int n1 = input.nextInt();

        System.out.print("Ingrese otro Número: ");
        int n2 = input.nextInt(); 
        
        int mayor = numeroMayor(n1, n2);
        System.out.println("El número mayor es: "+mayor);

        input.close();
        
    }

    public static int numeroMayor(int num1, int num2){
        if(num1 > num2){
            return num1;
        }else{
            return num2;
        }
   }
}
```

**Ejercicio 2:**

```java
import java.util.Scanner;

public class EjerMetodos2 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Ingrese un texto: ");
        String cadena = input.nextLine();

        int vocales = numeroVocales(cadena);
        System.out.println("El número de vocales es: "+vocales);

        input.close();
    }

    public static int numeroVocales(String texto){
        texto = texto.toLowerCase(); //convierte todo el texto a minusculas

        int contador = 0;
        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
            if (caracter == 'a' || caracter == 'e' || caracter == 'i' || caracter == 'o' || caracter == 'u') {
                contador++;
            }
        }
        return contador;
    }
}

```

**Ejercicio 3:**

```java
import java.util.Scanner;

public class EjerMetodos3 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Ingrese un texto: ");
        String texto = input.nextLine();

        String cambio = cambioMayusculaMinuscula(texto);
        System.out.println("El cambio es: "+cambio);

        input.close();
    }


    public static String cambioMayusculaMinuscula(String cadena){
        // Creamos un StringBuilder para construir la nueva cadena
    StringBuilder resultado = new StringBuilder();

    // Recorremos la cadena original
    for (int i = 0; i < cadena.length(); i++) {
        char caracter = cadena.charAt(i);

        // Verificamos si el carácter es mayúscula
        if (Character.isUpperCase(caracter)) {
            
            resultado.append(Character.toLowerCase(caracter)); // Si es mayúscula, lo convertimos a minúscula y lo agregamos al resultado
        } else if (Character.isLowerCase(caracter)) {
           
            resultado.append(Character.toUpperCase(caracter));  // Si es minúscula, lo convertimos a mayúscula y lo agregamos al resultado
        } else {
            
            resultado.append(caracter); // Si no es una letra, simplemente lo agregamos al resultado
        }
    }

    
    return resultado.toString();
    }
}

```

**Ejercicio 4:**

```java
import java.util.Scanner;

public class EjerMetodos4 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Ingrese una o varias palabras: ");
        String cadena = input.nextLine();

        int cantPalabras = numeroPalabras(cadena);
        System.out.println("El número de palabras que contiene es: "+cantPalabras);

        input.close();
    }

    public static int numeroPalabras(String texto) {
        // Dividir la cadena en palabras usando espacios en blanco como separadores
        String[] palabras = texto.split("\\s+"); //el método split("\\s+")para dividir la cadena en palabras. El argumento "\\s+"es una expresión regular que representa uno o más espacios en blanco

        // Contar y devolver el número de palabras
        return palabras.length;
    }
}

```

**Ejercicio 5:**

```java
import java.util.Arrays;
import java.util.Scanner;

public class EjerMetodos5 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Ingrese varias palabras separadas con espacio: ");
        String cadena = input.nextLine();

        String orden = ordenAlfabeticoPalab(cadena);
        System.out.println("Las palabras en orden alfabetico quedan: "+orden);

        input.close();

    }

    public static String ordenAlfabeticoPalab(String texto) {
        // Dividir la cadena en palabras usando espacios en blanco como separadores
        String[] palabras = texto.split("\\s+");

        // Ordenar el arreglo de palabras
        Arrays.sort(palabras);

        // Unir las palabras ordenadas en una sola cadena
        String resultado = String.join(" ", palabras);

        return resultado;
    }
}

```




