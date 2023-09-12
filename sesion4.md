<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4


<!-- Su documentación aquí -->
# Actividad 4: Ejercicios de control de flujo con expresiones compuestas 
```java
// Variables de tipo String
String nombre = "Juan Pérez";
String apellido = "González";
String identificación = "1000000001";
String correo = "juan.perez@ejemplo.com";
String carrera = "Desarrollo de Software";
String universidad = "Cesde";
// Variable de tipo int
int edad = 20;
// Variable de tipo boolean
boolean esActivo = true;
boolean becado = false;
// Variable de tipo char
char género = 'M';
// Variable de tipo double
double promedio = 4.5;
// Variable de tipo int
int semestre = 2;
```

Con la información anterior, implementa los siguientes ejercicios:

1. Determinar si el estudiante es mayor de edad y tiene un estado activo.
2. Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.
3. Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.
4. Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.
5. Mostrar toda la información del estudiante si está matriculado en el Cesde.
6. Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.
7. Determinar la cantidad de beca que recibe el estudiante según su promedio:
- 0.0 - 3.4: El estudiante no recibe beca.
- 3.5 - 3.9: El estudiante recibe una beca parcial del 25%.
- 4.0 - 4.4: El estudiante recibe una beca parcial del 50%.
- 4.5 - 5.0: El estudiante recibe una beca completa.

# Solución 
> Aqui va contenido todos los ejercicios incluidos tres ejercicios más que se inventaron, en total quedan **10 ejercicios**.

```java
import java.util.Scanner;

public class Ejercondicional{
    public static void main(String[] args) {
        //ingreso de datos por consola          
        Scanner input = new Scanner(System.in);

// Variables de tipo String
        String nombre = "Juan Pérez";
        String apellido = "González";
        String identificación = "1000000001";
        String correo = "juan.perez@ejemplo.com";
        String carrera = "Desarrollo de Software";
        String universidad = "Cesde";
// Variable de tipo int
        int edad = 20;
// Variable de tipo boolean
        boolean esActivo = true;
        boolean becado = false;
// Variable de tipo char
        char género = 'M';
// Variable de tipo double
        double promedio = 4.5;
// Variable de tipo int
        int semestre = 2;

        System.out.println("--------------------------------------------------------------------------------");
        System.out.println("Ejercicio 1");

        if (edad >= 18 && esActivo) {
            System.out.println("Es mayor de edad y esta activo");
        }

        System.out.println("--------------------------------------------------------------------------------");
        System.out.println("Ejercicio 2");

        if (!becado || "Desarrollo de software".equals(carrera)) {
            System.out.println("El estudiante tiene beca o estudia Desarrollo de Software");

        }

        System.out.println("--------------------------------------------------------------------------------");
        System.out.println("Ejercicio 3");

        if (semestre == 2 && esActivo) {
            System.out.println("Esta en ultimo semestre de la carrera y esta activo");
        }

        System.out.println("--------------------------------------------------------------------------------");
        System.out.println("Ejercicio 4");

        if ("Desarrollo de Software".equals(carrera) && promedio > 4.0) {
            System.out.println("El estudiante estudia Desarrollo de Software y tiene promedio superior a 4.0");
        }

        System.out.println("--------------------------------------------------------------------------------");
        System.out.println("Ejercicio 5");

        if ("Cesde".equals(universidad)) {
            System.out.println("Información del Estudiante:");
            System.out.println(nombre);
            System.out.println(apellido);
            System.out.println(identificación);
            System.out.println(correo);
            System.out.println(carrera);
        }

        System.out.println("--------------------------------------------------------------------------------");
        System.out.println("Ejercicio 6");

        if ("Cesde".equals(universidad) && promedio > 4.0 && esActivo) {
            System.out.println("El estudiante tiene una beca del 50%");
        }

        System.out.println("--------------------------------------------------------------------------------");
        System.out.println("Ejercicio 7");

        if (promedio >= 0.0 && promedio <= 3.4) {
            System.out.println("El estudiante no recibe beca");
        } else if (promedio >= 3.5 && promedio <= 3.9) {
            System.out.println("El estudiante recibe una beca parcial del 25%");
        } else if (promedio >= 4.0 && promedio <= 4.4) {
            System.out.println("El estudiante recibe una beca parcial del 50%");
        } else if (promedio >= 4.5 && promedio <= 5.0) {
            System.out.println("El estudiante recibe una beca completa");
        } else {
            System.out.println("Nota no valida");
        }

        System.out.println("--------------------------------------------------------------------------------");
        System.out.println("Ejercicio 8");

        System.out.print("Escribe un numero entre 1 y 999: ");
        int num = input.nextInt();

        if (num > 0 && num < 10) {
            System.out.println("Tú número es unidad");
        }else if (num >= 10 && num < 100) {
            System.out.println("Tú número es decena");
        }else if (num >= 100 && num < 1000){
            System.out.println("Tú número es centena");
        }
        
        System.out.println("-------------------------------------------------------------------------------------------");
        System.out.println("Ejercicio 9");
        
        System.out.print("Elija una opción de menú: 1.Bandaeja Paisa, 2.Ajiaco, 3.Sancocho, 4.Mamona, 5.Langosta: ");
        int menu = input.nextInt();
        
        switch(menu){
            
            case 1:
                System.out.println("Ud a elejido la Bandeja Paisa");
                break;
            case 2:
                System.out.println("Ud a elejido el Ajiaco");
                break;
            case 3:
                System.out.println("Ud a elejido el Sancocho");
                break;
            case 4:
                System.out.println("Ud a elejido la Mamona");
                break;
            case 5:
                System.out.println("Ud a elejido la Langosta");
                break;
            
            default:
                System.out.println("No ha elejido una opción valida de menú");
        }
        
        System.out.println("-----------------------------------------------------------------------------------------");
        System.out.println("Ejercicio 10");
        
        System.out.print("Escriba uno de los dos siguientes números 1 ó 2: ");
        int numero = input.nextInt();
        String mensaje;
        
        mensaje = (numero == 1 ) ? "Aceptado" : "Rechazado";
        System.out.println(mensaje);


        input.close();
    }
}
```







