<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 

# Actividad: 
>Ejecicios de métodos en Java
Resolver en parejas el ejercicio asignado por el docente.

### Calculadora de la mediana
La mediana es un valor estadístico que se utiliza para describir el centro de un conjunto de datos. Es el valor que se encuentra justo en el medio de un conjunto de datos ordenados de menor a mayor. Es decir, la mediana divide el conjunto de datos en dos partes iguales, donde la mitad de los valores están por encima de la mediana y la otra mitad están por debajo de ella.

Mediana con números impares:

Supongamos este grupo de números: {3, 7, 4, 2, 8}

Ordenarlos de menor a mayor: {2, 3, 4, 7, 8} El número de elementos es impar (5 elementos), por lo que la mediana será el elemento central una vez ordenados. El elemento central es el número 4. Por lo tanto, la mediana de este grupo de números impares es 4.

Mediana con números pares:

Supongamos este otro grupo: {5, 12, 2, 11, 3, 9}

Ordenarlos de menor a mayor: {2, 3, 5, 9, 11, 12} El número de elementos es par (6 elementos), por lo que la mediana será el promedio de los 2 elementos centrales una vez ordenados. Los elementos centrales son el 5 y el 9. El promedio de 5 y 9 es (5 + 9) / 2 = 7 Por lo tanto, la mediana de este grupo de números pares es 7.

La mediana es el elemento central de un grupo ordenado cuando la cantidad de elementos es impar. Y es el promedio de los dos elementos centrales cuando la cantidad es par.

>Ejemplo

```JAVA
import java.util.Arrays;
import java.lang.reflect.Array;

public class Main {
    public static void main(String[] args) {
        int[] comboDatos = {2, 6, 1, 8, 3, 5};
        Arrays.sort(comboDatos);
        int totalDatos = comboDatos.length;
        int suma = 0;
        double mediana;
        System.out.println("El total de datos es:" + totalDatos + " y es par");
        if (totalDatos % 2 == 0) {
            for (int i = 0; i < comboDatos.length; ) {
                suma += comboDatos[i];
            }
            mediana = (double) suma / comboDatos.length;
            for (int i = 0; i < comboDatos.length; i++) {
                System.out.println("La mediana es:" + " " + mediana);
            }
        }
    }
}
```
[Sesion8](https://xeduark.github.io/Evidencias_logica_de_programacion/sesion8.html)

[Sesion10](https://xeduark.github.io/Evidencias_logica_de_programacion/sesion10.html)






