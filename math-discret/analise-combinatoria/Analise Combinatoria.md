# Analise Combinatória

A analise combinatória se baseia em desenvolver métodos para contar elementos de um conjuntos, tais elementos que são formados por alguma regra.

---

## Principio Fundamental da Contagem
A contagem se baseia em entender o significado das operações.

Este principio também é chamado de principio multiplicativo, já que usamos a multiplicação, vamos pensar:

Temos o Homer comendo parado, chega o Ned e pergunta quantos filhos o Homer, tem e ele não lembra, tipico dele não?

![[PrincipioFundamentaldaContagem1.png]]

Então o Homer começa a contar:
- Um Lizza
- Dois Bart
- Três Magie

![[Principio Fundamental da Contagem2.png]]

Parece tosco, não?

Mas se atente ao que acabou de acontecer, o Homer usou a Contagem para saber o que queria e é exatamente para isto que o Principio Multiplicativo existe, para contarmos.

**Agora vamos a outro exemplo:**
Bart foi nadar de skate e possui um conjunto de pistas iniciais e outro conjunto de pistas secundarias ele quer saber quantas combinações de varias formas poderiam ser feitas.

![[Principio Fundamental da Contagem12.png]]

**Pensemos então:**
- Esse conjunto de setas que saem do Bart para as pistas iniciais chamemos de $p$ 
- O conjunto das setas que saem de $p$ para as pistas secundarias chamamos de $q$

![[Principio Fundamental da Contagem1.png]]

**Se contar cada possibilidade teremos:**
- Linhas que saem da primeira pista $q$ => 3
- Linhas que saem da segunda pista $q$ => 3
Assim temos: seis combinações possíveis de caminhos que Bart poderia escolher.

Note que se pensar o que aconteceu foi o seguinte: $3 + 3 = 6$

Já que são dois caminhos $p$ e saem de cada um 3, logo, podemos somar cada possível caminho.

> Podemos fazer isto seguindo o caminho contrario também já que poderiam ser 2 caminhos ligados:
> 
> $2 + 2 + 2 = 6$
> 
>Perceba na imagem que no Bart Inverso temos 6 setas saindo dele que é o mesmo resultado de: $3 + 3$ 
>![[Principio Fundamental da Contagem4.png]]

Agora pense, qual forma técnica da matemática existe para simplificar a soma de números ou parcelas (fatores) iguais?

>Sim você acertou! É a multiplicação

Logo podemos dizer que: $p \times q = n$, em que $n$ é o próprio numero de repetições, logo o que fizemos é exatamente o que a *Álgebra Linear* pressupõe que é definir técnicas para contar elementos de um conjunto.

### Exemplo
A mulher de Fernando, Sara, descobriu que o marido estava a traindo, ela então foi investigar, subiu a skin de Sherlock Holmes, ou seja, investigou para saber onde ele ia todo domingo a tarde. 
Para isso ela o seguiu e o viu entrar na casa de Elen, sua melhor amiga, ela então esperou por volta de vinte minutos do lado de fora escondida do outro lado da rua, ela então depois desse tempo entrou na casa e viu que os dois estão cometendo felação. 
De antemão ao ver isso Sara correu em direção de Fernando e ela estava com uma faca, logo, ao ver isso Fernando saiu pela janela e viu que tinha alguns meios para fugir da mulher, abaixo temos o que ele viu:
![[Analise Combinatoria - Ex1.png]]

Assim ele quer saber de quantas maneiras ele consegue fugir sem, para isso pensemos:
- Ele possui 3 caminhos de A para B
- Ele tem 5 caminhos de B para C
Logo temos duas formas de resolver isso:
1. Contando tudo:
	- Tomando o primeiro caminho: 5 possibilidades
	- Tomando o segundo caminho: 5 possibilidades
	- Tomando o terceiro caminho: 5 possibilidades
	- Assim, temos que somar todas as possibilidades, que resultam em: $$5 + 5 + 5 = 15$$
2. Uso do principio multiplicativo: 
	- Definimos o $p$ como 3 (os caminhos iniciais) 
	- Definir $q$ como 5 (os outros caminhos possíveis)
	- Agora multiplicamos o $p$ e $q$
Com um desses dois métodos **temos a quantidade total de possibilidades**. 

## Tipos de Agrupamentos
Existem alguns tipos de agrupamentos, são técnicas de contagem que possuem determinado método para resolver um problema de agrupamento especifico.

### Arranjo
É quando selecionamos parte dos elementos de um conjunto.
Ou seja, um arranjo se dá em:
- Tenho um determinado conjunto de elementos, a quantidade de elementos chamados de $n$
- Quero separá-los em grupos, a quantidade de elementos do agrupamento chamamos de $p$ 
Além disso tomamos que $n>p$, ou seja, a quantidade de elementos totais é maior que a quantidade de elementos de cada grupo.

> 💡 Sendo que esses agrupamentos são ordenados, no **arranjo** a **ordem importa**

#### Formula

$$
A_{n,p} = \frac{n!}{(n - p)!}
$$
> Lê-se: arranjo de $n$ elementos tomando de $p$ em $p$

#### Exemplo
##### Exemplo 1:
![[Analise Combinatoria  - ex1 - arranjo.png]]
**Solução:**
Devemos primeiro analisar as informações:
![[Analise Combinatoria ex1 - arranjo2.png]]
1. O que queremos agrupar?
	- O que está em laranja --> 10 atletas
2. A ordem importa?
	- Se olharmos para o que está em vermelho vemos fala: maneiras distintas, logo a ordem importa
3. Temos um número de agrupamentos, que seja menor que o número total de elementos?
	- Sim temos, o problema defini que o formato do pódio são 3 lugares --> veja em verde
Com essa analise do enunciado podemos ver que precisaremos usar exatamente o arranjo.
Para isso tememos a formula do arranjo:

$$
A_{n,p} = \frac{n!}{(n - p)!}
$$
- Nosso $n$ é igual a 10 atletas
- Nosso $p$ é igual a 3 lugares do pódio
Temos então:
$$
A_{10,3} = \frac{10!}{(10 - 3)!}
$$

> Lê-mos então: arranjo de 10 elementos tomados de 3 em 3

Resolvendo:
$$A_{10,3} = \frac{10!}{(10 - 3)!}$$
$$ A_{10,3} = \frac{10 \times 9 \times 8 \times 7!}{7!} $$
- Fazemos a subtração de $10 - 3$
- Simplificamos os fatoriais iguais ($7!$)
$$ A_{10,3} = 10 \times 9 \times 8 = 720$$
**Resposta:** Agora temos a quantidade de maneiras distintas dos 100 atletas formarem o pódio de 3 lugares.

##### Exemplo 2:
