<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 7 


<!-- Su documentación aquí -->
# Actividad: Ejecicios Array - ArrayList 
## 1. En parejas, probar, analizar y explicar el funcionamiento de los siguientes ejemplos de Array y ArrayList.

Ejemplo Array

```java
import java.util.Arrays;

public class EjercicioArray {

    public static void main(String[] args) {
        // Crear un array de números enteros
        int[] numeros = {5, 2, 10, 7, 1};

        // Imprimir el array original
        System.out.println("Array original: " + Arrays.toString(numeros));

        // Calcular la suma de los elementos del array
        int suma = 0;
        for (int i = 0; i < numeros.length; i++) {
            suma += numeros[i];
        }
        System.out.println("La suma de los elementos es: " + suma);

        // Encontrar el número más grande en el array
        int maximo = numeros[0];
        for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > maximo) {
                maximo = numeros[i];
            }
        }
        System.out.println("El número más grande es: " + maximo);

        // Ordenar el array en orden ascendente
        Arrays.sort(numeros);
        System.out.println("Array ordenado: " + Arrays.toString(numeros));
    }
}
```

Ejemplo Array list

```java
import java.util.ArrayList; 
import java.util.Scanner;

public class AppNotas {

  public static void main(String[] args) {

    ArrayList<String> notas = new ArrayList<>();
    
    Scanner scan = new Scanner(System.in);

    while(true) {

      System.out.println("1. Agregar nota");  
      System.out.println("2. Mostrar notas");
      System.out.println("3. Salir");

      int opcion = scan.nextInt();

      if (opcion == 1) {
        agregarNota(notas, scan);  
      } else if (opcion == 2) {
        mostrarNotas(notas);
      } else {
        break;
      }

    }

  }

  public static void agregarNota(ArrayList<String> notas, Scanner scan) {
    
    System.out.println("Ingrese el titulo de la nota:");
    String titulo = scan.nextLine();
    
    System.out.println("Ingrese el contenido de la nota:");
    String contenido = scan.nextLine();
    
    notas.add(titulo + " - " + contenido);

  }

  public static void mostrarNotas(ArrayList<String> notas) {

    for(String n : notas) {
      System.out.println(n);
    }

  }

}
```

## 2. Crear un ejemplo de Array y otro de ArrayList para visualizar sus diferencias.


# Solución
## Actividad 1
### Explicación de Ejemplo Array
En la primera línea se crea y se inicializa un array de números enteros, el cual se va a llamar "numeros", luego en la siguiente línea se imprime el array original, utilizando el método `.toString()` para convertir el array en una cadena y poderlo imprimir en consola de una manera legible.
Después se calcula la suma de los elementos del array utilizando un ciclo `for`, el cual va a recorrer por todos los elementos del array, y sumar uno por uno los elementos del array y luego almacenarlos en una variable llamada "suma", la cual luego imprime por consola el resultado de esa suma.
Luego con otro bucle `for` encontraremos el número mayor en el array, para este creamos una variable llamada "maximo" inicializada en 0, la cual nos va a permitir comparar cada elemento del array con esa variable, ya que, si alguno de los elementos es mayor que "maximo", se actualiza ese valor que esta por defecto ahí como 0 y por último se imprimirá ese valor máximo ya que ese sería el número mayor, que estamos buscando.
Por último se ordenan los elementos del array en orden ascendente, ya que originalmente está en desorden, esto se hace utilizando el método `.sort()` que se utiliza para ordenar los elementos de un array.

### Explicación de Ejemplo Array list
Primero que todo importamos dos librerías las cuales son la "ArrayList" y la "Scanner"  para trabajar con listas dinámicas y obtener la entrada del usuario.
Luego creamos un arraylist llamado "notas"  y después instanciamos la clase Scanner.
A continuación creamos un ciclo `while` en el cual vamos a tener tres opciones (1.agregar nota, 2.mostrar las notas, 3.salir), en la siguiente línea sirve para que se ingrese la opción por consola y lo almacene en una variable llamada "opcion".
Con un condicional `if-else if-else`, validamos la opción que se digito, el cual lo haremos creando y utilizando dos métodos uno se va a llamar **"agregarNota"** y el otro **"mostrarNota"**. En la función **"agregarNota"** solicita al usuario que ingrese el título y el contenido de la nota, y luego concatena ambos en una cadena y agrega esta cadena al ArrayList de notas con el método `.add()` y en la función **"mostrarNotas"** recorre el ArrayList de notas e imprime cada nota en la consola utilizando un `for each`.



## Actividad 2
### Array

```java
public class EjerArray{
    public static void main(String[] args) {
        String[] nombres = new String[5];

        //ADICIONA CADA ELEMENTO AL ARRAY
        nombres[0] = "Carolina";
        nombres[1] = "Gonzalo";
        nombres[2] = "Reina";
        nombres[3] = "Joaquin";
        nombres[4] = "Carlos";

        //tambien se puene inicializar de esta forma: int[] nombres ={"Carolina", "Gonzalo", "Reina", "Joaquin", "Carlos"}

        //RECORRE EL ARRAY PARA IMPRIMIR CADA ELEMENTO
        for (int i=0; i < nombres.length; i++){
            System.out.println(nombres[i]);
        }

 }

}
```

### ArrayList

```java
import java.util.ArrayList;

public class EjerArrayList {
    public static void main(String[] args) {
        ArrayList<String> nombres = new ArrayList<>();

        //ADICIONO LOS ELEMENETOS A MI ARRAYLIST
        nombres.add("Carolina");
        nombres.add("Reina");
        nombres.add("Gonzalo");
        nombres.add("Joaquin");
        nombres.add("Carlos");

        //MUESTRO LOS ELEMENTOS RECORIENDOLOS EN UN FOR EACH
        for(String nombre : nombres){
            System.out.println(nombre);
        }

        //ME MUESTRA ATARVES DEL METODO .size() EL TAMAÑO DEL ARRAYLIST
        int tamaño = nombres.size();
        System.out.println(tamaño);

        //tambien puedo mostrar los nombres con el metodo get(), de acuerdo a su posicion asi: String nombre = nombres.get(5); muestra a "Carlos"
        // los puedo eliminar con el metodo remove(), de acuerdo a su posicion asi: nombres.remove(2); elimina a "Gonzalo"
    }
}

```






