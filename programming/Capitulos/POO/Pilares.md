# Pilares
De forma que ela se baseia em alguns pilares:

<!-- TOC -->
* [Pilares](#pilares)
  * [Abstração](#abstração)
      * [Ao Transformar em código serial algo assim:](#ao-transformar-em-código-serial-algo-assim)
  * [Encapsulamento](#encapsulamento-)
    * [Modificadores](#modificadores)
  * [**Herança**](#herança)
    * [Transformando **em** **código:**](#transformando-em-código)
  * [**Poliformismo**](#poliformismo-)
    * [Voltando ao nosso Minecraft:](#voltando-ao-nosso-minecraft)
    * [Transformando em código:](#transformando-em-código-1)
<!-- TOC -->

---


## Abstração

> _Jogar os detalhes para debaixo do tapete_

![[AbstraçãoCodigo.png]]
- Deixar **apenas o essencial** que o objeto precisa.
- Por exemplo, vamos abstrair um jogador do Minecraft, ou seja, **pensar** nas **características** e **ações** mais **importantes**:    
­![[Abstração.png]]

#### Ao Transformar em código serial algo assim:
![[AbstraçãoCodigo.png]]
- Por convenção, usamos o nome da classe no singular e usando o pascal case
- No caso, vamos **abstrair a questão da linguagem**, já que o importante são os conceitos
- Assim criamos uma classe – modelo, que possui **apenas o que é importante** para um jogador

## Encapsulamento 

> _cada um no seu quadrado_

- Deixar as características do objeto (**atributo****s**) e o que ele faz (**métodos**) **acessível** apenas **a ele mesmo** e **seu acesso é controlado**
- Usaremos o exemplo abaixo para representar encapsulamento
![[Encapsulamento.png]]

Caso **não exista este pilar**, ou seja, os atributos não estão encapsulados – no seu “quadrado” ou melhor no seu objeto, logo, **qualquer um pode acessar diretamente**:

- **Transformando em código:**
![[EncapsulamentoCodigo.png]]
- Assim podemos observar que não possuir um encapsulamento correto pode ocorrer em falhas no sistema

- **Logo**, **para** resolver isso devemos **encapsular** o que a classe Jogador possui para que somente seja acessado seus **atributos** e **métodos,** dentro da própria classe:
    - Quando criarmos outros objetos tanto da classe Jogador ou mesmo tentar acessar algum atributo do Jogador, não será possível.
    
    - Isso graças aos **modificadores de acesso** que são palavras-chaves, escritas nos atributos e métodos para definir **como eles serão encapsulados**, logo, encapsulamos usando modificadores.
        
- Antes estava _**public**_ , agora está _**private**_ , os **modificadores mudaram** e o encapsulamento também e agora **não é possível acessar** os atributos dentro dos objetos da classe Jogador **diretamente**:
![[Encapsulamento1.png]]

> Obs.: As outras partes do código não são importantes no momento para aparecerem
![[Encapsulamento2.png]]


### Modificadores
- **Modificadores:** _**public**_
![[ModificadorPublic.png]]

- **Modificadores:** _**private**_
![[ModificadorPrivate.png]]

- **Modificadores:** _**protected**_
![[ModificadorProtected.png]]

##  **Herança**

> _copia, mas não faz igual_

Nesse pilar pense assim: há uma **classe pai**, aquela que vai ser usada para ser a **base** das **classes filhas**, ou seja, você vai **copiar uma classe -** na verdade o que será copiado são os **métodos** e **atributos -** e **colar em outra classe**.   
- De forma que ao exemplificar pensando ainda no Minecraft, ficaria aassim:
![[Herança.png]]
	- Temos uma classe (modelo) → servindo para conter as características e ações básicas de Jogador e Mob
        
- Sendo que tanto **Jogador e Mob** **terão o que a classe pai tem**, mas **serão vistos como outras classes**, ou seja, **é uma copia** do que o modelo tem, **mas não é igual**, as filhas podem sobrescrever o que uma ação faz para ficar personalizada, só que isso é [Poliformismo](#Poliformismo)

### Transformando **em** **código:**
![[HerançaCodigo1.png]]
![[HerançaCodigo2.png]]

## **Poliformismo** 
> _eu sou o Douglas, você não é o Douglas_

Com esse pilar devemos se basear na Herança, já que o poliformismo é ter **um mesmo metodo**, o que o objeto faz, que possui o **mesmo nome da classe pai e** **ma** **filha**, só que com **uma forma diferente de fazer as coisas.**

### Voltando ao nosso Minecraft:
Como temos, **Jogador e Mob** que **possuem formas diferentes de fazer a mesma coisa**, ou seja,

- Os dois atacam, correm, etc, porém o Mob tem certos tipos de ataque diferente do Jogador
![[Poliformismo.png]]


Logo para fazer isso além de usar a [Herança](#Herança) temos que **sobrescrever** o que jaz **escrito em Personagem,** para **cada classe filha** que tenha que possuir **uma ação** que tem o **mesmo nome**, mas **varia em comportamento**.

### Transformando em código:
  ![[PoliformismoCodigo1.png]]
- Mas não mudamos, por exemplo, seu retorno ou então os parâmetros que são aceitos
- Sendo que poderia ser feito isso, com o Poliformismo temos os **mesmo nomes de métodos só que com formas diferentes de usá-los**
![[PoliformismoCodigo2.png]]

---

[[Conceitos base]] <- Anterior | Próximo ->  