<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 7 


# Actividad: 

## Ejecicios Array - ArrayList

1. En parejas, probar, analizar y explicar el funcionamiento de los siguientes ejemplos de Array y ArrayList.

>Ejemplo Array:

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
>Ejemplo Array list:

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

2. Crear un ejemplo de Array y otro de ArrayList para visualizar sus diferencias.

### 1. Array 

```java
import java.util.Arrays;
public class Main {
    public static void main(String[] args) {
       int[] vueltas = {50,53,57,52,50};
       for (int i = 0; i < 5; i++) {
           System.out.println(vueltas[i] + " ");
        }
       vueltas[0] = 75;
        for (int i = 0; i < 5; i++) {
            System.out.println(vueltas[i] + " ");
        }


    }
}
```
### 2. ArrayList

```java
import java.util;
//By: xeduark
public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        ArrayList<Integer> numeros = new ArrayList();
        int n;

        do {
            System.out.println("Introduce números enteros. 0 para acabar: ");
            System.out.println("Numero: ");
            n = sc.nextInt();
            if (n != 0){
                numeros.add(n);
            }
        }while (n != 0);

        System.out.println("Ha introducido: " + numeros.size() + " números:");

        
        System.out.println(numeros);
                                        
        Iterator it = numeros.iterator();
        while(it.hasNext()){
            System.out.println(it.next());
        }
        
        double suma = 0;
        for(Integer i: numeros){
            suma = suma + i;
        }
        System.out.println("Suma: " + suma);
        System.out.println("Media: " + suma/numeros.size());
    }
}

```
[Sesion6](https://xeduark.github.io/Evidencias_logica_de_programacion/sesion6.html)

[Sesion8](https://xeduark.github.io/Evidencias_logica_de_programacion/sesion8.html)






