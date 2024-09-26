# Principio Fundamental da Contagem
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

Agora vamos a outro exemplo:
Bart foi nadar de skate e possui um conjunto de pistas iniciais e outro conjunto de pistas secundarias ele quer saber quantas combinações (voltas) de varias formas poderiam ser feitas.

![[Principio Fundamental da Contagem12.png]]

Pensemos então:
- Esse conjunto de setas que saem do Bart para as pistas iniciais chamemos de $p$ 
- O conjunto das setas que saem de $p$ para as pistas secundarias chamamos de $q$

![[Principio Fundamental da Contagem1.png]]

Se contar cada possibilidade teremos:
- Linhas que saem da primeira pista $p$ => 3
- Linhas que saem da segunda pista $p$ => 3
Assim temos: seis combinações possíveis de caminhos que Bart poderia escolher.

Note que se pensar o que aconteceu foi o seguinte: $3 + 3 = 6$

Já que são dois caminhos $p$ e saem de cada um 3, logo, podemos somar cada possivel caminho.

> Podemos fazer isto seguindo o caminho contrario também já que poderiam ser 2 caminhos ligados
> $2 + 2 + 2 = 6$
>Perceba na imagem que no Bart Inverso temos 6 setas saindo dele que é o mesmo resultado de: $3 + 3$ 
>![[Principio Fundamental da Contagem4.png]]

Agora pense, qual forma técnica da matemática existe para simplificar a soma de números ou parcelas (fatores) iguais?

>Sim você acertou! É a multiplicação

Logo podemos dizer que: $p \times q = n$, em que $n$ é o próprio numero de repetições, logo o que fizemos é exatamente o que a *Álgebra Linear* pressupõe que é definir técnicas para contar elementos de um conjunto.

