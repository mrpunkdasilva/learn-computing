# Álgebra Relacional

## Que diabo é isso?
A **Álgebra Relacional** é a linguagem formal de consultas é o SQL que veio antes do SQL. Já que essa algebra foi usada como base de inspiração para a criação do que conhecemos hoje como Strutured Query Language (SQL).

> 💡 A **Álgebra Relacional** é um calculo sobre **conjuntos** e **relações**

## Preludio 
Ok, entendemos o que seria essa tal algebra, mas para falar essa lingua precisamos agora entender seu ABC (abecedário):

- **Tupla** => é a linha da tabela
![[Álgebra Relacional - Tupla.png]]

> 💡 Lembrando que quando se trada de bancos de dados relacionais tudo se resume e termina em tabelas 

- **Atributo** => é o cabeçalho da tabela
![[Álgebra Relacional - Atributo.png]]

- **Relação** => é a tabela
![[Álgebra Relacional - RELAÇÃO.png]]

- **Domínio** => é o tipo do dado que vai descrever os valores que cada atributo pode ter
![[Álgebra Relacional - DOMINIO.png]]

> 📌 Todo e qualquer atributo possui um **domínio**
> Por exemplo, se olharmos para o atributo *ID* ele só aceita números, claro que poderia ter sido mais "claros" e dizer que só aceitam **inteiros**

## E no que isso afeta o Vasco?
No Vasco nada, mas para o entendimento da como funcionam a manipulação de bancos de dados e até para o desempenho de consultas, já que se entendermos os conceitos de Álgebra Relacional podemos extrair e promover um melhor desempenho em consultas nas bases de dados.

>👽 Essa última parte desempenho é muito:
>![[FoiOqueElaDisse.png]]

---

## Operações

### Seleção $\sigma$
> **$\sigma$ => está letra grega se chama *sigma***
> 👽 ![[sigma-squirdwind.png]]
> Está operação seleciona apenas as tuplas que satisfaçam a condição

Essa operação é que nem redpill e sigma, só seleciona quem entra nas condições impostas:
> 👽 ![[redpill1.png]]

#### Definição de livro
Com o texto acima você já entendeu a função principal do Operador de Seleção (o sigma) então vamos tentar fazer uma definição mais de livro:

É uma operação que consiste em receber um conjunto de entrada e produzir um subconjunto de forma que a estrutura é idêntica ao conjunto de entrada, porém, ele retorna apenas os elementos que satisfaçam a condição.

>💡 Estrutura idêntica quer dizer que os atributos não mudam 
> Só o que vai mudar com o uso da seleção é a tupla, que é vai mudar a partir da condição imposta 

#### Notação

$$
\sigma_{predicado}(relação)
$$
- **predicado** => condição
- **relação**   => tabela

#### Uso
Agora que já temos noção de sua notação, vamos ao uso: 
- Vamos tomar um exemplo em que queremos selecionar na tabela (relação) Personagens a tupla que possui ID igual a 1

![[Álgebra Relacional - Seleção - Uso.png]]
> 📌 Note que é como informei a cima: a estrutura da relação (tabela) não  

##### Operadores
Para fazermos uso completo dessa operação temos alguns operadores:
**Operadores de Comparação:** 
- $=$ 
![[Álgebra Relacional - Operador Igual.png]]
- $>$
![[Álgebra Relacional - Operador Maior.png]]
- $<$ 
![[Álgebra Relacional Operador Menor.png]]
- $\geq$ 
![[Álgebra Relacional - Maior Igual.png]]
- $\leq$
![[Álgebra Relacional - Operador Menor Igual.png]]

**Operadores de Lógicos:**
- $\wedge$ -> e
![[Álgebra Relacional - Operador E.png]]

- $\vee$ -> ou
![[Álgebra Relacional - Operador Ou.png]]

- $\neg$ -> negação
![[Álgebra Relacional - Operador Negação.png]]

##### Propriedade
O operador de seleção é comutativo, ou seja, não importa a ordem das operações tudo gera no mesmo.

![[Álgebra Relacional - OPerador Seleção Comutatividade.png]]

**Exemplo:**
![[Álgebra Relacional - EX2.png]]

---

### Projeção $\pi$

> $\pi$ letra grega pi que representa a *projeção*

A projeção funciona de forma que você passa um conjunto de atributos e a partir desses atributos filtrara as colunas do conjunto de entrada.

> Como opera sobre somente um único conjunto de entrada

#### Notação

$$\pi_{atributo}\text{(Relação)}$$

**Exemplo 1:** Queremos fazer uma projeção do nome na tabela Personagens
![[Álgebra Relacional - Projeção EX1.png]]

**Exemplo 2:** Descobrir o `NOME` e o `ID` de todos os personagens do sexo "Valar da Universal" e "Elfo do Rodo"
- Com isso temos que fazer uma projeção de uma seleção, ou seja:
	- Vamos primeiro selecionar a partir das condições do `sexo` e
	- Projetar os campos `nome` e `id` da relação que vem a partir da seleção

A operação ficaria assim:

$$
	\pi_{nome, id}(\sigma_{sexo = \text{'Elfo do Rodo' } \wedge \text{ } sexo = \text{'Valar da Universal'}})(Personagens)
$$
![[Álgebra Relacional - Projetção - Ex2-1.png]]

O fluxo de resolução é o seguinte:
1. Seleciona 
![[Álgebra Relacional - Operação Projetção - Ex2 - 2.png]]

2. Projeta
![[Álgebra Relacional - Projetção - EX 2 3.png]]

> O operador de projeção **não** é comutativo.

### Produto Cartesiano

É quando fazemos todas as possíveis combinações entre os elementos das relações, ou seja, para um elemento de $A$ fazemos uma combinação com todos os elementos de $B$ e assim por diante até todas as possíveis combinações.

Podemos definir dois dados: 
- Total de colunas do Produto Cartesiano: se dá pela soma número de colunas da primeira tabela + numero de colunas da segunda tabela
- Total de linhas do Produto Cartesiano: numero de linhas da primeira tabela x numero de linha da segunda tabela

> De modo geral, são só dados que existem, mas não tem muita utilidade prática

#### Notação
A notação do produto cartesiano se dá na mesma forma que em Conjuntos:
$$
\text{A} \times \text{B}
$$
#### Uso

Temos as tabelas Alunos e Cursos e queremos fazer o produto cartesiano dessas duas relações.

> Alunos:
![[Álgebra Relacional - PC- ALUNO.png]]

> Cursos:
![[Álgebra Relacional - PC - Cursos.png]]

> $$ \text{Alunos} \times \text{Cursos} $$
![[Álgebra Relacional - PC - RESULTANTE.png]]

Com isso, vemos que uma linha de **Alunos** se relaciona com cada linha de **Cursos**.


### União $\cup$


