<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 7 


<!-- Su documentación aquí -->

# Actividad: Ejecicios Array - ArrayList

1. En parejas, probar, analizar y explicar el funcionamiento de los siguientes ejemplos de Array y ArrayList.

### Ejemplo Array

```
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

### Ejemplo de Array-list:

```
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

### Crear un ejemplo de Array y otro de ArrayList para visualizar sus diferencias.

# Array

```
public class Actividad7 {

    public static void main(String[] args) {
        // Declaración y creación de un array de calificaciones
        double[] calificaciones = {3.0, 2.7, 2.6, 3.9, 4.5};

        // Calcula el promedio de las calificaciones
        double promedio = calcularPromedio(calificaciones);

        // Muestra el resultado
        System.out.println("Calificaciones:");
        for (int i = 0; i < calificaciones.length; i++) {
            System.out.println("Estudiante " + (i + 1) + ": " + calificaciones[i]);
        }

        System.out.println("Promedio: " + promedio);
    }

    public static double calcularPromedio(double[] calificaciones) {
        double suma = 0;

        // Suma todas las calificaciones en el array
        for (int i = 0; i < calificaciones.length; i++) {
            suma += calificaciones[i];
        }

        // Calcula el promedio dividiendo la suma por la cantidad de calificaciones
        double promedio = suma / calificaciones.length;

        return promedio;
    }
}
```

# Array-list

```
public class Actividad7 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        ArrayList<String> estudiantes = new ArrayList<String>();

        while (true) {
            System.out.print("Ingrese el nombre del estudiante (o 'salir' para terminar): ");
            String nombre = input.nextLine();

            if (nombre.equalsIgnoreCase("salir")) {
                break;
            }

            estudiantes.add(nombre);
        }

        // Mostrar los nombres de los estudiantes
        System.out.println("Nombres de estudiantes:");
        for (String estudiante : estudiantes) {
            System.out.println(estudiante);
        }
    }
}
```







