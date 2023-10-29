<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 13 


<!-- Su documentación aquí -->
# Ejercicios de lógica de programación para el desarrollo de habilidades colaborativas
En esta sesión, el docente coordinará una serie de ejercicios de lógica de programación que fomentarán la participación activa de los estudiantes en un entorno colaborativo. Estos ejercicios ayudarán a los estudiantes a desarrollar habilidades de lógica, resolución de problemas, comunicación, colaboración e intercambio de ideas. Se espera que esta experiencia de aprendizaje sea enriquecedora y contribuya al desarrollo de las competencias necesarias en el campo de la programación y la informática.

## Repositorio Proyecto Integrador (Consola). Grupo-Martes-Mañana
```
git clone https://github.com/jfinfocesde/pi_consola
```

# Solución
Aqui se muestra el primer algoritmo del proyecto integrador que esta desarrollando mi equipo

### GRUPO 5

### Algoritmo 1
Este algoritmo da a elegir entre 6 figuras geometricas tridimensionales (cubo, cono, esfera, prisma rectangular, piramide, cilindro), se ingresan sus parametros por consola y se halla el volumen en cm3 de la figura seleccionada.
```java
package com.example;

import java.util.Scanner;
import java.lang.Math;

public class Grupo5 {
    public void ejercicio1() {
        Scanner input = new Scanner(System.in);

        System.out.println("selecciona una figura geometrica: ");
        System.out.println("1. cubo");
        System.out.println("2. cilindro");
        System.out.println("3. esfera");
        System.out.println("4. cono");
        System.out.println("5. prisma");
        System.out.println("6. piramide");

        int opcion = input.nextInt();
        System.out.println("Ud eligio el: " + opcion);

        double volumen = 0;

        switch (opcion) {
            case 1:
                System.out.print("ingresa el lado del cubo:");
                double ladoCubo = input.nextDouble();
                volumen = Math.pow(ladoCubo, 3);
                break;
            case 2:
                System.out.print("ingresa el radio del cilindro:");
                double radioCilindro = input.nextDouble();
                System.out.print("ingresa la altura del cilindro:");
                double alturaCilindro = input.nextDouble();
                volumen = Math.PI * Math.pow(radioCilindro, 2) * alturaCilindro;
                break;
            case 3:
                System.out.print("ingresa el radio de la esfera:");
                double radioEsfera = input.nextDouble();
                volumen = (4.0 / 3.0) * Math.PI * Math.pow(radioEsfera, 3);
                break;
            case 4:
                System.out.print("ingresa el radio del cono:");
                double radioCono = input.nextDouble();
                System.out.print("ingresa la altura del cono:");
                double alturaCono = input.nextDouble();
                volumen = (1.0 / 3.0) * Math.PI * Math.pow(radioCono, 2) * alturaCono;
                break;
            case 5:
                System.out.print("ingresa el area de la base del prisma:");
                double areaBasePrisma = input.nextDouble();
                System.out.print("ingresa  la altura del prisma:");
                double alturaPrisma = input.nextDouble();
                volumen = areaBasePrisma * alturaPrisma;
                break;
            case 6:
                System.out.print("Ingrese la longitud de la base del triángulo: ");
                double base = input.nextDouble();
                System.out.print("Ingrese la altura del triángulo: ");
                double alturaTriangulo = input.nextDouble();
                System.out.print("Ingrese la altura de la pirámide: ");
                double alturaPiramide = input.nextDouble();
                double areaBase = (base * alturaTriangulo) / 2;
                volumen = (1.0 / 3) * areaBase * alturaPiramide;
                break;

            default:
                System.out.println("Opcion invalida");
                break;
        }

        System.out.println("el volumen de la figura seleccionada es: " + volumen+ " cm3");

        input.close();
    }
}

```





