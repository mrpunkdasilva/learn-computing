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
Algumas letrinhas do alfabeto de função, afinal, precisamos primeiro entender  algumas letras para depois aprender uma aprender a falar uma palavra.

### Simbologia da função:
- Usamo um `f` minusculo e uma variavel entre parenteses (normalmente se usa `x`)
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

## Encontrando os elementos:

### Encontrando Dominio
Encontrar o dominio é encontrar os valores de A.

Nos exemplos vamos encontrar os valores dos dominios de funções reais (que pertence ao conjunto dos números reais $\mathbb{R}$)

Existe um algoritmo com alguns passos para fazer isso e eles são:
1. Verificar as restrições
2. Aplicar as restrições 
3. Fazer o dominio

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
1. Neste caso, em raizes temos uma restrição de que não existe raiz quadrada negativa, então dentro da raiz deve ser $\geq 0$
$$
x-2 \geq 0
$$
2. Definiremos a restrição:
$$
x - 2 \geq 0 \implies x \geq 2
$$

3. Agora podemos definir o dominio:
$$
Dom = [2, +\infty[
$$
4 - $$