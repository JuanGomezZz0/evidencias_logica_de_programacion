<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 11 


<!-- Su documentación aquí -->

# Actividad: Ejercicios de Lógica de Programación.

- Basándose en el algoritmo 1 de la sesión 11, aplicar la siguiente variante: Dado un conjunto de números enteros, se debe determinar si existe algún número que aparezca más de una vez. Si es así, se deben imprimir todos los números que aparezcan más de una vez.

- Desarrollar un algoritmo que realice la conversión de binario a decimal.

# Solución

### Ejercicio 1

```

public class ActividadSesion11 {


    public static void main(String[] args) {
       
        int[] numeros = {6, 2, 2, 5, 3, 6, 7, 8, 9, 10};

  
        List<Integer> numerosRepetidos = new ArrayList<>();

        for (int i = 0; i < numeros.length; i++) {
            for (int j = i + 1; j < numeros.length; j++) {
                if (numeros[i] == numeros[j] && !numerosRepetidos.contains(numeros[i])) {
                    numerosRepetidos.add(numeros[i]);
                }
            }
        }

        if (!numerosRepetidos.isEmpty()) {
            System.out.println("Los números repetidos son: " + numerosRepetidos);
        } else {
            System.out.println("No hay ningún número repetido");
        }
    }
}
```

### Actividad 2

```
public class TEST {
    public static void main(String[] args) {
        String binario = "110101"; // Cambia esto por tu número binario

        int decimal = binarioADecimal(binario);
        System.out.println("El número binario " + binario + " es equivalente a " + decimal + " en decimal.");
    }

    public static int binarioADecimal(String binario) {
        int decimal = 0;
        int longitud = binario.length();

        for (int i = 0; i < longitud; i++) {
            char digito = binario.charAt(i);
            int valor = Character.getNumericValue(digito);
            int exponente = longitud - 1 - i; // Exponente de 2

            // Multiplica el dígito por 2 elevado a la potencia correspondiente y suma al resultado.
            decimal += valor * Math.pow(2, exponente);
        }

        return decimal;
    }
}

```