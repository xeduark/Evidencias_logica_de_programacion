<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 3 


# Actividad 3: 
## Ejercicios de operaciones básicas en Java.

1. **Suma y multiplicación:** Escribe un programa que solicite al usuario dos números enteros y luego imprima la suma y multiplicación de esos números.

2. **Resta y división:** Escribe un programa que tome dos números enteros ingresados por el usuario y calcule la resta y división de esos números.

3. **Operaciones combinadas:** Escribe un programa que solicite al usuario tres números enteros y realice las siguientes operaciones: suma de los tres números, multiplicación del primer número por el segundo y división del resultado entre el tercer número.

4. **Operaciones con decimales:** Escribe un programa que solicite al usuario dos números decimales y realice las siguientes operaciones: suma, resta, multiplicación y división.

5. **Incremento y decremento:** Escribe un programa que declare una variable entera y la inicialice con un valor. Luego, incrementa su valor en 1 y muestra el resultado. Después, decrementa su valor en 1 y muestra el resultado nuevamente.

6. **Operador de asignación compuesta:** Escribe un programa que declare una variable entera y la inicialice con un valor. Utiliza el operador de asignación compuesta para sumar 5 a la variable y luego mostrar su valor.

7. **Operadores lógicos:** Escribe un programa que tome dos valores booleanos ingresados por el usuario y muestre el resultado de las operaciones lógicas AND, OR y NOT entre esos valores.

8. **Operador ternario:** Escribe un programa que tome un número entero ingresado por el usuario y utilice el operador ternario para determinar si el número es positivo o negativo. Luego, muestra el resultado en la salida.

### SOLUCIÓN 

1. **Suma y multiplicación:**
```JAVA
//By : xeduark
public class Main {
    public static void main(String[] args) {
        int n1;
        int n2;

        Scanner a = new Scanner(System.in);
        System.out.println("Escribe dos numeros para obtener el resultado de su suma, multiplicacion");

        System.out.println("Ingresa el primer numero");
        n1 = a.nextInt();
        System.out.println("Ingresa el segundo numero");
        n2 = a.nextInt();
        System.out.println("La suma de estos numeros es " + (n1+n2));
        System.out.println("La multiplicacion de estos numeros es " + (n1*n2));

    }
    }
```

2. **Resta y división:**

```JAVA 
//  By : xeduark
public class Main {
    public static void main(String[] args) {
        int n1;
        int n2;

        Scanner a = new Scanner(System.in);
        System.out.println("Escribe dos numeros para obtener el resultado de su resta, division");

        System.out.println("Ingresa el primer numero");
        n1 = a.nextInt();
        System.out.println("Ingresa el segundo numero");
        n2 = a.nextInt();
        System.out.println("La resta de estos numeros es " + (n1-n2));
        System.out.println("La division de estos numeros es " + (n1/n2));

    }
}
```
3. **Operaciones combinadas:**

```JAVA
//By : xeduark
public class Main {
    public static void main(String[] args) {
        int n1;
        int n2;
        int n3;


        Scanner a = new Scanner(System.in);
        System.out.println("Escribe tres numeros para obtener diferentes operaciones");

        System.out.println("Ingresa el primer numero");
        n1 = a.nextInt();
        System.out.println("Ingresa el segundo numero");
        n2 = a.nextInt();
        System.out.println("Ingresa el tercer numero");
        n3 = a.nextInt();

        System.out.println("La suma de los tres numeros es " + (n1 + n2 + n3));
        System.out.println("La multiplicacion del primero por el segundo es " + (n1 * n2));
        System.out.println("La division del resultado de los dos primeros entre el tercero es " + (n1*n2/n3));
    }
}

```

4. **Operaciones con decimales:**

``` JAVA
//By: xeduark
public class Main {
    public static void main(String[] args) {
        double n1;
        double n2;


        Scanner a = new Scanner(System.in);
        System.out.println("Escribe dos numeros para obtener diferentes operaciones");

        System.out.println("Ingresa el primer numero");
        n1 = a.nextInt();
        System.out.println("Ingresa el segundo numero");
        n2 = a.nextInt();

        System.out.println("La suma de estos numeros es " + (n1 + n2 ));
        System.out.println("La multiplicacion de estos numeros es " + (n1 * n2 ));
        System.out.println("La resta de estos numeros es " + (n1 - n2 ));
        System.out.println("La division de estos numeros es " + (n1 / n2 ));

        }
    }

```

5. **Incremento y decremento:**

``` JAVA
//By: xeduark
import java.util.Scanner;

public class Main {
    public Main() {
    }

    public static void main(String[] args) {
        new Scanner(System.in);
        int n1 = 10;
        ++n1;
        System.out.println("El resultado de la variable n1 es:" + n1);
        --n1;
        System.out.println("El resultado de la variable n1 es:" + n1);
    }
}

```

6. **Operador de asignación compuesta:**

``` JAVA 
//By: xeduark
public class Main {
    public static void main(String[] args) {
        int  n1 = 10;
        n1 += 5;
        System.out.println(n1);



        }
    }

```

7. **Operadores lógicos:**

``` JAVA
import java.util.Scanner;
//By: xeduark
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Ingresa tu edad: ");
        int numero = sc.nextInt();


                boolean esEstudiante = true;
                boolean esDiaLaboral = false;
                boolean esVacaciones = true;

                boolean resultado1 = (numero > 18) && esEstudiante;
                boolean resultado2 = esDiaLaboral || esVacaciones;
                boolean resultado3 = !esDiaLaboral;

                System.out.println("NO PUEDE ENTRAR: " + resultado1);
                System.out.println("PUEDE ENTRAR: " + resultado2);
                System.out.println("PUEDE ENTRAR: " + resultado3);
            }
        }


```
8. **Operador ternario:**

``` JAVA
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner a = new Scanner(System.in);

        System.out.println("Escribe un número:");
        double numero = a.nextDouble();

        if (numero == 0) {
            System.out.println("El número es neutro");
        } else if (numero < 0) {
            System.out.println("El número es negativo");
        } else {
            System.out.println("El número es positivo");
        }
    }
}


```






