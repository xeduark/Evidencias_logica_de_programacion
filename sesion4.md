<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4


# Actividad 4: 
## Ejercicios de control de flujo con expresiones compuestas

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
   * 0.0 - 3.4: El estudiante no recibe beca.
   * 3.5 - 3.9: El estudiante recibe una beca parcial del 25%.
   * 4.0 - 4.4: El estudiante recibe una beca parcial del 50%.
   * 4.5 - 5.0: El estudiante recibe una beca completa.

## SOLUCIÓN

```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner SR = new Scanner(System.in);
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

        System.out.println("_________________________________________________________________________________________________");
        System.out.println("Ejercicio 1");

        if (edad >= 18 && esActivo) {
            System.out.println("Si es mayor de edad y esta activo");

        } else {
            System.out.println("No es mayor de edad");
        }

        System.out.println("_________________________________________________________________________________________________");
        System.out.println("Ejercicio 2");

        if (becado == true && carrera.equals("Desarrollo de Software")) {
            System.out.println("El estudiante tiene una beca y estudia Desarrollo de Software");

        } else if (becado == !true || carrera.equals("Desarrollo de Software")) {
            System.out.println("El estudiante no tiene una beca pero estudia Desarrollo de Software");
        } else {
            System.out.println("El estudiante no tiene una beca y tampoco estudia Desarrollo de Software");
        }
        System.out.println("_________________________________________________________________________________________________");
        System.out.println("Ejercicio 3");

        if (semestre == 3 && esActivo == true) {
            System.out.println("El estudiante se encuentra en el ultimó semestre y se encuentra activo");
        } else if (semestre == 3 && esActivo == !true) {
            System.out.println("El estudiante se encuentra en el ultimó semestre pero se encuentra inactivo");
        } else if (semestre <= 3 || esActivo == true) {
            System.out.println("El estudiante se encuentra en el " + semestre + " semestre y se encuentra activo");
        } else {
            System.out.println("usuario no encontrado");
        }

        System.out.println("_________________________________________________________________________________________________");
        System.out.println("Ejercicio 4");

        if (carrera.equals("Desarrollo de Software") && promedio >= 4.5) {
            System.out.println("El estudiante esta cursando Desarrollo de Software y tiene un promedio de 4.5");
        } else {
            System.out.println("El estudiante se encuentra cursando " + carrera + " y tiene un promedio de " + promedio);
        }
        System.out.println("_________________________________________________________________________________________________");
        System.out.println("Ejercicio 5");

        if (universidad.equals("Cesde")) {
            System.out.println("nombre= " + nombre);
            System.out.println("apellido=" + apellido);
            System.out.println("identificación= " + identificación);
            System.out.println("correo= " + correo);
            System.out.println("carrera= " + carrera);
            System.out.println("universidad= " + universidad);
            System.out.println("edad= " + edad);
            System.out.println("Estado activo");
            System.out.println("no becado");
            System.out.println("género= " + género);
            System.out.println("promedio= " + promedio);
            System.out.println("semestre= " + semestre);
        } else {
            System.out.println("No es estudiante Cesde");
        }
        System.out.println("_________________________________________________________________________________________________");
        System.out.println("Ejercicio 6");

        if (universidad.equals("Cesde") && promedio >= 4.0 && esActivo) {
            System.out.println("Tienes una Beca del 50% para continuar tu carrera en Cesde");
        } else {
            System.out.println("Lo sentimos, actualmente no calificas para una beca");
        }

        System.out.println("_________________________________________________________________________________________________");
        System.out.println("Ejercicio 7");

        if (promedio >= 0.0 && promedio <= 3.4) {
            System.out.println("El estudiante no recibe beca.");
        } else if (promedio >= 3.5 && promedio <= 3.9) {
            System.out.println("El estudiante recibe una beca parcial del 25%.");
        } else if (promedio >= 4.0 && promedio <= 4.4) {
            System.out.println("El estudiante recibe una beca parcial del 50%.");

        } else if (promedio >= 4.5 && promedio <= 5.0) {
            System.out.println("El estudiante recibe una beca completa.");
        } else {
            System.out.println("Error, verifique la nota");
        }

        System.out.println("_________________________________________________________________________________________________");
        System.out.println("Ejercicio 8");

        System.out.println("Ingrese su numero de identificacion:");
        String dato1 = SR.nextLine();

        if (dato1.equals(identificación)) {
            System.out.println("Su correo electronico es" + correo);

            System.out.println("Desea cambiar su correo electronico?");
            String dato2 = SR.nextLine();

            if (dato2.equals("si")) {
                System.out.println("Ingrese el nuevo correo:");
            }
            String dato3 = SR.nextLine();

            System.out.println("Su correo ha sido cambiado con exito");
            System.out.println("Su nuevo correo es: " + dato3);
        } else {
            System.out.println("Verifique su numero de identificacion");
        }

        System.out.println("_________________________________________________________________________________________________");
        System.out.println("Ejercicio 9");

        if (universidad.equals("Cesde")) {
            System.out.println("Ingrese la sede en la que está matriculado");
            String sede = SR.nextLine();

            System.out.println("Su sede es " + sede);

        }

        System.out.println("_________________________________________________________________________________________________");
        System.out.println("Ejercicio 10");

        if (universidad.equals("Cesde") && esActivo == true) {
            System.out.println("Ten en cuenta que puedes conocer mas acerca de nuestros programas de educacion en tu sede de Bello");
            System.out.println("Deseas conocer mas acerca de los programas que tenemos para ti?");
            String cult = SR.nextLine();

            if (cult.equals("si")) {
                System.out.println("Ingresa a nuestra pagina en Cesde.com/Estudiantes para conocer mas");
            } else {
                System.out.println("Buena suerte");
            }

        }

    }
}
```
[Sesion3](https://xeduark.github.io/Evidencias_logica_de_programacion/sesion3.html)

[Sesion5](https://xeduark.github.io/Evidencias_logica_de_programacion/sesion5.html)





