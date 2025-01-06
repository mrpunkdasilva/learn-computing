# Learn Scss


**Table of Contents**

- [Intro](#intro)
	- [O que é?](#o-que-%C3%A9)
	- [Como funciona?](#como-funciona)
- [Install](#install)
- [Primeiros passos](#primeiros-passos)
	- [Um pouquinho:](#um-pouquinho)
- [Nesting](#nesting)
- [Herança Extend](#heran%C3%A7a-extend)
- [Variáveis e Import](#vari%C3%A1veis-e-import)
	- [Import](#import)
	- [Variaveis](#variaveis)
- [Mixin](#mixin)
- [Funções](#fun%C3%A7%C3%B5es)
	- [Algumas funções já existentes:](#algumas-fun%C3%A7%C3%B5es-j%C3%A1-existentes)
- [Minificação](#minifica%C3%A7%C3%A3o)
---

## Intro

### O que é?
**Sass** é um **pré-processador** CSS moderno que possui muito poder. Como o nome já indica pré-processadores são ferramenta do qua possui:
 - Entrada
 - Processamento
 - Saída

**Sendo assim**, um pré-processador **CSS**, irá:
- Possuir uma entrada (ou seja, um arquivo Sass)
- Processara este arquivo Sass para CSS
- Retornara um arquivo CSS, já processado : `.sass -> .css`

### Como funciona?
No Sass deixamos nosso código _mais enxuto e ganhamos mais agilidade_. Deixando nosso CSS **mais organizado**.
Ao escrever nesse pré-processador **ainda se escreve CSS**, entretanto de uma forma mais **elegante** e **reutilizável**.

Alguns dos superpoderes do dele são:
- Variaveis
- Funções
- Mixins (blocos de código reutilizaveis)

Para criar um arquivo Sass é simples devemos criar:
+ Criar um arquivo, cujo a extenção deve ser: `.scss`

> **! Deve-se ter em mente que o HTML não entendera o código Sass, para tal devemos** `buildar` **os arquivos**

---

## Install
Para instalar vá em, como material de referencia:
`https://sass-lang.com/instal`
- Se usar Node:
`npm install -g sass`
- Se usar choco:
`choco install sass`
- Se usar brew (MAC e Linux):
`brew install sass/sass/sass`

---

## Primeiros passos

- Para começar deve-se criar um arquivo contento os códigos sass + css
- Para buildar o projeto:
	`sass fileInput.scss:fileOutput.css`
- Para buildar o projeto em tempo real, usa-se o param:
	`sass --watch fileInput.scss:fileOutput.css`


### Um pouquinho:

- Um superpoder é o de conseguir aninhar (agrupar) estilos, conseguindo poupar mais código
```scss
p {

	span {
		background: red;	
	}

	b {
		background-color: black;
	}

}
```

---

## Nesting

Nesting seletor proprio do Sass que serve como o `this`, servindo para referenciar a `esse` elemento. Ou seja usando estaria dizendo que determinado estilo será colocado a _esse elemento_;
Esse seletor é indicado pelo simbolo de `&`;

**Exemplos:**

1.
```scss
p {

	&:hover {
		background: #fff;
	}

}
````

2.
```scss
.btn {
	color: yellow;
	text-decoration-color: black;

	&:hover {
		background-color: black;
		color: yellow;
	}
}
```

---

## Herança Extend
Um dos superpoderes é o `extend` do Sass onde um elemento herda os estilos de um outro elemento já criado. 

Pode se ter duas formas de se ter herança:

- Com **Nesting**:
```scss
.btn {
	width: 200px;
	background: none;
	padding: 10px 0;
	border: 0;
	border-radius: 10px;

	&.btn-laranja {
		background: orange;
	}
}
```

- Com **extend**, deve-se usá-lo para gerar heranças de elementos:
```scss
.btn {
	width: 200px;
	background: none;
	padding: 10px 0;
	border: 0;
	border-radius: 10px;
}

.btn-laranja {
	@extend .btn;
	background: orange;
}
```

---

## Variáveis e Import

### Import
Para se importar estilos de um outro arquivo usa-se a diretiva: 
**Sintaxe |>** 
`@import 'stylesheet.scss';`
- Assim o arquivo que recebeu a importação terá todos os estilos do arquivo importado

### Variaveis
Um dos superpoderes especiais do Sass são as variáveis, já que é a forma de criar e como elas são tratas quando usadas com o `import` tornam o uso delas mais reutilizaveis.
**Sintaxe |>** 
```scss
$color-orang: #fff;
$font-body: 'Roboto, cursive';
```
- As variáveis devem ter como prefixo o dólar ($)

---

## Mixin
Mixins são um dos poderes para se ter blocos de código mais reutilizáveis quando tem que fazer os mesmo estilos.

- Para funcionar devemos cria-lo:
	- **Ao usar mixins pode-se usar parâmetros e eles devem também ter o dólar como prefixo**
```scss
@mixin button-style($background, $color) {
	background: $background;
	color: $color;
}
```

- Assim que criados, para serem usados podemos inclui-los dentro de um determinado elemento passando seus devidos argumentos:
```scss
btn-laranja {	
	@extend .btn;
	@include button-style($background, $color);
}
```

> **! Isso tudo consegue gerar ainda mais produtividade, reutilização e rapidez**

---

## Funções
São blocos de código pré-prontos do do próprio Sass ou mesmo personalizado em que você mesmo cria.
> **! As funções existentes estão na documentação oficial ou mesmo na W3CSchools**

### Algumas funções já existentes:
- `darken`
  + Vai servir para deixar uma cor escura, ou seja **colocar escuridão em** alguma cor
  + Sintaxe: 
	```scss
		@mixin button-style($background, $color) {
		background: $background;
		color: $color;

		&:hover {
			background: darken($background, 5%);
		}
	}
	```

- `desaturate`
  + Vai servir para mexer na desaturação da cor, ou seja, mexer na quantidade de cinza existente na cor
  + Sintaxe: 
	```scss
	@mixin button-style($background, $color) {
		background: $background;
		color: $color;

		&:hover {
			background: desaturate($background, 5%);
		}
	}
	```

- `mix`
  + Vai servir para misturar as cores passadas, podendo misturar duas cores, a partir de cálculos feitos internamente
  + Sintaxe: 
	```scss
	@mixin button-style($background, $color) {
		background: $background;
		color: $color;

		&:hover {
			background: desaturate($background, 5%);
			color: mix($color, purple);
		}
	}
	```

- `grayscale`
  + Vai servir para dar uma escala de cinza na cor passada
  + Sintaxe: 
	```scss
	@mixin button-style($background, $color) {
		background: $background;
		color: $color;

		&:hover {
			background: desaturate($background, 5%);
			color: mix($color, purple);
			text-decoration-style: dotted;
			text-decoration-color: grayscale($background);
		}
	}
	```

---

## Minificação
Minificação é uma técnica para **diminiuir drasticamente as linhas de código** o que vai gerar
mais **performance** e **escalabilidade**.

Para tal, rode o comando:

```sh
sass  .\assets\scss\styles.scss:.\assets\css\styles.css --style compressed
```

