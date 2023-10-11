<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


# Actividad: 
>Ejecicios de métodos en Java

Implementar los siguientes métodos:

1. Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.
2. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.
3. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.
4. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.
5. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

### SOLUCIÓN

1. 
```JAVA

//By:xeduark


import java.util.Scanner;

public class main {
    static int maximo(int a, int b) {
        int max = 0;

        if (a > b)
            max = a;
        else
            max = b;
        return (max);
    }
public static void main(String[]args)
{
    Scanner datos=new Scanner(System.in);
    int max=0;
    int a=0,b=0;
    System.out.println("Ingrese un numero:");
    a=datos.nextInt();
    System.out.println("Ingresa otro numero:");
    b=datos.nextInt();

    max=maximo(a,b);
    System.out.println("El numero mayor es: " +max);
}

}

```

2. 
```java
import java.util.Scanner;

//By:xeduark
public class Main {
        public static int contarVocales(String cadena) {
            String vocales = "aeiouAEIOU";
            int contador = 0;

            for (int i = 0; i < cadena.length(); i++) {
                char letra = cadena.charAt(i);
                if (vocales.contains(String.valueOf(letra))) {
                    contador++;
                }
            }

            return contador;
        }

        public static void main(String[] args) {
            Scanner cadena =new Scanner(System.in);
            System.out.print("Ingrese una cadena de texto: ");
            String texto = cadena.nextLine();

            int numeroVocales = contarVocales(texto);
            System.out.println("El número de vocales en la cadena es: " + numeroVocales);

            cadena.close();
        }
    }
```
3. 

```java
// By: xeduark
public class Main {
    public static String cambiarMayusculasMinisculas(String cadena) {
        StringBuilder resultado = new StringBuilder();

        for (int i = 0; i < cadena.length(); i++) {
            char caracter = cadena.charAt(i);

            if (Character.isUpperCase(caracter)) {
                resultado.append(Character.toLowerCase(caracter));
            } else if (Character.isLowerCase(caracter)) {
                resultado.append(Character.toUpperCase(caracter));
            } else {
                resultado.append(caracter);
            }
        }

        return resultado.toString();
    }

    public static void main(String[] args) {
        String cadena = "EjEmPlO De CaDeNa";
        String resultado = cambiarMayusculasMinisculas(cadena);
        System.out.println("Cadena original: " + cadena);
        System.out.println("Cadena modificada: " + resultado);
    }
}
```

4. 

```java
//By xeduark
public class Main {
    public int contarPalabras(String texto) {
        int contador = 0;
        String[] palabras = texto.split(" ");

        for (String palabra : palabras) {
            if (palabra.equalsIgnoreCase("java")) {
                contador++;
            }
        }

        return contador;
    }
   
}
```
5. 

```java

//By : Xeduark

import java.util.Arrays;



public class Main {
    public static void main(String[] args) {

        public static String ordenarPalabras(String texto); {
            // Dividir el texto en palabras
            String[] palabras = texto.split(" Hola soy amigo de todos en el Cesde");
            Arrays.sort(palabras);
            String resultado = String.join(" ", palabras);
            return resultado;

        }
    }
}

```






