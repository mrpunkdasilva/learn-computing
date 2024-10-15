### Table of Contents

- [Dicionario Base de Função](#dicionario-base-de-fun%C3%A7%C3%A3o)
	- [Simbologia da função:](#simbologia-da-fun%C3%A7%C3%A3o)
		- [Elementos da função:](#elementos-da-fun%C3%A7%C3%A3o)
		- [Definição](#defini%C3%A7%C3%A3o)
- [Casos](#casos)
	- [Casos em que será função:](#casos-em-que-ser%C3%A1-fun%C3%A7%C3%A3o)
	- [Casos em que não será função:](#casos-em-que-n%C3%A3o-ser%C3%A1-fun%C3%A7%C3%A3o)
- [Tipos de Funções](#tipos-de-fun%C3%A7%C3%B5es)
	- [Injetora](#injetora)
	- [Sobrejetora](#sobrejetora)
	- [Bijetora](#bijetora)
	- [Exemplos](#exemplos)
- [Encontrando os elementos:](#encontrando-os-elementos)
	- [Encontrando Domínio](#encontrando-dom%C3%ADnio)
		- [Exemplos:](#exemplos)


---

# Função 

Uma função é um tipo de relação com alguma regra especifica entre elementos de um conjunto.

```
				|--------|
	ENTRADA ->  |  f(x)  | -> Saída
				|--------|

- Entrada é o dominio
- Saída é a imagem
``` 
 

---

## Dicionario Base de Função
Algumas letrinhas do alfabeto de função, afinal, precisamos primeiro entender algumas letras para depois aprender a falar uma palavra.

### Simbologia da função:
- Usamo um `f` minusculo e uma variável entre parenteses (normalmente se usa `x`)
![[Pasted image 20240916115220.png]]

#### Elementos da função:
- ***Dominio*** -> é a entrada da função, todos os valores de A
- ***Imagem*** -> a saída da função, todos os valores de B que estão
- ***Contradominio*** -> são todos os elementos de B
	- Tanto os elementos que se conectam com A como aqueles que não se conectam
![[Pasted image 20240916115753.png]]

#### Definição

>  Isto é definir uma função:

$$f(x) = 2x²$$

![[Pasted image 20240916115922.png]]	

---

## Casos

### Casos em que será função:
1. Só será função quando todos os elementos do dominio estão ligados com o contradomínio:
![[Pasted image 20240916105628.png]]

2. Poderá ser também mesmo que sobre ou fique algum elemento do contradominio sem estar relacionado com algum elemento do dominio
![[Pasted image 20240916110628.png]]


### Casos em que não será função:
1. Não será função quando temos um elemento do dominio conectado com dois ou mais elementos do contradominio:
![[Pasted image 20240916105752.png]]

2. Se ficar um elemento do dominio sem se conectar com algum elemento do contradominio:
![[Pasted image 20240916111450.png]]

---


## Tipos de Funções
Existem três tipos principais:
- injetora
- sobrejetora
- bijetora

### Injetora
![[TipoFuncaoInjetora.webp]]

### Sobrejetora
![[TipoFuncaoSobrejetora.webp]]

### Bijetora
![[TipoFuncaoBijetora.webp]]

### Exemplos

**Exemplo:**
$A = \{ 1, 2, 3, 4 \}$
$B = \{ 5, , 6 \}$
$R = \{ (1, 5), (2,6), (3, 5), (4, 6) \}$

> Como nesta função (relação) temos elementos repetidos de $B$ se conectando em $A$ temos que não é bijetora, mas é sobrejetora já que não existem elementos isolados em $B$


**Exemplo:**
$Dom = \{ 1,  2, 3 \}$
$ContraDom =   \{  2, 3, 4  \}$
$f(x) = x + 1$

$f(1) = 1 + 1 = 2$
$f(2) = 2 + 1 = 3$
$f(2) = 3+ 1 = 4$

$Img = \{  2, 3, 4\}$

> 💡 Lembre-se: podemos chamar $f(x)$ de $y$, já que $y$ é a nossa imagem e é ela que é calculada no $f(x)$
> Vamos usar o exemplo acima:
> $f(x) = y$
> $y = x + 1$
> $y = 1 + 1 = 2$
> $y = 2 + 1 = 3$
> $y = 3 + 1 = 4$
> $Img = \{ 2, 3, 4 \}$

---

## Encontrando os elementos:

### Encontrando Domínio
Encontrar o domínio é encontrar os valores de $A$.

Nos exemplos vamos encontrar os valores dos domínios de funções reais (que pertence ao conjunto dos números reais $\mathbb{R}$)

Existe um algoritmo com alguns passos para fazer isso e eles são:
1. Verificar as restrições
2. Aplicar as restrições 
3. Fazer o domínio

> 💡 Para buscar o dominio é melhor sempre buscar as restrições

#### Exemplos:

1 - $$f(x) = x + 3$$
**Solução**:
1. Para resolver pensemos, ela possui restrição?
	- Não possui, já que independente do valor que eu coloque em $x$, vai existir um $x \in  \mathbb{R}$
1. Como não temos restrições, não aplicamos nada
2. Agora podemos definir o dominio: $Dom =  \mathbb{R}$

2 - $$f(x) = \frac{x + 3}{x - 2}$$
**Solução**:
1. Ao analisar a parte de cima, vemos que não há restrição, afinal independente do valor de $x$ , vai existir um $x \in  \mathbb{R}$. Mas na parte de baixo temos uma restrição já que não podemos dividir por $0$, logo, encontramos a nossa restrição
2. Para definir a restrição faremos:
$$
f(x) = \frac{x + 3}{x - 2} 
$$
Devemos ter a restrição deste jeito para o denominador (parte de baixo):
$$
x - 2 \neq 0
$$
Trabalhando na restrição, só passarmos o $2$ para o outro lado:
$$x \neq 2$$
3.  Agora com a restrição montada devemos fazer  o domínio:
$$
Dom = \mathbb{R} - \{2\}
$$

3 - $$f(x) = \sqrt{ x - 2 }$$
**Solução**:
1. Neste caso, em raízes temos uma restrição de que não existe raiz quadrada negativa, então dentro da raiz deve ser $\geq 0$
$$
x-2 \geq 0
$$
2. Definiremos a restrição:
$$
x - 2 \geq 0 \implies x \geq 2
$$

3. Agora podemos definir o domínio:
$$
Dom = [2, +\infty[
$$
4 - 
$$
y = \frac{3x}{\sqrt{ 2x - 6 }}
$$
**Solução**:
1. Neste caso temos duas restrições:
	- Não podemos ter: $2x - 6 =  0$
	- E nem: $2x - 6 < 0$
2. Logo temos nossa definição de restrição:
$$
2x - 6 > 0
$$
$$
2x > 6
$$
$$
x > \frac{6}{2}
$$
$$
x > 3
$$
3. Definimos agora o domínio:
$$
Dom =  (3, +\infty[
$$

5 - $$ f(x) = \frac{\sqrt[2]{-x+4 }}{\sqrt[3]{ x - 1 }} $$
1. Temos algumas restrições, que são parecidas se olharmos:
	- Na parte de cima temos uma restrição de que: $-x + 4 \geq 0$
	- Na parte de baixo temos a restrição de que: $x - 1 \neq 0$
		- Isso se dá pois toda raiz de índice impar resulta em um par
2. Agora vamos desenvolver:
	$$
	x - 1 \neq 0
	$$$$x \neq 1$$
- Agora definiremos a restrição do denominador:
$$-x + 4 \geq 0 $$$$
-x \geq -4
$$$$
-x \geq -4 \times  (-1)
$$
- Quando multiplicamos por $-1$ tudo muda:
$$
x  \leq 4 
$$
3. Definiremos o domínio agora, com as duas restrições:
$$
Dom = (-\infty, 4] - \{1\} 
$$

6 - $$f(x) = \frac{3}{x² - 4}$$
1. As restrições são: $x²-4 \neq 0$
2. Definiremos a restrição:
$$x²-4 \neq 0$$
$$x² \neq 4$$
$$x \neq \sqrt{4}$$
$$x \pm 2$$
3. Logo o Domínio temos:
$$
Dom = \mathbb{R} - \pm 2
$$
