[⬅️ Volver al Menú Principal](./README.md)

# 🔴 Solución e Implementación en Java

Implementación orientada a objetos estructurada mediante métodos estáticos, la clase `Scanner` para lectura de datos y `System.out.printf` para alineación visual.

---

## 💻 Código Fuente

```java
import java.util.Scanner;
public class operacionesMatrices{

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
PS C:\Users\alvar\OneDrive\Datos adjuntos\Documentos\UNL ALVARO\TEORIA DE LA PROGRAMACION\PROGRAMAS JAVA> javac operacionesMatrices.java
PS C:\Users\alvar\OneDrive\Datos adjuntos\Documentos\UNL ALVARO\TEORIA DE LA PROGRAMACION\PROGRAMAS JAVA> java operacionesMatrices      

 OPERACIONES CON MATRICES DE 2 FILAS EN 3 COLUMNAS: 

VALORES PARA LA MATRIZ A:
------------------------------
COLOQUE EL DATO PARA SU POSICION[0][0]: 10
COLOQUE EL DATO PARA SU POSICION[0][1]: 11
COLOQUE EL DATO PARA SU POSICION[0][2]: 12
COLOQUE EL DATO PARA SU POSICION[1][0]: 13
COLOQUE EL DATO PARA SU POSICION[1][1]: 14
COLOQUE EL DATO PARA SU POSICION[1][2]: 15

VALORES PARA LA MATRIZ B:
------------------------------
COLOQUE EL DATO PARA SU POSICION[0][0]: 15
COLOQUE EL DATO PARA SU POSICION[0][1]: 14
COLOQUE EL DATO PARA SU POSICION[0][2]: 13
COLOQUE EL DATO PARA SU POSICION[1][0]: 12
COLOQUE EL DATO PARA SU POSICION[1][1]: 11
COLOQUE EL DATO PARA SU POSICION[1][2]: 10

RESPUESTA SUMA:
[25]    [25]    [25]
[25]    [25]    [25]

RESPUESTA RESTA:
[-5]    [-3]    [-1]
[1]     [3]     [5]

RESPUESTA MULTIPLICACION:
[150]   [154]   [156]
[156]   [154]   [150]
PS C:\Users\alvar\OneDrive\Datos adjuntos\Documentos\UNL ALVARO\TEORIA DE LA PROGRAMACION\PROGRAMAS JAVA> 
```

---
[⬅️ Volver al Menú Principal](./README.md)
