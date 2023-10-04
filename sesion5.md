<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 


# Actividad 5: 
## Ejercicios de bucles
_Resolver los siguientes ejercicios:_

### Ejercicios - while
1. Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.
2. Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.
### Ejercicios - do while
1. Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.
2. Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.
### Ejercicios - for
1. Imprimir los números impares del 1 al 50.
2. Imprimir los números primos del 1 al 100.

## SOLUCIÓN

### Ejercicios - while

1.
 ```JAVA
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        int Multi;

        System.out.println("¿Que tabla desea Realizar?");
        Scanner valor1 = new Scanner(System.in);
        Multi = valor1.nextInt();

        int n1 = 1;
        while (n1 <= 10) {
            System.out.println(Multi + " X " + n1 + " = " + Multi * n1);
            n1++;

        }
    }
}
```
2. 
```JAVA
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        int n1 = 0;
        int cantidadNumeros = 0;

        System.out.println("INGRESA TU NUMERO DE CEDULA");
        Scanner ingresoDeDatos = new Scanner(System.in);
        String cadena1;
        cadena1 = ingresoDeDatos.nextLine();

        while (n1 < cadena1.length()){
            char caracter = cadena1.charAt(n1);
            if (Character.isDigit(caracter)){
                cantidadNumeros++;
            }
            n1++;
        }
        System.out.println("LA CANTIDAD DE CARACTERES DE SU CEDULA SON :"+cantidadNumeros);
    }
}
```
### Ejercicios - do while

1. 
```JAVA
import java.util.Scanner;
class Main {
  public static void main(String[] args) {
     Scanner entradaDatos = new Scanner(System.in);
    int i = 1;     
        System.out.println("Por favor ingrese un numero:");
        int numero =entradaDatos.nextInt();
           do {
            System.out.println(i);
         i++;         
        }while(i<=100 && numero >=0 ); 
  }
}
```
2. 
```JAVA
import java.util.Scanner;
class Main {
  public static void main(String[] args) {
     Scanner entradaDatos = new Scanner(System.in);
     System.out.println("ingresa un  numero: ");
        int numero = entradaDatos.nextInt();
        System.out.println("la tabla de multiplicar del " +numero+ " es: ");
        
        int i =1;
        do{
            
            System.out.println( numero + "x" +i+ "=" +numero*i);
            
            i++;  
        }while(i<=10 && numero!=0);
  }
}
```
### Ejercicios - for

1. 

```JAVA
class Main {
  public static void main(String[] args) {
    for (int i=1; i<50; i+=2) {
            System.out.println(i);
            
            
        }
  }
}
```
2. 
```JAVA
class Main {
  public static void main(String[] args) {
    int num1max = 100;

        for (int i = 1; i <= num1max; i++) {
            int divisor = 0;
            for (int x = 1; x <= i / 2; x++) {
                if (i % x == 0) {
                    divisor += 2;

                }
                if (divisor > 2) {
                    break;
                }

            }
            if (divisor == 2) {
                System.out.println(i);

            }
        }
  }
}
```
[Sesion4](https://xeduark.github.io/Evidencias_logica_de_programacion/sesion4.html)

[Sesion6](https://xeduark.github.io/Evidencias_logica_de_programacion/sesion6.html)






