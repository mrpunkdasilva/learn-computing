# Portas Lógicas
Os computadores são constituidos de elemento eletrônicos como: **capacitores**, **resistores** e **transistores**.

- **Capacitores:** são os componentes reponsaveis por armazenar e liberar carga eletrica, sendo que realiza a filtragem de ruída e stabilizar tensões;

 - **Resistores:** limita a passagem de corrente elétrica, usado para controlar a voltagem da corrente eletrica;

- **Transistores:** amplificam sinais e controlam o fluxo da corrente dentro do circuito, eles cuidam de permitir ou não a passagm de binários para realizarem operações atravéz das portas lógicas, e tudo isso formam os `circuitos lógicos`

Portas Lógicas são a base para a contrução de um processador, elas são embutidas em um CI (Circuito Integrado) com o objetivo de realizar tarefas espeficas. Sendo econtradas tanto em ULSI (Ultra Larga Escala Integrada) atá a circuitos mais simples.


## Álgebra de Chaveamento
Assim como a aĺgebra básica da escola se criou a necessidade de fazer operações com os digitos binarios. Então urge a **Álgebra de Chaveamento**.

Para tal era necessario primeiro definir-se as representações gráficas e então se deu 0 (falso), 1 (verdadeiro).

### Porta AND  
Está porta aceita dois operandos: A e B, sendo binarios 0 e 1. 
A operação AND simula a multiplicaçãoo  binaria, possuindo a finalidade de garantir que o mesmo bit de entrada seja o mesmo da saída (transferencia de bit, ou seja, é usado para transferir dados da memoria para a CPU).

Porta Lógica AND 
|Entrada|  Saída  |
|-------|---------|
| A | B |  Y = AB |
|---|---|---------|
| 1 | 0 |    0    |
| 0 | 1 |    0    |
| 1 | 1 |    1    |
| 0 | 0 |    0    |


### Porta OR  
Está porta aceita dois operandos: A e B, sendo binarios 0 e 1.
Ela simula a soma binaria, ou seja, só reultara em verdadeiro (1) se um dos operandos forem 1

Porta Lógica OR  
|Entrada|  Saída  |
|-------|---------|
| A | B | Y = A+B |
|---|---|---------|
| 1 | 0 |    1    |
| 0 | 1 |    1    |
| 1 | 1 |    1    |
| 0 | 0 |    0    |


### Porta XOR  (exclusive or)
Está porta aceita dois operandos: A e B, sendo binarios 0 e 1.
Ele serve como uma verificação de igualdade, em que se os operando tiverem os seus valores binarios iguais, ou seja, se A e B forem iguais a 1 ou 0. então a operação irá reultar em 0 (falso).
Logo, se seus valores são diferentes a operação resultara em verdadeiro (1).

Porta Lógica XOR 
|Entrada|  Saída  |
|-------|---------|
| A | B |Y = A XOR B |
|---|---|---------|
| 1 | 1 |    0    |
| 0 | 1 |    1    |
| 1 | 0 |    1    |
| 0 | 0 |    0    |


### Porta NOT  
Está porta aceita um operando: A, sendo binario 0 ou 1.
Ela faz uma inversão de valores, ou seja, s o valor do operando for 1 ele se torna 0 de mesmo modo que seja o vlor 0 ele o inverte para 1.

Porta Lógica NOT 
|Entrada|  Saída  |
|-------|---------|
| A     |  NOT A  |
|-------|---------|
|    1  |    0    |
|    0  |    1    |

### Porta Derivadas
> A execução dessas portas se dá por uma de cada vez, ou seja, irá executar primeiro uma e depois a outra.

### Porta NAND  
Está porta aceita dois operandos: A e B, sendo binarios 0 e 1.
Ela faz a operação AND e em seguida faz a execução do NOT

Porta Lógica NAND 
|Entrada|  Saída  |
|-------|---------|
| A | B | Y = A NAND B |
|---|---|---------|
| 1 | 0 |    1    |
| 0 | 1 |    1    |
| 1 | 1 |    0    |
| 0 | 0 |    1    |


### Porta NOR  
Está porta aceita dois operandos: A e B, sendo binarios 0 e 1.
Ele faz primiero o OR e em seguida opra o NOT.

Porta Lógica NOR  
|Entrada|  Saída  |
|-------|---------|
| A | B | Y = A+B |
|---|---|---------|
| 1 | 0 |    1    |
| 0 | 1 |    1    |
| 1 | 1 |    1    |
| 0 | 0 |    0    |




