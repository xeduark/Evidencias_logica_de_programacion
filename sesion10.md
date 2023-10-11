<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


# Actividad: 
>Prueba, ejecución y explicación de ejercicios de lógica de programación.

Selecciona dos ejercicios de la sesión 10, impleméntalos, ejecútalos y proporciona una explicación detallada de cada uno.

1. ### Programa en Java para formar subgrupos con integrantes aleatorios de igual cantidad.

```java
import java.util.ArrayList;
import java.util.Collections;
import java.util.Scanner;

public class FormacionSubgrupos {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      ArrayList<String> integrantes = new ArrayList<String>();

      // Solicitar lista de integrantes
      System.out.print("Ingrese la lista de integrantes separados por coma: ");
      String inputIntegrantes = input.nextLine();
      String[] integrantesArray = inputIntegrantes.split(",");
      for (String integrante : integrantesArray) {
         integrantes.add(integrante.trim());
      }

      // Solicitar cantidad de subgrupos
      System.out.print("Ingrese la cantidad de subgrupos que desea formar: ");
      int cantidadSubgrupos = input.nextInt();

      // Formar subgrupos
      int integrantesPorSubgrupo = integrantes.size() / cantidadSubgrupos;
      int integrantesSobrantes = integrantes.size() % cantidadSubgrupos;
      Collections.shuffle(integrantes); // mezclar la lista de integrantes para formar subgrupos aleatorios
      int indiceInicial = 0;
      for (int i = 0; i < cantidadSubgrupos; i++) {
         int integrantesEnSubgrupo = integrantesPorSubgrupo;
         if (integrantesSobrantes > 0) {
            integrantesEnSubgrupo++;
            integrantesSobrantes--;
         }
         int indiceFinal = indiceInicial + integrantesEnSubgrupo;
         ArrayList<String> subgrupo = new ArrayList<String>(integrantes.subList(indiceInicial, indiceFinal));
         indiceInicial = indiceFinal;
         System.out.printf("Subgrupo %d: %s%n", i + 1, subgrupo);
      }
   }
}
```
### Explicación:

2. ### Programa en Java para asignar aleatoriamente ejercicios a un grupo de personas sin repetir.

```java

import java.util.ArrayList;
import java.util.Collections;
import java.util.Scanner;

public class AsignacionEjercicios {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      ArrayList<String> personas = new ArrayList<String>();

      // Solicitar lista de personas
      System.out.print("Ingrese la lista de personas separadas por coma: ");
      String inputPersonas = input.nextLine();
      String[] personasArray = inputPersonas.split(",");
      for (String persona : personasArray) {
         personas.add(persona.trim());
      }

      // Obtener cantidad de ejercicios
      int cantidadEjercicios = personas.size();

      // Generar lista de ejercicios aleatorios sin repetir
      ArrayList<Integer> numerosEjercicios = new ArrayList<Integer>();
      for (int i = 1; i <= cantidadEjercicios; i++) {
         numerosEjercicios.add(i);
      }
      Collections.shuffle(numerosEjercicios); // mezclar la lista de números de ejercicios para asignarlos aleatoriamente
      ArrayList<String> ejercicios = new ArrayList<String>();
      for (int i = 0; i < cantidadEjercicios; i++) {
         ejercicios.add("Ejercicio " + numerosEjercicios.get(i));
      }

      // Asignar ejercicios a personas
      Collections.shuffle(personas); // mezclar la lista de personas para asignarles ejercicios aleatorios
      for (int i = 0; i < cantidadEjercicios; i++) {
         System.out.printf("%s: %s%n", personas.get(i), ejercicios.get(i));
      }
   }
}
```
### Explicación:

[Sesion9](https://xeduark.github.io/Evidencias_logica_de_programacion/sesion9.html)

[Sesion11](https://xeduark.github.io/Evidencias_logica_de_programacion/sesion11.html)



