# Conceitos base

<!-- TOC -->
* [Conceitos base](#conceitos-base)
  * [Classes](#classes)
    * [Vamos a um exemplo no Minecraft:](#vamos-a-um-exemplo-no-minecraft)
    * [Transformando em código:](#transformando-em-código)
  * [Objeto](#objeto)
    * [Vamos a um exemplo no Minecraft:](#vamos-a-um-exemplo-no-minecraft-1)
    * [Transformando em código:](#transformando-em-código-1)
  * [Atributos](#atributos)
    * [Vamos a um exemplo no Minecraft:](#vamos-a-um-exemplo-no-minecraft-2)
    * [Transformando em código:](#transformando-em-código-2)
  * [Métodos](#métodos)
    * [Vamos a um exemplo no Minecraft:](#vamos-a-um-exemplo-no-minecraft-3)
    * [Transformando em código:](#transformando-em-código-3)
<!-- TOC -->

---

## Classes

> Quando se usa POO, **tudo ou quase é uma classe e por tabela é um objeto.**

Com isso em mente e o conceito do que seria programação orientada a objetos, temos que pensar que para **representarmos algo** do mundo real, precisamos primeiro fazer o modelo da “coisa” ou “ser”, para isso criamos as **classes**, que por vez elas terão as suas respectivas **características** → **atributos** e suas **ações → métodos.**

### Vamos a um exemplo no Minecraft:
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

### Vamos a um exemplo no Minecraft:
![[Objeto.png]]

Como vemos no exemplo a classe Jogador **possui três instancias** → Jogador1, Jogador2, Jogador3

- Que **possuem** as **características** e **ações** **definidas na classe Jogador**.

### Transformando em código:
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

## Métodos

> **Tudo aquilo que as classes fazem.**

Os métodos são responsáveis pelas **ações de uma classe (ou seja, do objeto)**, sendo que possuímos dois tipos:
- **construtor** → **inicializa a classe**, (obrigatório) e o primeiro a ser executado assim que a classe é invocada (quando usamos o ``new)
- **métodos não construtor** → todo e qualquer outro **método** **que não é o construtor**

### Vamos a um exemplo no Minecraft:
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

[[Intro - POO I]] <- Anterior | Próximo ->  [[Pilares]]