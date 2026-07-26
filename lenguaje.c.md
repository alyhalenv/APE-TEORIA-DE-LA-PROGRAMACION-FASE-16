[⬅️ Volver al Menú Principal](./README.md)

# 🔵 Solución e Implementación en C

En esta sección se presenta el código desarrollado en el lenguaje **C**, acompañado de su respectiva comprobación y salida en terminal.

---

## 💻 Código Fuente

```c
#include <stdio.h>
const int filas = 2;
const int columnas = 3;

void completar(int matriz[filas][columnas]){
    for (int a = 0; a < filas; a++){     
        for (int b = 0; b < columnas; b++){  
            printf("COLOQUE EL DATO PARA SU POSICION [%i][%i]: ", a, b);
            scanf("%i", &matriz[a][b]);
        } 
    }
}

void suma(int matriz1[filas][columnas], int matriz2[filas][columnas], int resultado[filas][columnas]){
    for (int a = 0; a < filas; a++){     
        for (int b = 0; b < columnas; b++){
            resultado[a][b] = matriz1[a][b] + matriz2[a][b];
        }
    }
}

void resta(int matriz1[filas][columnas], int matriz2[filas][columnas], int resultado[filas][columnas]){
    for (int a = 0; a < filas; a++){     
        for (int b = 0; b < columnas; b++){
            resultado[a][b] = matriz1[a][b] - matriz2[a][b];
        }
    }
}

void multiplicacion(int matriz1[filas][columnas], int matriz2[filas][columnas], int resultado[filas][columnas]){
    for (int a = 0; a < filas; a++){     
        for (int b = 0; b < columnas; b++){
            resultado[a][b] = matriz1[a][b] * matriz2[a][b];
        }
    }
}

void mostrar(int matriz[filas][columnas]){
    for (int a = 0; a < filas; a++){     
        for (int b = 0; b < columnas; b++){
            printf("[%i]\t", matriz[a][b]);
        }
        printf("\n");
    }
}

int main() {
    int matrizA[filas][columnas], matrizB[filas][columnas];
    int resSuma[filas][columnas], resResta[filas][columnas], resMult[filas][columnas];

    printf("\n OPERACIONES CON MATRICES DE 2 FILAS EN 3 COLUMNAS :\n");
    
    printf("\nVALORES PARA LA MATRIZ A:\n");
    printf("------------------------------\n");
    completar(matrizA);
    
    printf("\nVALORES PARA LA MATRIZ B:\n");
    printf("------------------------------\n");
    completar(matrizB);
    
    suma(matrizA, matrizB, resSuma);
    resta(matrizA, matrizB, resResta);
    multiplicacion(matrizA, matrizB, resMult);
    
    printf("\nRESPUESTA SUMA:\n");
    mostrar(resSuma);

    printf("\nRESPUESTA RESTA:\n");
    mostrar(resResta);

    printf("\nRESPUESTA MULTIPLICACION:\n");
    mostrar(resMult);

    return 0;
}
```

---

## 🖥️ Verificación en Terminal

```text
PS C:\Users\alvar\OneDrive\Datos adjuntos\Documentos\UNL ALVARO\TEORIA DE LA PROGRAMACION\PROGRAMAS C> gcc apefinal.c -o apefinal                           
PS C:\Users\alvar\OneDrive\Datos adjuntos\Documentos\UNL ALVARO\TEORIA DE LA PROGRAMACION\PROGRAMAS C> .\apefinal.exe                                       
                                                                                                                  
 OPERACIONES CON MATRICES DE 2 FILAS EN 3 COLUMNAS :

VALORES PARA LA MATRIZ A:
------------------------------
COLOQUE EL DATO PARA SU POSICION [0][0]: 6 
COLOQUE EL DATO PARA SU POSICION [0][1]: 5
COLOQUE EL DATO PARA SU POSICION [0][2]: 4
COLOQUE EL DATO PARA SU POSICION [1][0]: 3
COLOQUE EL DATO PARA SU POSICION [1][1]: 2
COLOQUE EL DATO PARA SU POSICION [1][2]: 1

VALORES PARA LA MATRIZ B:
------------------------------
COLOQUE EL DATO PARA SU POSICION [0][0]: 1
COLOQUE EL DATO PARA SU POSICION [0][1]: 2
COLOQUE EL DATO PARA SU POSICION [0][2]: 3
COLOQUE EL DATO PARA SU POSICION [1][0]: 4
COLOQUE EL DATO PARA SU POSICION [1][1]: 5
COLOQUE EL DATO PARA SU POSICION [1][2]: 6

RESPUESTA SUMA:
[7]     [7]     [7]
[7]     [7]     [7]

RESPUESTA RESTA:
[5]     [3]     [1]
[-1]    [-3]    [-5]

RESPUESTA MULTIPLICACION:
[6]     [10]    [12]
[12]    [10]    [6]
PS C:\Users\alvar\OneDrive\Datos adjuntos\Documentos\UNL ALVARO\TEORIA DE LA PROGRAMACION\PROGRAMAS C> 
```

---
[⬅️ Volver al Menú Principal](./README.md)
