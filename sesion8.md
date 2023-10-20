<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


<!-- Su documentación aquí -->

# Actividad: Ejecicios de métodos en Java

### Implementar los siguientes métodos:

- Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.
- Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.
- Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.
- Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.
- Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

# Solución: 

### Mayor de dos números.

```
public class TEST {

    public static int obtenerMayor(int numero1, int numero2) {
        if (numero1 > numero2) {
            return numero1;
        } else {
            return numero2;
        }
    }

    public static void main(String[] args) {
        int numero1 = 10;
        int numero2 = 20;
        int resultado = obtenerMayor(numero1, numero2);
        System.out.println("El número mayor entre " + numero1 + " y " + numero2 + " es: " + resultado);
    }
}

```

### Contador de vocales

```
public class TEST {

    public static int contarVocales(String texto) {
        int contador = 0;
        // Convertir la cadena a minúsculas para simplificar la comparación
        texto = texto.toLowerCase();

        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
            if (caracter == 'a' || caracter == 'e' || caracter == 'i' || caracter == 'o' || caracter == 'u') {
                contador++;
            }
        }

        return contador;
    }

    public static void main(String[] args) {
        String texto = "Hola, este es un ejemplo de conteo de vocales.";
        int cantidadVocales = contarVocales(texto);
        System.out.println("El número de vocales en la cadena es: " + cantidadVocales);
    }
}

```
### Intercambio de mayúsculas y minúsculas. 

```
public class TEST {

    public static String cambiarMayusculasMinisculas(String texto) {
        StringBuilder resultado = new StringBuilder();

        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
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
        String texto = "Hola, Este Es Un Ejemplo De Cambio De Mayúsculas A Minúsculas.";
        String resultado = cambiarMayusculasMinisculas(texto);
        System.out.println("Texto original: " + texto);
        System.out.println("Texto con mayúsculas y minúsculas intercambiadas: " + resultado);
    }
}

```

### Cantidad de palabras en texto.

```
public class TEST {

    public static int contarPalabras(String texto) {
        // Dividir la cadena en palabras utilizando espacios en blanco como separadores
        String[] palabras = texto.split("\\s+");
        return palabras.length;
    }

    public static void main(String[] args) {
        String texto = "Este es un ejemplo de conteo de palabras en Java.";
        int cantidadPalabras = contarPalabras(texto);
        System.out.println("El número de palabras en la cadena es: " + cantidadPalabras);
    }
}
```

### Cadena en orden alfabético

```
import java.util.Arrays;

public class TEST {

    public static String ordenarPalabrasAlfabeticamente(String texto) {
        // Dividir la cadena en palabras utilizando espacios en blanco como separadores
        String[] palabras = texto.split("\\s+");
        
        // Ordenar las palabras alfabéticamente
        Arrays.sort(palabras);
        
        // Unir las palabras ordenadas en una nueva cadena
        String resultado = String.join(" ", palabras);
        
        return resultado;
    }

    public static void main(String[] args) {
        String texto = "Esta es una cadena de ejemplo con palabras desordenadas";
        String textoOrdenado = ordenarPalabrasAlfabeticamente(texto);
        System.out.println("Texto original: " + texto);
        System.out.println("Texto con palabras ordenadas alfabéticamente: " + textoOrdenado);
    }
}

```