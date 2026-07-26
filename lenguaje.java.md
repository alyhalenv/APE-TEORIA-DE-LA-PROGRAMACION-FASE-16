[⬅️ Volver al Menú Principal](./README.md)

# 🔴 Solución e Implementación en Java

Implementación orientada a objetos estructurada mediante métodos estáticos, la clase `Scanner` para lectura de datos y `System.out.printf` para alineación visual.

---

## 💻 Código Fuente

```java
import java.util.Scanner;

public class lenguaje {
    static final int FILAS = 2;
    static final int COLUMNAS = 3;
    static Scanner scanner = new Scanner(System.in);

    public static void completar(int[][] matriz) {
        for (int a = 0; a < FILAS; a++) {
            for (int b = 0; b < COLUMNAS; b++) {
                System.out.print("COLOQUE EL DATO PARA SU POSICION [" + a + "][" + b + "]: ");
                matriz[a][b] = scanner.nextInt();
            }
        }
    }

    public static void suma(int[][] matriz1, int[][] matriz2, int[][] resultado) {
        for (int a = 0; a < FILAS; a++) {
            for (int b = 0; b < COLUMNAS; b++) {
                resultado[a][b] = matriz1[a][b] + matriz2[a][b];
            }
        }
    }

    public static void resta(int[][] matriz1, int[][] matriz2, int[][] resultado) {
        for (int a = 0; a < FILAS; a++) {
            for (int b = 0; b < COLUMNAS; b++) {
                resultado[a][b] = matriz1[a][b] - matriz2[a][b];
            }
        }
    }

    public static void multiplicacion(int[][] matriz1, int[][] matriz2, int[][] resultado) {
        for (int a = 0; a < FILAS; a++) {
            for (int b = 0; b < COLUMNAS; b++) {
                resultado[a][b] = matriz1[a][b] * matriz2[a][b];
            }
        }
    }

    public static void mostrar(int[][] matriz) {
        for (int a = 0; a < FILAS; a++) {
            for (int b = 0; b < COLUMNAS; b++) {
                System.out.printf("[%3d]", matriz[a][b]);
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {
        int[][] matrizA = new int[FILAS][COLUMNAS];
        int[][] matrizB = new int[FILAS][COLUMNAS];
        int[][] resSuma = new int[FILAS][COLUMNAS];
        int[][] resResta = new int[FILAS][COLUMNAS];
        int[][] resMult = new int[FILAS][COLUMNAS];

        System.out.println("\n OPERACIONES CON MATRICES DE 2 FILAS EN 3 COLUMNAS :\n");
        System.out.println("VALORES PARA LA MATRIZ A:\n------------------------------");
        completar(matrizA);

        System.out.println("\nVALORES PARA LA MATRIZ B:\n------------------------------");
        completar(matrizB);

        suma(matrizA, matrizB, resSuma);
        resta(matrizA, matrizB, resResta);
        multiplicacion(matrizA, matrizB, resMult);

        System.out.println("\nRESPUESTA SUMA:");
        mostrar(resSuma);

        System.out.println("\nRESPUESTA RESTA:");
        mostrar(resResta);

        System.out.println("\nRESPUESTA MULTIPLICACION:");
        mostrar(resMult);
    }
}
```

---

## 🖥️ Verificación en Terminal

```text
 OPERACIONES CON MATRICES DE 2 FILAS EN 3 COLUMNAS :

VALORES PARA LA MATRIZ A:
------------------------------
COLOQUE EL DATO PARA SU POSICION [0][0]: 5
COLOQUE EL DATO PARA SU POSICION [0][1]: 2
COLOQUE EL DATO PARA SU POSICION [0][2]: 4
...

RESPUESTA SUMA:
[  8][  4][  6]
[  5][  9][  7]

RESPUESTA RESTA:
[  2][  0][  2]
[ -1][  3][  1]

RESPUESTA MULTIPLICACION:
[ 15][  4][  8]
[  6][ 18][ 12]
```

---
[⬅️ Volver al Menú Principal](./README.md)
