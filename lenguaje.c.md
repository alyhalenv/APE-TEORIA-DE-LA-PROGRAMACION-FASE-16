[⬅️ Volver al Menú Principal](./README.md)

# 🔵 Solución e Implementación en C

Implementación de matrices de $2 \times 3$ utilizando arrays bidimensionales nativos, paso por referencia e impresión formateada en consola mediante `printf`.

---

## 💻 Código Fuente

```c
#include <stdio.h>

#define FILAS 2
#define COLUMNAS 3

void completar(int matriz[FILAS][COLUMNAS]) {
    for(int a = 0; a < FILAS; a++) {
        for(int b = 0; b < COLUMNAS; b++) {
            printf("COLOQUE EL DATO PARA SU POSICION [%d][%d]: ", a, b);
            scanf("%d", &matriz[a][b]);
        }
    }
}

void suma(int matriz1[FILAS][COLUMNAS], int matriz2[FILAS][COLUMNAS], int resultado[FILAS][COLUMNAS]) {
    for(int a = 0; a < FILAS; a++) {
        for(int b = 0; b < COLUMNAS; b++) {
            resultado[a][b] = matriz1[a][b] + matriz2[a][b];
        }
    }
}

void resta(int matriz1[FILAS][COLUMNAS], int matriz2[FILAS][COLUMNAS], int resultado[FILAS][COLUMNAS]) {
    for(int a = 0; a < FILAS; a++) {
        for(int b = 0; b < COLUMNAS; b++) {
            resultado[a][b] = matriz1[a][b] - matriz2[a][b];
        }
    }
}

void multiplicacion(int matriz1[FILAS][COLUMNAS], int matriz2[FILAS][COLUMNAS], int resultado[FILAS][COLUMNAS]) {
    for(int a = 0; a < FILAS; a++) {
        for(int b = 0; b < COLUMNAS; b++) {
            resultado[a][b] = matriz1[a][b] * matriz2[a][b];
        }
    }
}

void mostrar(int matriz[FILAS][COLUMNAS]) {
    for(int a = 0; a < FILAS; a++) {
        for(int b = 0; b < COLUMNAS; b++) {
            printf("[%3d]", matriz[a][b]);
        }
        printf("\n");
    }
}

int main() {
    int matrizA[FILAS][COLUMNAS], matrizB[FILAS][COLUMNAS];
    int resSuma[FILAS][COLUMNAS], resResta[FILAS][COLUMNAS], resMult[FILAS][COLUMNAS];

    printf("\n OPERACIONES CON MATRICES DE 2 FILAS EN 3 COLUMNAS :\n\n");
    printf("VALORES PARA LA MATRIZ A:\n------------------------------\n");
    completar(matrizA);

    printf("\nVALORES PARA LA MATRIZ B:\n------------------------------\n");
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
 OPERACIONES CON MATRICES DE 2 FILAS EN 3 COLUMNAS :

VALORES PARA LA MATRIZ A:
------------------------------
COLOQUE EL DATO PARA SU POSICION [0][0]: 5
COLOQUE EL DATO PARA SU POSICION [0][1]: 2
COLOQUE EL DATO PARA SU POSICION [0][2]: 4
COLOQUE EL DATO PARA SU POSICION [1][0]: 2
COLOQUE EL DATO PARA SU POSICION [1][1]: 6
COLOQUE EL DATO PARA SU POSICION [1][2]: 4

VALORES PARA LA MATRIZ B:
------------------------------
COLOQUE EL DATO PARA SU POSICION [0][0]: 3
COLOQUE EL DATO PARA SU POSICION [0][1]: 2
COLOQUE EL DATO PARA SU POSICION [0][2]: 2
COLOQUE EL DATO PARA SU POSICION [1][0]: 3
COLOQUE EL DATO PARA SU POSICION [1][1]: 3
COLOQUE EL DATO PARA SU POSICION [1][2]: 3

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
