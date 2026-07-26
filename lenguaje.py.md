[⬅️ Volver al Menú Principal](./README.md)

# 🟢 Solución e Implementación en Python

En esta sección se presenta el código desarrollado en el lenguaje **Python**, acompañado de su respectiva comprobación y salida en terminal.

---

## 💻 Código Fuente

```python
filas = 2
columnas = 3

def completar (matriz):
    for a in range(filas):
        for b in range(columnas):
            matriz[a][b]= int(input(f"COLOQUE EL DATO PARA SU POSICION [{a}][{b}]: "))

def suma (matriz1, matriz2 ,resultado):
    for a in range(filas):
        for b in range(columnas):
            resultado[a][b]=matriz1[a][b] + matriz2[a][b]

def resta (matriz1, matriz2 ,resultado):
    for a in range(filas):
        for b in range(columnas):
            resultado[a][b]=matriz1[a][b] - matriz2[a][b]

def multiplicacion (matriz1, matriz2 ,resultado):
    for a in range(filas):
        for b in range(columnas):
            resultado[a][b]=matriz1[a][b] * matriz2[a][b]

def mostrar(matriz):
    for a in range(filas):
        for b in range(columnas):
            print("[%3d]" % matriz[a][b], end=" ")
        print()

matrizA=[[0]*columnas for _ in range(filas)]
matrizB=[[0]*columnas for _ in range(filas)]
resSuma=[[0]*columnas for _ in range(filas)]
resResta=[[0]*columnas for _ in range(filas)]
resMult=[[0]*columnas for _ in range(filas)]


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
PS C:\Users\alvar\OneDrive\Datos adjuntos\Documentos\UNL ALVARO\TEORIA DE LA PROGRAMACION\PROGRAMAS PY> & C:\Users\alvar\AppData\Local\Programs\Python\Python313\python.exe "c:/Users/alvar/OneDrive/Datos adjuntos/Documentos/UNL ALVARO/TEORIA DE LA PROGRAMACION/PROGRAMAS PY/apefinal.py"

 OPERACIONES CON MATRICES DE 2 FILAS EN 3 COLUMNAS :


VALORES PARA LA MATRIZ A:

------------------------------

COLOQUE EL DATO PARA SU POSICION [0][0]: 45
COLOQUE EL DATO PARA SU POSICION [0][1]: 12
COLOQUE EL DATO PARA SU POSICION [0][2]: 67
COLOQUE EL DATO PARA SU POSICION [1][0]: 23
COLOQUE EL DATO PARA SU POSICION [1][1]: 11
COLOQUE EL DATO PARA SU POSICION [1][2]: 24

VALORES PARA LA MATRIZ B:

------------------------------

COLOQUE EL DATO PARA SU POSICION [0][0]: 20
COLOQUE EL DATO PARA SU POSICION [0][1]: 0
COLOQUE EL DATO PARA SU POSICION [0][2]: 14
COLOQUE EL DATO PARA SU POSICION [1][0]: 8
COLOQUE EL DATO PARA SU POSICION [1][1]: 9
COLOQUE EL DATO PARA SU POSICION [1][2]: 154

RESPUESTA SUMA:

[ 65] [ 12] [ 81] 
[ 31] [ 20] [178] 

RESPUESTA RESTA:

[ 25] [ 12] [ 53] 
[ 15] [  2] [-130] 

RESPUESTA MULTIPLICACION:

[900] [  0] [938] 
[184] [ 99] [3696] 
PS C:\Users\alvar\OneDrive\Datos adjuntos\Documentos\UNL ALVARO\TEORIA DE LA PROGRAMACION\PROGRAMAS PY> 
```

---
[⬅️ Volver al Menú Principal](./README.md)
