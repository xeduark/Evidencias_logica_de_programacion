<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 11 


# Actividad: 
>Ejercicios de Lógica de Programación

1. Basándose en el algoritmo 1 de la sesión 11, aplicar la siguiente variante: Dado un conjunto de números enteros, se debe determinar si existe algún número que aparezca más de una vez. Si es así, se deben imprimir todos los números que aparezcan más de una vez.

2. Desarrollar un algoritmo que realice la conversión de binario a decimal.

### Solución:

1. 

```java
//By:xeduark
 import java.util.*;
public class Main {

        public static void main(String[] args) {
            int[] numeros = {1, 2, 3, 4, 5, 2, 6, 7, 8, 3, 9, 9};//en este caso imprime 2, 3 y 9
            identificarNumerosRepetidos(numeros);
        }

        public static void identificarNumerosRepetidos(int[] numeros) {
            Map<Integer, Integer> contador = new HashMap<>();

            for (int numero : numeros) {
                if (contador.containsKey(numero)) {
                    contador.put(numero, contador.get(numero) + 1);
                } else {
                    contador.put(numero, 1);
                }
            }

            System.out.println("Números repetidos:");

            for (Map.Entry<Integer, Integer> entry : contador.entrySet()) {
                if (entry.getValue() > 1) {
                    System.out.println(entry.getKey());
                }
            }
        }
    }

```

2. 

```java
//By: xeduark
public class Main {

        public static void main(String[] args) {
            String binary = "101010"; // Aquí puedes ingresamos el número binario que queremos convertir

            int decimal = 0;
            int power = 0;

            for (int i = binary.length() - 1; i >= 0; i--) {
                int digit = Character.getNumericValue(binary.charAt(i));
                decimal += digit * Math.pow(2, power);
                power++;
            }

            System.out.println("El número decimal equivalente es: " + decimal);
            //Este algoritmo toma un número binario como una cadena de caracteres y lo convierte a decimal utilizando el método de potencias de 2
            // Recorre la cadena de derecha a izquierda, obteniendo cada dígito y multiplicándolo por la potencia correspondiente de 2.
            // Luego, suma todos los resultados para obtener el número decimal equivalente.

        }

    }
```






