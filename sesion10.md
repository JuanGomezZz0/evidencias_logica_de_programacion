<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


<!-- Su documentación aquí -->

# Actividad: Prueba, ejecución y explicación de ejercicios de lógica de programación.

- Selecciona dos ejercicios de la sesión 10, impleméntalos, ejecútalos y proporciona una explicación detallada de cada uno

# Solución: 

### Ejercicio 1
```
import java.util.Scanner;

public class IMC {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      double weight, height, imc;
      
      // Solicita el peso y la altura
      System.out.print("Ingrese su peso en kilogramos: ");
      weight = input.nextDouble();
      System.out.print("Ingrese su altura en metros: ");
      height = input.nextDouble();

      // Calcula el IMC
      imc = weight / (height * height);

      // Muestra el resultado en la consola
      System.out.printf("Su IMC es %.2f", imc);
   }
}
```
### Explicación: 

- El código proporcionado es un programa simple en Java que calcula el Índice de Masa Corporal (IMC) de una persona. El IMC es una medida comúnmente utilizada para estimar si una persona tiene un peso saludable en relación con su altura. El programa solicita al usuario que ingrese su peso en kilogramos y su altura en metros, realiza el cálculo del IMC y muestra el resultado en la consola.

En resumen, este programa solicita al usuario que ingrese su peso y altura, calcula el IMC y muestra el resultado en la consola. El IMC se utiliza para evaluar si una persona tiene un peso saludable en función de su altura, y este programa es un ejemplo simple de cómo realizar ese cálculo en Java.

### Ejercicio 2

```
import java.util.Scanner;

public class MRU {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      double velocidad, tiempo, distancia;
      
      // Solicita la velocidad y el tiempo
      System.out.print("Ingrese la velocidad en metros por segundo: ");
      velocidad = input.nextDouble();
      System.out.print("Ingrese el tiempo en segundos: ");
      tiempo = input.nextDouble();

      // Calcula la distancia recorrida
      distancia = velocidad * tiempo;

      // Muestra el resultado en la consola
      System.out.printf("La distancia recorrida es de %.2f metros.", distancia);
   }
}
```

### Explicación: 

- El código que proporcionaste es un programa en Java que calcula la distancia recorrida utilizando la fórmula del Movimiento Rectilíneo Uniforme (MRU). El MRU es un concepto de física que describe un movimiento en línea recta a velocidad constante. El programa solicita al usuario ingresar la velocidad en metros por segundo y el tiempo en segundos, luego calcula la distancia recorrida y muestra el resultado en la consola.

En resumen, este programa solicita al usuario que ingrese la velocidad y el tiempo, calcula la distancia recorrida según la fórmula del MRU y muestra el resultado en la consola. El MRU es un concepto fundamental en física y este programa ejemplifica cómo se puede calcular la distancia en un escenario de movimiento rectilíneo uniforme.


