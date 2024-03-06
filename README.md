# Repo_2
## Resultados reto #3
>1.Plantear el algoritmo para obtener los números primos hasta n, usando pseudocódigo y diagramas de flujo.

### Pseudocódigo
```pseudocode
n : entero
i : entero 
j : entero
inicio 
i :=2
Mientras (i< n) hacer
  j:=2
  Mientras (j<=i/2) hacer
   si el modulo(i,j) ==0 
      escribir  ("j no es primo") 
   sino 
      escribir ("j es primo")
   j := j + 1
i := i + 1
Fin
```
### Diagrama de flujo 
```mermaid
flowchart TD
A(Inicio)-->B[número entero n]
B-->C[i := 2]
C-->D[j := 2]
D-->E{j <= i / 2?}
E-->|si|F{i % j == 0?}
E-->|no|I
F-->|no|G[No es primo]
F-->|si|H[Es primo]
G-->I[i += 1]
H-->I
I-->J[i < n?]
J-->|si|K[j+= 1]
K-->E
J-->|no|L[Fin]
```
>2.Revise el procedimiento matemático para hallar raíces cuadradas (son divisiones y restas), plantee el algoritmo en pseudocódigo y en diagrama de flujo.

### Pseudocódigo
```pseudocode
Inicio
n : entero
i : entero
p : entero 
lista de divisores primos de n (i,...)
lista de p veces que se utiliza cada divisor primo

 Mientras (n > 1)
        si (n % i) == 0
            Aumentar en 1 la cantidad de veces que se utiliza i
            n = n / i
        sino
         i = i + 1
raiz = i**( p / 2), por cada divisores primo que se utilizo
Fin
```
###Diagrama de flujo
```mermaid
flowchart TD
A(inicio)-->B[lista de divisores primos de n]
B-->C[lista de p veces que se utiliza cada divisor primo]
C-->D{¿n>1?}
D-->|si|E{¿n % i == 0?}
E-->|si|F[Aumentar en 1 la cantidad de veces que se utiliza i]
F-->G[n = n / i]
G-->D
E-->|no|H[i = i + 1]
D-->|no|I["raiz = i**( p / 2)"]
I-->J(Fin)
```


