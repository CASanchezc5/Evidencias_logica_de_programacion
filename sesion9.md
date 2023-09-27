<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 


<!-- Su documentación aquí -->
# Ejercicios de Lógica de Programación
## 1. Calculadora de resistencias eléctricas
Una resistencia eléctrica es un componente electrónico que se utiliza para limitar el flujo de corriente eléctrica en un circuito. Es decir, su función es oponerse al paso de la corriente eléctrica y disminuir su intensidad.

Las resistencias se componen generalmente de un material conductor, como el carbono o el metal, que se coloca en un cuerpo cerámico o de vidrio. El valor de la resistencia (es decir, la cantidad de oposición que ofrece al paso de la corriente eléctrica) se mide en ohms, y depende de la composición del material y de su geometría.

Las resistencias se utilizan en una gran variedad de circuitos electrónicos, tanto en circuitos analógicos como digitales. Algunas de las aplicaciones más comunes de las resistencias incluyen la limitación de corriente en circuitos de alimentación, el ajuste de niveles de voltaje y corriente en circuitos de amplificación, y la medición de corriente y voltaje en circuitos de control y monitoreo.

Calculadora Código de colores - Online

https://www.digikey.com/es/resources/conversion-calculators/conversion-calculator-resistor-color-code

![color resistencias](https://firebasestorage.googleapis.com/v0/b/imagenes-dd8e6.appspot.com/o/colores%20resistencias.png?alt=media&token=5c316654-f746-4a5e-ba2a-6d43a31de035)

El objetivo de este ejercicio es crear un programa en Java que permita calcular el valor de una resistencia eléctrica a partir de los colores de sus bandas, y que tenga en cuenta la tolerancia.

Para ello, el programa debe solicitar al usuario que elija los colores de las tres bandas de la resistencia a través de un menú de opciones. Los colores disponibles son: negro, marrón, rojo, naranja, amarillo, verde, azul, violeta, gris y blanco.

Una vez que el usuario ha elegido los colores de las tres bandas, el programa debe pedir al usuario que seleccione la tolerancia de la resistencia a través de otro menú de opciones. Las opciones disponibles son: marrón (1%), rojo (2%), oro (5%) y plata (10%). Si el usuario no selecciona ninguna opción válida, se debe utilizar la tolerancia por defecto del 5%.

Con los colores y la tolerancia seleccionados, el programa debe calcular el valor de la resistencia y mostrarlo en la consola, junto con la tolerancia seleccionada.

Para calcular el valor de la resistencia, se debe utilizar la fórmula: valor = ((valor1 10) + valor2) multiplicador, donde valor1 y valor2 son los valores correspondientes a los dos primeros colores elegidos por el usuario (según la tabla de colores), y multiplicador es el valor correspondiente al tercer color elegido por el usuario (también según la tabla de colores). Finalmente, se debe mostrar el valor de la resistencia en ohms y la tolerancia seleccionada.

## 2. Calculadora de la mediana
La mediana es un valor estadístico que se utiliza para describir el centro de un conjunto de datos. Es el valor que se encuentra justo en el medio de un conjunto de datos ordenados de menor a mayor. Es decir, la mediana divide el conjunto de datos en dos partes iguales, donde la mitad de los valores están por encima de la mediana y la otra mitad están por debajo de ella.

Mediana con números impares:

Supongamos este grupo de números: {3, 7, 4, 2, 8}

Ordenarlos de menor a mayor: {2, 3, 4, 7, 8} El número de elementos es impar (5 elementos), por lo que la mediana será el elemento central una vez ordenados. El elemento central es el número 4. Por lo tanto, la mediana de este grupo de números impares es 4.

Mediana con números pares:

Supongamos este otro grupo: {5, 12, 2, 11, 3, 9}

Ordenarlos de menor a mayor: {2, 3, 5, 9, 11, 12} El número de elementos es par (6 elementos), por lo que la mediana será el promedio de los 2 elementos centrales una vez ordenados. Los elementos centrales son el 5 y el 9. El promedio de 5 y 9 es (5 + 9) / 2 = 7 Por lo tanto, la mediana de este grupo de números pares es 7.

La mediana es el elemento central de un grupo ordenado cuando la cantidad de elementos es impar. Y es el promedio de los dos elementos centrales cuando la cantidad es par.


# Solución
Este ejercicio lo realizamos en clase (en parejas) y fueron repartidos, en mi caso me toco el ejercicio número 1 **" Calculadora de resistencias eléctricas"**.

```java
//CALCULADORA DE RESISTENCIAS ELECTRICAS
import java.util.Scanner;

public class Ejercicio1{
    public static void main(String[] args) {
        System.out.println("============== BANDA DE COLOR 1 ==================");
        int color1 = menu1();
        System.out.print("El color seleccionado es: ");
        System.out.println(color1);
        System.out.println("================================================");
    
        System.out.println("============== BANDA DE COLOR 2 ==================");
        int color2 = menu1();
        System.out.print("El color seleccionado es: ");
        System.out.println(color2);
        System.out.println("================================================");

        System.out.println("============== MULTIPLICADOR ==================");
        int color3 = menu1();
        System.out.print("El color seleccionado es: ");
        System.out.println(color3);
        System.out.println("================================================");

        int v1 = color1;
        int v2 = color2;
        int v3 = color3;

        int v4 = (v1 *10) + v2;

        double mult=0;
        // Aqui verifica el multiplicador
        if (v3 == 0) {
            mult = v4 *1;
        }else if (v3 == 1) {
            mult = v4 * 10;
        }else if (v3 == 2) {
            mult = v4 * 100;
        }else if (v3 == 3) {
            mult = v4 * 1000;
        }else if (v3 == 4) {
            mult = v4 * 10000;
        }else if (v3 == 5) {
            mult = v4 * 100000;
        }else if (v3 == 6) {
            mult = v4 * 1000000;
        }else if (v3 == 7) {
            mult = v4 /10;
        }else if (v3 == 8) {
            mult = v4 /100;
        } else {
            System.out.println("");
        }
        // System.out.println(v4);
        String resultadoFormateado = formatearResultado(mult);
        System.out.println("Valor de la Resistencia: " + resultadoFormateado + " "+menu2());
    
    
    }

    public static int menu1(){ // este menu sirve para las tres primeras fases 
        Scanner input = new Scanner (System.in);
        System.out.println("0 - Negro");
        System.out.println("1 - Marron");
        System.out.println("2 - Rojo");
        System.out.println("3 - Naranja");
        System.out.println("4 - Amarillo");
        System.out.println("5 - Verde");
        System.out.println("6 - Azul");
        System.out.println("7 - Morado");
        System.out.println("8 - Gris");
        System.out.println("9 - Blanco");
        System.out.print("Seleccione un color: ");
        int color = input.nextInt();
        // input.close();
        return color; 
    }

    public static String menu2(){ // este sirve para la presición
        Scanner input1 = new Scanner (System.in);
        System.out.println("Marrón +/- 1%"); 
        System.out.println("Rojo +/- 2%"); 
        System.out.println("Oro +/- 5%"); 
        System.out.println("Plata +/- 10%"); 
        System.out.print("Seleccione un color: ");
        
       String color2 = input1.nextLine();
        if (color2.equals("Marron")) {
            return "Marrón +/- 1%";
        } else if (color2.equals("Rojo")) {
            return "Rojo +/- 2%";
        } else if (color2.equals("Oro")) {
            return "Oro +/- 5%";
        } else if (color2.equals("Plata")) {
            return "Plata +/- 10%";
        } else {
            return "Color no reconocido";
        }
       
    }

    public static String formatearResultado(double resultado) {
        if (resultado >= 1000) {
            // Si es mayor o igual a 1000, dividir por 1000 y agregar "K"
            return (resultado / 1000) + " K";
        } else {
            // De lo contrario, dejar el resultado tal como está
            return String.valueOf(resultado +" Ohms");
        }
    }
}

```





