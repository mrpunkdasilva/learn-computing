# Matrizes e sistemas de equações

## Introdução

Matriz é uma tabela que contem **elementos¹** e são dados por $i$ itens na horizontal e $j$ itens na vertical  

> ✏️ Esses elementos, são chamados também de entradas ou elementos da matriz

### Notação de matrizes

Como toda linguagem, a matemática possui sua sintaxe para todos os seus objetos, então para criarmos matrizes temos que seguir algumas regras;

**Regras básicas:**
- Para nomear matrizes damos uma letra maiúsculaMatrizes e sistemas de equações-ex2.png
- Os elementos da matriz são denotados por letras minusculas (caso formos representar ps elementos com letras)
- Devemos usar '()' (parenteses) e '[]' (colchetes) para definir o bloco da matriz - inicio e fim. Existem outras formas

**Exemplo:** 

$$
M =  
\begin{pmatrix}
1 2 \\
3 4 \\
5 6\\
\end{pmatrix}
$$

$$
M =  
\begin{bmatrix}
1 2 \\
3 4 \\
5 6\\
\end{bmatrix}
$$

$$
M =  
\begin{Bmatrix}
1 2 \\
3 4 \\
5 6\\
\end{Bmatrix}
$$

$$
M =  
\begin{pmatrix}
a_{ij} \text{  }\text{ } \dots \text{  }\text{ } b_{ij} \\
c_{ij} \text{  }\text{ } \dots \text{  }\text{ } d_{ij}  \\
\end{pmatrix}
$$

$$
M_{ij} =  
\begin{pmatrix}
a_{ij} \text{  }\text{ } \dots \text{  }\text{ } b_{ij} \\
c_{ij} \text{  }\text{ } \dots \text{  }\text{ } d_{ij}  \\
\end{pmatrix}
$$

Para definirmos a estrutura dessa tabela, definimos duas partes:
- **Linhas (horizontal)** - são os segmentos divididos na ***horizontal***
![[Matrizes e sistemas de equações-ex1.png]]

- **Colunas (vertical)** - são os segmentos divididos na ***vertical***
![[Matrizes e sistemas de equações-ex2.png]]


> 💡 Os elementos de uma matriz podem ser números: reais, complexos; funções; ou até mesmo outras matrizes


---

## Conceitos base

### 1. Igualdade
Uma matriz **só** será igual a outra, caso tenha a **mesma ordem⁽²⁾** e os **elementos são correspondentes** ou seja:

> $$
 M_{ij} = V_{rs} \Rightarrow i = r \text{ e } j = s \text{ e } a_{ij} = b_{ij} \text{ , }  l \leq i \leq m, l \leq j \leq n 
$$

> A **ordem** de uma matriz é o número de linhas 

Lendo isso podemos dizer que: 
- As matrizes $M_{ij} = V_{rs}$ só serão iguais se:
	1. Número de linhas de M ($i$) for igual ao número de linhas de V ($r$)
	2. Número de colunas de M ($j$) for igual ao número de colunas de V ($s$)
	3. Caso cada elemento da matriz M seja correspondente ao elementos da matriz V, devendo eles estarem nos mesmo indices ($ij$) 
	4. 
**Gatoxemplo:**
> ![[Matrizes e sistemas de equações-exg2.png]]

No exemplo temos as matrizes M e V que ao compararmos sua ordem que é de 2x2, 2 linhas por 2 colunas, e compararmos cada elementos das duas com base nos indices vemos que elas são iguais.

---

#### Algumas matrizes especiais
>![[kitten-love.gif]]

##### Matriz Quadrada
Possui o mesmo número de linhas e colunas.

**Exemplo:**
Nessa matriz chamada M temos o seguinte

$$
M_{(2\times2)} =  
\begin{pmatrix}
a_{ll} \text{ } \dots \text{  } a_{\ln} \\
\vdots \text{ } \text{ } \ddots \text{ }\text{ } \vdots\\
a_{nl} \text{ } \text{ } \dots \text{ }  \text{  } \text{ } a_{nn} \\
\end{pmatrix}
$$

> ✏️ Chamamos de diagonal principal aos elementos: 
> $a_{ij}$ com $i=j \in \{1,\dots, n\}$ 
> - Ou seja, todos os elementos que estão no índice em que a **linha** e a **coluna** possui **mesmo valor**

##### Matriz Identidade de Ordem $n$
É a matriz quadrada $M$ de ordem $n$ que tem todos os seus elementos da *diagonal principal* iguais a 1 e o resto igual a zero;
**Exemplo:**

$$
M =  
\begin{pmatrix}
1 0 0 \\
0 1 0 \\
0 0 1 
\end{pmatrix}
$$

##### Matriz Nula
É a matriz de ordem $m \times n$ em que todos os elementos são zero
**Exemplo:**

$$
M =  
\begin{pmatrix}
0 0 0 \\
0 0 0 \\
0 0 0 
\end{pmatrix}
$$

##### Matriz Linha 
É a matriz que é dada pela ordem: $1 \times n$, onde:
- O número de linhas é sempre um
- O número de colunas varia (n)
**Exemplo:**
  
$$
M =  
\begin{pmatrix}
0 0 0 0 0 0 
\end{pmatrix}
$$
##### Matriz Coluna 
É a matriz que é dada pela ordem: $m \times 1$, onde:
- O número de colunas é sempre um
- O número de linhas varia (m)
**Exemplo:**
  
$$
M =  
\begin{bmatrix}
0  \\
0  \\
0  \\
0  \\
0  \\
0 
\end{bmatrix}
$$

##### Matriz Diagonal
É uma matriz quadrada, em que todos os elementos menos os da diagonal principal são nulos (zero)
**Exemplo:**

$$
M =  
\begin{bmatrix}
1 0 0 \\
0 2 0 \\
0 0 3 
\end{bmatrix}
$$

##### Matriz Transposta de uma matriz dada
É quando pegamos uma matriz e a invertemos, ou seja:
- O valor das linhas se tornam das colunas
- O valor das colunas se tornam linhas
**Exemplo:**
  
$$
M_{(3 \times 2)} =  
\begin{bmatrix}
1 2  \\
3 4  \\
5 6  
\end{bmatrix} \Longrightarrow M^{t} = M^{t}_{(2 \times 3)} =
\begin{bmatrix}
1 3 5 \\
2 4 6
\end{bmatrix}
$$

##### Matriz Simétrica
Ela será simétrica caso:
- Temos uma matriz $M$ quadrada
- A matriz transposta de $M$ seja igual a matriz original
**Exemplo:**
  
$$
M_{(2 \times 2)} =  
\begin{bmatrix}
1 0  \\
0 4  \\  
\end{bmatrix} \Longrightarrow M^{t} = M^{t}_{(2 \times 2)} =
\begin{bmatrix}
1 0 \\
0 4
\end{bmatrix}
$$
Como a matriz $M = M^{t}$ então ela temos uma simétrica

##### Matriz Antissimétrica
É quando fazemos a transposta, depois fazemos o oposto e então se a matriz resultante tiver a sua diagonal principal nula e se a oposta for igual a transposta
**Exemplo:**

$$
M_{(2 \times 2)} =  
\begin{bmatrix}
 0 \text{  } \text{  }\text{ }\text{  }\text{  }2  \\
-2 \text{  }\text{  }\text{  } 0   \\  
\end{bmatrix} \Longrightarrow M^{t} = M^{t}_{(2 \times 2)} =
\begin{bmatrix}
 0 \text{  }\text{  }\text{  }\text{  } 2 \\
-2 \text{  }\text{  } 0 
\end{bmatrix} \Longrightarrow -M =
\begin{bmatrix}
0 \text{  }-2 \\
2 \text{  }0 
\end{bmatrix}
$$

---

### 2. Operações com matrizes
