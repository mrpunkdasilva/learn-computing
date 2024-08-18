# Programação Orientada a Objetos

## Começando pelo começo

Para começar, primeiro precisamos entender o conceito de POO, ou, Programação Orientada a Objetos. Ela é **uma técnica de programação** – ou seja, **uma forma de pensar em criar algoritmos**.

A forma base de se pensar em POO é **abstrair**_,_ e **criar classes** para **servirem de modelo** para a criação **dos objetos** que **serão usados nos programas** – percebera que POO tenta se voltar mais a realidade já que tenta pegar **objetos do mundo real e transformá-los em** **código**.

Ela segue alguns **Pilares** e **conceitos** **base**, que veremos a frente. De todo modo, POO é uma das formas que são mais utilizadas em toda a computação sendo uma das formas de resolver problemas computacionais mais bem aceitos e vistos na computação.

---

## Conceitos base

### Classes

> Quando se usa POO, **tudo ou quase é uma classe e por tabela é um objeto.**

Com isso em mente e o conceito do que seria programação orientada a objetos, temos que pensar que para **representarmos algo** do mundo real, precisamos primeiro fazer o modelo da “coisa” ou “ser”, para isso criamos as **classes**, que por vez elas terão as suas respectivas **características** → **atributos** e suas **ações → métodos.**

#### Vamos a um exemplo no Minecraft:
![[Classes.png]]

 **Tudo** **no Minecraft** **é um objeto,** ou seja, o seu personagem, os mobs, os blocos, o mundo

Então eles foram **feitos a partir de classes que por sua vez são modelos desses objeto**s → **o que terão** e **como irão se comportar**

Dessa forma podemos, **não só reutilizar código,** como **modularizar em classes o que o programa vai fazer** de modo que vai gerar mais facilidade na hora de criar e manter o sistema.

### Transformando em código:
Para criar uma classe, usamos a palavra reservada _class_ :
![[ClassesCodigo.png]]

As classes por padrão começam sempre com as primeiras letras em maiúscula → uso do **PascalCase**. Elas possuem:
- **atributos** → o que aquele modelo terá
- **métodos** → deve sempre começar com o método construtor que vai iniciar a classe

## Objeto

> Um Objeto é a instancia de um classe.

Pense que o **objeto é o uso do modelo** e ele que usamos para interagir com o sistema, contendo todos os **atributos** e **métodos da classe**.

#### Vamos a um exemplo no Minecraft:
![[Objeto.png]]

Como vemos no exemplo a classe Jogador **possui três instancias** → Jogador1, Jogador2, Jogador3

- Que **possuem** as **características** e **ações** **definidas na classe Jogador**.

#### Transformando em código:
![[ObjetoCodigo.png]]
- Para criar objetos precisamos instanciar as classes e para isso usamos a palavra-chave:
```
new NomeDaClasse()
```

- Devemos usar parênteses para a chamada do **método construtor**.

> Lembrando que, não podemos adicionar ou remover atributos ou métodos pelo objeto, somente a classe faz isso


## Atributos

> Os atributos são as **características** da classe.

Podemos pensar que os atributos são essenciais já que é o que as classes vão usar e definira o que os objetos terão.

### Vamos a um exemplo no Minecraft:
![[Atributos.png]]

A o observarmos vemos que os **atributos são a base para uma classe** já que são eles que serão usados na hora que for fazer alguma ação ou então ser usada para até mesmo outro objeto.

### Transformando em código:
![[AtributosCodigo.png]]
- Podemos definir um atributo desse modo:
```
modificador tipo nomeDoAtributo
```

E para usá-los usamos a palavra reservada → `this` servindo para referenciar que vamos usar os atributos e métodos “dessa” ou “essa” classe;
![[AtributosCodigo2.png]]
![[Atributos3.png]]

### Métodos

> **Tudo aquilo que as classes fazem.**

Os métodos são responsáveis pelas **ações de uma classe (ou seja, do objeto)**, sendo que possuímos dois tipos:
- **construtor** → **inicializa a classe**, (obrigatório) e o primeiro a ser executado assim que a classe é invocada (quando usamos o ``new)
- **métodos não construtor** → todo e qualquer outro **método** **que não é o construtor**

#### Vamos a um exemplo no Minecraft:
No exemplo vemos que um objeto Jogador ele precisa de algumas ações básicas como:

- andar | correr | comer | nadar

E existe uma etapa antes de você jogar que é criar o jogador **isto é** chamar o método construtor para que inicialize o objeto com algumas informações como nome, skin, etc.

### Transformando em código:
- Para criar o método construtor:
```
modificador NomeDaClasse(tipo parametro) {}
```
 ![[MétodosConstructor.png]]

- Para criar métodos não construtores:
```
modificador nomeDoMetodo() {}
```
  ![[MétodosComum.png]]
  
- Agora vamos usá-los:
![[MétodosUsando.png]]


---

## Pilares
De forma que ela se baseia em alguns pilares:

### Abstração

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

### Encapsulamento 

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


#### Modificadores
- **Modificadores:** _**public**_
![[ModificadorPublic.png]]

- **Modificadores:** _**private**_
![[ModificadorPrivate.png]]

- **Modificadores:** _**protected**_
![[ModificadorProtected.png]]

###  **Herança**

> _copia, mas não faz igual_

Nesse pilar pense assim: há uma **classe pai**, aquela que vai ser usada para ser a **base** das **classes filhas**, ou seja, você vai **copiar uma classe -** na verdade o que será copiado são os **métodos** e **atributos -** e **colar em outra classe**.   
- De forma que ao exemplificar pensando ainda no Minecraft, ficaria aassim:
![[Herança.png]]
	- Temos uma classe (modelo) → servindo para conter as características e ações básicas de Jogador e Mob
        
- Sendo que tanto **Jogador e Mob** **terão o que a classe pai tem**, mas **serão vistos como outras classes**, ou seja, **é uma copia** do que o modelo tem, **mas não é igual**, as filhas podem sobrescrever o que uma ação faz para ficar personalizada, só que isso é [Poliformismo](#Poliformismo)

#### Transformando **em** **código:**
 ![[HerançaCodigo1.png]]
![[HerançaCodigo2.png]]

### **Poliformismo** 
> _eu sou o Douglas, você não é o Douglas_

Com esse pilar devemos se basear na Herança, já que o poliformismo é ter **um mesmo metodo**, o que o objeto faz, que possui o **mesmo nome da classe pai e** **ma** **filha**, só que com **uma forma diferente de fazer as coisas.**

#### Voltando ao nosso Minecraft:
Como temos, **Jogador e Mob** que **possuem formas diferentes de fazer a mesma coisa**, ou seja,

- Os dois atacam, correm, etc, porém o Mob tem certos tipos de ataque diferente do Jogador
![[Poliformismo.png]]


Logo para fazer isso além de usar a [Herança](#Herança) temos que **sobrescrever** o que jaz **escrito em Personagem,** para **cada classe filha** que tenha que possuir **uma ação** que tem o **mesmo nome**, mas **varia em comportamento**.

#### Transformando em código:
  ![[PoliformismoCodigo1.png]]
- Mas não mudamos, por exemplo, seu retorno ou então os parâmetros que são aceitos
- Sendo que poderia ser feito isso, com o Poliformismo temos os **mesmo nomes de métodos só que com formas diferentes de usá-los**
![[PoliformismoCodigo2.png]]