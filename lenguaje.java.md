[⬅️ Volver al Menú Principal](./README.md)

# 🔴 Solución e Implementación en Java

Implementación orientada a objetos estructurada mediante métodos estáticos, la clase `Scanner` para lectura de datos y `System.out.printf` para alineación visual.

---

## 💻 Código Fuente

```java
import java.util.Scanner;
public class operacionesMatrices{
    //Constantes definidas
    public static final int filas = 2;
    public static final int columnas = 3;

    public static void completar(int[][] matriz){
        Scanner entrada = new Scanner(System.in);
        for(int a = 0;a < filas;a++){
            for(int b = 0; b < columnas; b++){
                System.out.printf("COLOQUE EL DATO PARA SU POSICION[%d][%d]: ",a,b);
                matriz[a][b] = entrada.nextInt();
            }
        }
    }

    public static void suma(int[][] matriz1, int[][] matriz2, int[][]resultado){
        for (int a = 0; a < filas; a++){     
            for (int b = 0; b < columnas; b++){
                resultado[a][b] = matriz1[a][b] + matriz2[a][b];
            }
        }
    }

    public static void resta(int[][] matriz1, int[][] matriz2, int[][]resultado){
        for (int a = 0; a < filas; a++){     
            for (int b = 0; b < columnas; b++){
                resultado[a][b] = matriz1[a][b] - matriz2[a][b];
            }
        }
    }
    public static void multiplicar(int[][] matriz1, int[][] matriz2, int[][]resultado){
        for (int a = 0; a < filas; a++){     
            for (int b = 0; b < columnas; b++){
                resultado[a][b] = matriz1[a][b] * matriz2[a][b];
            }
        }
    }
    public static void mostrar(int[][]matriz){
        for (int a = 0; a < filas; a++){     
            for (int b = 0; b < columnas; b++){
                System.out.printf("[%d]\t", matriz[a][b]);
            }
        System.out.print("\n");
    }   
    }


    public static void main(String[] args){
        int[][] matrizA = new int [filas][columnas];
        int[][] matrizB = new int [filas][columnas];
        int[][]resSuma = new int [filas][columnas];
        int[][]resResta = new int [filas][columnas];
        int[][]resMult = new int [filas][columnas];
        
        System.out.print("\n OPERACIONES CON MATRICES DE 2 FILAS EN 3 COLUMNAS: \n");

        System.out.print("\nVALORES PARA LA MATRIZ A:\n");
        System.out.print("------------------------------\n");
        completar(matrizA);

        System.out.print("\nVALORES PARA LA MATRIZ B:\n");
        System.out.print("------------------------------\n");
        completar(matrizB);

        suma(matrizA, matrizB, resSuma);
        resta(matrizA, matrizB, resResta);
        multiplicar(matrizA, matrizB, resMult);

        System.out.print("\nRESPUESTA SUMA:\n");
        mostrar(resSuma);

        System.out.print("\nRESPUESTA RESTA:\n");
        mostrar(resResta);

        System.out.print("\nRESPUESTA MULTIPLICACION:\n");
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
