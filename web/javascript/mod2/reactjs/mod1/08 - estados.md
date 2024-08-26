# Modulo 1 - ReactJS

<!-- TOC -->
* [Modulo 1 - ReactJS](#modulo-1---reactjs)
  * [Estados (States)](#estados-states)
    * [Imutabilidade](#imutabilidade)
    * [Key Prop](#key-prop)
<!-- TOC -->

## Estados (States)

São variaveis com poder de mudarem o estado da interface, ou seja, seu valor é refletido na aplicação.

O Hook `useState` permite ter variáveis em componentes funcionais. Você passa o estado inicial para esta função e ele retorna uma variável com o valor atual do estado (não necessariamente o estado inicial).


1. Para isso importe o Hook:

```js
import { useState } from "react";
```

2. Use-o:

```js
const [studentName, setStudentName] = useState("");
```

~ `useState("")` -> vai definir o estado inicial, retornando dois elementos:

+	o estado e a função que irá alterar o estado:
	- studentName -> estado
	- setStudentName -> alterador do estado

> ! Sempre será nessa ordem !

- `[studentName, setStudentName]` -> é a destructing do useState(), criando duas consts, pegando valores vindos do Hook.

-  O React renderiza a tela conforme cada estado muda, porém, para ser mais performatico ele renderiza apenas o objeto do DOM que foi mudado. 

-  De forma inteligente e independendeb buscando ser o mais performatico possível, atraves de seu algoritmo chamado de: Algoritmo de Reconciliação.


### Imutabilidade

Esse princípio é regido por:

		"O contéudo deve ser substituido e não modificado".

Como modificar um conteúdo se torna menos e bem menos performatico. A opção mais viavel, quando olhamos para a performance é substituir **todo** o conteúdo por um novo.


### Key Prop

Essa prop é a chave unica que serve para que componentes criados dinamicamente se tornem mais performaticos, assim que um componente não a tiver, vai ser gerado um 'Warning' que dira que esse componente deve ter a prop `key` e que deve ser unica para que o React consiga saber quem ele é de modo certeiro o que vai pesar na performance do sistema já que sendo uma key unica ele consegue manipular e ver o componente de forma mais performatica.

- Normalmente se usa um `id` para servir como valor para a `key`

