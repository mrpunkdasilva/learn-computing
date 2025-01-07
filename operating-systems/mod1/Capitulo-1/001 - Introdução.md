# Introdução 

Um **Sistema Operacional** é uma interface que interliga o **hardware** e o **software**, fazendo o gerenciamento dos dois mundos do computador.

> A inexistência, de um **SO** resulta em um impedimento de uma interação natural com o computador.

Como todo grande projeto complexo caímos em uma operação em que deve ser bem definida em como o **SO** irá trabalhar, quais são seus requisitos.

E o **SO** tem algumas funções básicas que é:
- dar partida no sistema
- gerenciar memoria 
- gerenciar dispositivos E/S

--- 
## O que os Sistemas Operacionais fazem
Um **sistema computadorizado** ou só computador, pode ser *dividido em quatro partes*:
- [[Hardware]]
- Sistema Operacional
- [[Software]]
- [[Usuários]]


- **Também podemos considerar que um sistema computadorizado é composto por:**

```
										
[0101] |                             | [  ] -> Finge que é um PC
[010]  |--: Dados        Hardware :--| |==| 
[01]   |       |             |       | ----
			   -- Software----
					 |
					 |
				|--------|
				|  WIN95 |
				|--------|     
```



- **Exemplo de Funcionamento de um Sistema Operacional**

```
+---------+   +---------+   +---------+   +---------+
| usuário |   | usuário |   | usuário |   | usuário |
|    1    |   |    2    |   |    3    |   |    n    |
+---------+   +---------+   +---------+   +---------+
     |             |             |             |
     |             |             |             |
   +------------+ +----------+ *----------+  *----------+
   | compilador | | montador | | editor de | | sistema |
   |            | |          | | textos   | | de banco|
   |            | |          | |          | | de dados|
   +------------+ +----------+ +----------+ +--------+
                        |
                        |
                    +----------+
                    | programas|
                    | de sistema|
                    | e aplicat-|
                    | ivos     |
                    +----------+
                        |
                        |
                    +----------+
                    | sistema   |
                    | operacional|
                    +----------+
                        |
                        |
                    +----------+
                    | hardware do|
                    | computador |
                    +----------+
```

```mermaid
graph TD

subgraph Usuarios

U1[Usuário 1] --> Compilador

U2[Usuário 2] --> Montador

U3[Usuário 3] --> EditorTextos

Un[Usuário n] --> BancoDados

end

  

subgraph Ferramentas

Compilador[Compilador]

Montador[Montador]

EditorTextos[Editor de Textos]

BancoDados[Sistema de Banco de Dados]

end

  

Compilador --> Programas

Montador --> Programas

EditorTextos --> Programas

BancoDados --> Programas

  

Programas[Programas de Sistema e Aplicativos] --> SO[Sistema Operacional]

SO --> Hardware[Hardware do Computador]
```
---

[[002 - Operação do computador]]