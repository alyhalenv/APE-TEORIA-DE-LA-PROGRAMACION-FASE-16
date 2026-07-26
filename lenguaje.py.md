[⬅️ Volver al Menú Principal](./README.md)

# 🟢 Solución e Implementación en Python

Implementación limpia en Python 3 utilizando inicialización segura mediante *list comprehensions*, f-strings para captura de datos y formateo `%3d` para la alineación tabular.

---

## 💻 Código Fuente

```python
filas = 2
columnas = 3


def completar(matriz):
    for a in range(filas):
        for b in range(columnas):
            matriz[a][b] = int(
                input(f"COLOQUE EL DATO PARA SU POSICION [{a}][{b}]: ")
            )


def suma(matriz1, matriz2, resultado):
    for a in range(filas):
        for b in range(columnas):
            resultado[a][b] = matriz1[a][b] + matriz2[a][b]


def resta(matriz1, matriz2, resultado):
    for a in range(filas):
        for b in range(columnas):
            resultado[a][b] = matriz1[a][b] - matriz2[a][b]


def multiplicacion(matriz1, matriz2, resultado):
    for a in range(filas):
        for b in range(columnas):
            resultado[a][b] = matriz1[a][b] * matriz2[a][b]


def mostrar(matriz):
    for a in range(filas):
        for b in range(columnas):
            print("[%3d]" % matriz[a][b], end=" ")
        print()


matrizA = [[0] * columnas for _ in range(filas)]
matrizB = [[0] * columnas for _ in range(filas)]
resSuma = [[0] * columnas for _ in range(filas)]
resResta = [[0] * columnas for _ in range(filas)]
resMult = [[0] * columnas for _ in range(filas)]

print("\n OPERACIONES CON MATRICES DE 2 FILAS EN 3 COLUMNAS :\n")

print("\nVALORES PARA LA MATRIZ A:\n")
print("------------------------------\n")
completar(matrizA)

print("\nVALORES PARA LA MATRIZ B:\n")
print("------------------------------\n")
completar(matrizB)

suma(matrizA, matrizB, resSuma)
resta(matrizA, matrizB, resResta)
multiplicacion(matrizA, matrizB, resMult)

print("\nRESPUESTA SUMA:\n")
mostrar(resSuma)

print("\nRESPUESTA RESTA:\n")
mostrar(resResta)

print("\nRESPUESTA MULTIPLICACION:\n")
mostrar(resMult)
```

---

## 🖥️ Verificación en Terminal

```text
 OPERACIONES CON MATRICES DE 2 FILAS EN 3 COLUMNAS :

VALORES PARA LA MATRIZ A:

------------------------------

COLOQUE EL DATO PARA SU POSICION [0][0]: 5
COLOQUE EL DATO PARA SU POSICION [0][1]: 2
...

RESPUESTA SUMA:

[  8] [  4] [  6] 
[  5] [  9] [  7] 

RESPUESTA RESTA:

[  2] [  0] [  2] 
[ -1] [  3] [  1] 

RESPUESTA MULTIPLICACION:

[ 15] [  4] [  8] 
[  6] [ 18] [ 12] 
```

---
[⬅️ Volver al Menú Principal](./README.md)
