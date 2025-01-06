# Learn Bulma


**Table of Contents**

- [Intro](#intro)
- [Coisas necessarias antes de instalar:](#coisas-necessarias-antes-de-instalar)
- [Start - Instalação](#start---instala%C3%A7%C3%A3o)
	- [CSS + Bulma](#css--bulma)
	- [Scss + Bulma#](#scss--bulma)
- [Fonts e Colors](#fonts-e-colors)
	- [Fonts](#fonts)
		- [Size (Tamanho)](#size-tamanho)
		- [Cases (Tipo de caixa)](#cases-tipo-de-caixa)
		- [Style (Estilo)](#style-estilo)
	- [Weight (Peso)](#weight-peso)
	- [Align (Alinhamento)](#align-alinhamento)
	- [Classes compostas para fontes](#classes-compostas-para-fontes)
- [Colors](#colors)
	- [Cores de fundo](#cores-de-fundo)
- [Spacing & Containers](#spacing--containers)
	- [Spacing](#spacing)
		- [Padding](#padding)
			- [Directions](#directions)
		- [Margin](#margin)
			- [Directions](#directions)
	- [Containers](#containers)
		- [Section](#section)
		- [Container](#container)
- [Navbar (Desktop e Mobile)](#navbar-desktop-e-mobile)
- [Breadcrumps](#breadcrumps)
	- [Alinhamento](#alinhamento)
	- [Icons](#icons)
	- [Alternatives Separators](#alternatives-separators)
	- [Sizes](#sizes)
- [Grid Columns](#grid-columns)
	- [Sizes](#sizes)
		- [Sistema de 12 colunas](#sistema-de-12-colunas)
- [Responsive Classes](#responsive-classes)
	- [Tabbet Content](#tabbet-content)
- [Message Boxes](#message-boxes)
- [Buttons](#buttons)
- [Cards](#cards)
- [Form Fields](#form-fields)
- [Footer](#footer)
- [Nota do autor](#nota-do-autor)


## Intro

- Bulma é um framework CSS para criar sites de modo mais **rapido**, **moderno**, **responsivo** e **open source**.

- Ele possui: 
	- [x] Flexbox e Grid Layout
	- [x] Helpers;
	- [x] Components;
	- [x] Customização;
	- [x] Responsividade

- Se concentra em trazer apenas o CSS, ou seja, as regras de estilo dos elementos que ele possui
- Por exemplo modals, terá só os estilos dele não contento JavaScript, assim torna-se mais livre
a forma que implementamos esse elemento.

---
## Coisas necessarias antes de instalar:
1. Usar DOCTYPE HTML5:
```html
<!DOCTYPE html>
``` 

2. Usar meta tag de responsividade:
```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

---

## Start - Instalação
Para usar o Bulma é bem simples. 

### CSS + Bulma
Importar o arquivo CSS do Bulma do diretorio do jsDelivr

- HTML (Link)
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css">
```

- CSS (import)
```css
@import "https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css";
```

### Scss + Bulma#
Instalar o package do Bulma com: npm ou yarn. Por `cdnjs`
- `npm i bulma`
- `yarn add bulma`

---

> 💡 A maioria das classes do Bulma começam: `is` e `has`

## Fonts e Colors
Veremos como trabalhar com fontes e cores no Bulma.

### Fonts

#### Size (Tamanho)
- Para trabalhar com fontes usamos a diretiva: `is-size-<number>`
- `<number>` é um número que varia de **1 a 7**

+ Exemplos
```html
<h1 class="is-size-1">Hello, Bulma</h1>
<h2 class="is-size-2">Hello, Bulma</h2>
<h3 class="is-size-3">Hello, Bulma</h3>
<p class="is-size-7">Hello, Bulma</p>
```

#### Cases (Tipo de caixa)
- Definir os tipos de caixa para textos.
- Deve-se usar a diretiva: `is-<case>`
- `<case>` seria o uma das caixas que podem ser usadas: **lowercase**, **uppercase** e **capitalize**;

+ Exemplos: 
```html
<h1 class="is-size-4 is-uppercase">Hello dark again</p>
<p class="is-lowercase">HellFIRE again</p>
<p class="is-capitalize">I am back to hell</p>
```

#### Style (Estilo)
- Alguns estilos podem ser usados como no exemplo:

+ Exemplo:
```html
<p class="is-size-4 is-uppercase is-italic">Hello dark again</p>
```

### Weight (Peso)
- Para tal regra usa-se: `has-font-weight-<value>` 
- `<value>` valor do peso da fonte, podendo ser por exemplo: **bold**, **light**

+ Exemplos:
```html
<p class="is-size-7 is-uppercase is-italic has-font-weight-bold">
	Hello dark again
</p>
```

### Align (Alinhamento)
- Definir alinhamento do texto: `has-text-<align>`
- `<align>` valor do alinhamento do texto, podendo ser: **left** (default, padrão), **centered**, **right** , **justify***

+ Exemplos:
```html
<h1 class="is-size-7 has-font-weight-bold has-text-centered">
	Dark Souls 2
</h1>
```

### Classes compostas para fontes
Elas são de título e subtitulo. 

+ Exemplos:
```html
<h2 class="title">Title</h2>
<h3 class="subtitle">Subtitle</h3>
<h1 class="title has-text-centered">
	Dark Souls 2
</h1>
```

> 💡 Classes compostas são regras de estilos vindas dessas outras classes que possuem um papel mais genérico na estilização de um elemento em tela, como por exemplo: um título.


## Colors
No Bulma existe cores padrões com suas respectivas classes como: cores de ações e entre outras.

Cores de ações:
São cores que por sua vez representam uma determinada ação:
```html
<p class="has-text-primary">I'm primary text</p>
<p class="has-text-warning">I'm warning text</p>
<p class="has-text-danger-light">I'm danger text</p>
<p class="has-text-info">I'm info text</p>
<p class="has-text-success">I'm success text</p>

<!-- 
Temas de cores claro ou escuro referente a cor padrão do Bulma 
-->
<p class="has-text-dark">I'm dark text</p>
<p class="has-text-light">I'm light text</p>	
```

> 💡 Para tornar as cores mais claras ou escuras como se fossem temas usa-se: 
> - Exemplos: `text-success-light` ou `text-success-dark`. 
 Ou seja basta adicionar: **light** (claro) ou **dark** (escuro)

### Cores de fundo 

As cores de fundo no Bulma funcionam assim: `has-background-<value>-<teme>`
	
- `<value>` é nome da cor correspondente ao que o Bulma possui;
- `<teme>` (opcional) sendo o tema da cor, se será: dark ou light

+ Exemplos:
```html
<p class="has-text-primary has-background-light">I'm primary text</p>
<p class="has-text-warning has-background-danger">I'm warning text</p>
<p class="has-text-light has-background-primary-dark">I'm light text</p>
```

---

## Spacing & Containers

### Spacing

#### Padding
Para mexer nesse espaçamento usa-se a diretiva: `p<direction>-<value>`

- `<direction>` direção do padding, se não informado será o `<value>` será colocado em todas as direções do elemento;
-  `<value>` valor do padding a ser inserido;

##### Directions 
- `py-<value>`
	- Mexer na direção `y` do elemento, isto é, colocar padding no top e no bottom dele

- `px-<value>`
	- Mexer na direção `x` do elemento, isto é, colocar padding no left e no right dele

- `pt-<value>`
	- Mexer na direção `top` do elemento

- `pl-<value>`
	- Mexer na direção `left` do elemento


- `pb-<value>`
	- Mexer na direção `bottom` do elemento

- `pr-<value>`
	- Mexer na direção `right` do elemento


#### Margin
Para mexer nesse espaçamento usa-se a diretiva: `m<direction>-<value>`

- `<direction>` direção da margin, se não informado será o `<value>` será colocado em todas as direções do elemento;
-  `<value>` valor do padding a ser inserido;

##### Directions 
- `my-<value>`
	- Mexer na direção `y` do elemento, isto é, colocar margin no top e no bottom dele

- `mx-<value>`
	- Mexer na direção `x` do elemento, isto é, colocar margin no left e no right dele

- `mt-<value>`
	- Mexer na direção `top` do elemento

- `ml-<value>`
	- Mexer na direção `left` do elemento


- `mb-<value>`
	- Mexer na direção `bottom` do elemento

- `mr-<value>`
	- Mexer na direção `right` do elemento


+ **Exemplos**: 
```html
<p class="p-6">
	Lorem ipsum dolor sit amet consectetur, adipisicing elit. Laborum aspernatur iste, obcaecati?
</p>
<h1 class="py-6">Hello, Bulma</h1>
<h2 class="px-4 py-2">Hello, Bulma</h2>
<h2 class="mr-4 pb-2">Hello, Bulma</h2>
```


### Containers
Para os containers o Bulma possui suas classes especificas como a seguir.

#### Section
- Usada em seções, com suas proprias regras de estilo.
+ **Exemplos**: 
```html
<section class="section">
	<p>
		Lorem ipsum dolor sit, amet consectetur adipisicing elit. Explicabo, voluptas. Illo corrupti explicabo dignissimos iste, necessitatibus vitae quasi? Sint, porro atque suscipit cupiditate.
	</p>
</section>
```

#### Container
- Uso de modo geral.
+ **Exemplos**: 
```html
<section class="section">
	<div class="container">
		<p>
			Lorem ipsum dolor sit, amet consectetur adipisicing elit. Explicabo, voluptas. Illo corrupti explicabo dignissimos iste, necessitatibus vitae quasi? Sint, porro atque suscipit cupiditate.
		</p>
	</div>
</section>
```

---


## Navbar (Desktop e Mobile)

	[index.html]

```html
<nav class="navbar has-shadow is-white">
	<!-- logo - brand  -->
	<div class="navbar-brand">
  	<a href="index.html" class="navbar-item">
  		<img 
  			src="https://via.placeholder.com/780x150.png" 
  			style="max-height: 70px;"
  			class="py-2 px-2" 
  		/>
  	</a>

  	<button class="navbar-burger" id="burger">
  		<span></span>
  		<span></span>
  		<span></span>
  	</button>
	</div>

	<!-- menu - links -->
	<div class="navbar-menu" id="nav-links">
		<div class="navbar-end">
			<a href="#" class="navbar-item">
				Minha conta
			</a>
			<a href="#" class="navbar-item">
				Cart (0)
			</a>
		</div>
	</div>
</nav>

<script src="index.js" defer></script>	
```

	[index.js]

```js
// module menu
const burgerIcon = document.querySelector("#burger");
const navbarMenu =  document.querySelector("#nav-links");

burgerIcon.addEventListener("click", () => {
	navbarMenu.classList.toggle("is-active");
});

```

---

## Breadcrumps
Breadcumps (migalhas de pão), links de páginas, funcionam para direcionar o usuário da página em que ele está. Desse jeito: `ORM / Sequelize / Start`

**Exemplo**:

```html
<!-- breadcumps -->
<section class="section pt-4 pb-0">
	<nav class="breadcrumb" aria-label="breadcrumbs">
	  <ul>
	    <li>
	    	<a href="#">
	    		Dev Punk
	    	</a>
	    </li>
	    <li>
	    	<a href="#">
	    		Shop
	    	</a>
	    </li>
	    <li class="is-active">
	    	<a href="#" aria-current="page">
	    		Breadcrumb
	    	</a>
	    </li>
	  </ul>
	</nav>
</section>
```

### Alinhamento
As opções de alinhamento são: `is-centered` e `is-right`

- **Exemplo** `centered`: 

```html
<nav class="breadcrumb is-centered" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

- **Exemplo** `right`:

```html
<nav class="breadcrumb is-right" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

### Icons 
Pode-se ter ícones também no breadcump

**Exemplo**:

```html
<nav class="breadcrumb" aria-label="breadcrumbs">
  <ul>
    <li>
      <a href="#">
        <span class="icon is-small">
          <i class="fas fa-home" aria-hidden="true"></i>
        </span>
        <span>Bulma</span>
      </a>
    </li>
    <li>
      <a href="#">
        <span class="icon is-small">
          <i class="fas fa-book" aria-hidden="true"></i>
        </span>
        <span>Documentation</span>
      </a>
    </li>
    <li>
      <a href="#">
        <span class="icon is-small">
          <i class="fas fa-puzzle-piece" aria-hidden="true"></i>
        </span>
        <span>Components</span>
      </a>
    </li>
    <li class="is-active">
      <a href="#">
        <span class="icon is-small">
          <i class="fas fa-thumbs-up" aria-hidden="true"></i>
        </span>
        <span>Breadcrumb</span>
      </a>
    </li>
  </ul>
</nav>
```

### Alternatives Separators
Existem 4 adicionais separadores, sendo eles: `has-arrow-separator`, `has-bullet-separator`, `has-dot-separator` e `has-succeeds-seprator`

- **Exemplo**:  `has-arrow-separator`

```html
<nav class="breadcrumb has-arrow-separator" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

- **Exemplo**: `has-bullet-separator`

```html
<nav class="breadcrumb has-bullet-separator" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

- **Exemplo**:  `breadcrumb has-dot-separator`

```html
<nav class="breadcrumb has-dot-separator" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

- **Exemplo**: `breadcrumb has-succeeds-separator`

```html
<nav class="breadcrumb has-succeeds-separator" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

### Sizes
Os tamanhos nativos do Bulma são: `is-small`, `is-medium` e `is-large`

- **Exemplo**: `breadcrumb is-small`

```html
<nav class="breadcrumb is-small" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

- **Exemplo**: `breadcrumb is-medium`

```html
<nav class="breadcrumb is-medium" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

- **Exemplo**: `breadcrumb is-large`

```html
<nav class="breadcrumb is-large" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```


----

## Grid Columns 
Construir columns layout com Bulma se torna mais simples e responsivo:
1. Adicione `columns` que será o container da coluna
2. Adicione `column` que será um elemento dentro do container

- **Exemplo básico:** 
```html
<div class="columns">
  <div class="column">
    First column
  </div>
  <div class="column">
    Second column
  </div>
  <div class="column">
    Third column
  </div>
  <div class="column">
    Fourth column
  </div>
</div>
```

### Sizes
A variações de tamanho nas columns, para realizar tal trabalho usa-se os sizes.

Se você quiser alterar o tamanho de uma única coluna, você pode usar uma das seguintes classes:

- `is-three-quarters`
- `is-two-thirds`
- `is-half`
- `is-one-third`
- `is-one-quarter`
- `is-full`

As outras colunas preencherão o espaço restante automaticamente.
- **Exemplo**: 
```html
<div class="columns">
  <div class="column is-four-fifths">is-four-fifths</div>
  <div class="column">Auto</div>
  <div class="column">Auto</div>
</div>

<div class="columns">
  <div class="column is-three-quarters">is-three-quarters</div>
  <div class="column">Auto</div>
  <div class="column">Auto</div>
</div>

<div class="columns">
  <div class="column is-two-thirds">is-two-thirds</div>
  <div class="column">Auto</div>
  <div class="column">Auto</div>
</div>

<div class="columns">
  <div class="column is-three-fifths">is-three-fifths</div>
  <div class="column">Auto</div>
  <div class="column">Auto</div>
</div>

<div class="columns">
  <div class="column is-half">is-half</div>
  <div class="column">Auto</div>
  <div class="column">Auto</div>
</div>

<div class="columns">
  <div class="column is-two-fifths">is-two-fifths</div>
  <div class="column">Auto</div>
  <div class="column">Auto</div>
</div>

<div class="columns">
  <div class="column is-one-third">is-one-third</div>
  <div class="column">Auto</div>
  <div class="column">Auto</div>
</div>

<div class="columns">
  <div class="column is-one-quarter">is-one-quarter</div>
  <div class="column">Auto</div>
  <div class="column">Auto</div>
</div>

<div class="columns">
  <div class="column is-one-fifth">is-one-fifth</div>
  <div class="column">Auto</div>
  <div class="column">Auto</div>
</div>
```

#### Sistema de 12 colunas

Como a grade pode ser dividida em 12 colunas, existem classes de tamanho para cada divisão:

- `is-1`
- `is-2`
- `is-3`
- `is-4`
- `is-5`
- `is-6`
- `is-7`
- `is-8`
- `is-9`
- `is-10`
- `is-11`
- `is-12`

> 💡 Convenção de nomenclatura
> - Cada classe modificadora é nomeada de acordo com quantas colunas você deseja de 12. 
> - Então, se você quiser 7 colunas de 12, use .is-7

- Exemplo:
```html
<div class="columns is-vcentered">
	<div class="column is-3">
		<h1 class="is-sie-1 title">
			Jest
		</h1>

		<h2 class="is-size-2 subtitle">
			Dark Roast
		</h2>

		<p>
			Lorem ipsum, dolor sit amet consectetur, adipisicing elit. Mollitia, veniam, obcaecati. Dicta delectus repellat vel, numquam accusantium rerum.
		</p>
	</div>

	<div class="column is-5 has-text-centered">
		<img 
			src="https://th.bing.com/th/id/OIP.gWgBZQLOP7jV3xEvoYRcaAHaF2?pid=ImgDet&rs=1" 
			alt="Coffee Jest Dark Roast" 
			class="px-6" 
		/>
	</div>

	<div class="column is-4">
		<div class="is-size-4 mb-4">
			R$ 10,45
		</div>

		<p class="mb-4">
			Lorem ipsum dolor sit amet, consectetur, adipisicing elit. Iste saepe voluptates, assumenda.
		</p>
	</div>
</div>
</div>
```

---

## Responsive Classes
O Bulma fornece controle de algumas classes para se ter responsividade, através de classes do mesmo.

Sendo elas:

- `-mobile`
- `-tablet`
- `-desktop`
- `-widescreen`
- `-fullhd`

**Exemplos de uso:**
```html
<!-- 
	Esse tamanho será aplicado em todas as telas 
-->
<div class="is-size-1">
	Hellow
</div>

<!-- 
	Com a diretiva `-mobile`, o estilo só será aplicado
	em telas mobile (de celulares)
-->
<div class="is-size-1-mobile">
	Hellow
</div>

<!-- 
	Com a diretiva `-tablet`, o estilo só será aplicado
	em telas de tablets superiores
-->
<div class="is-size-1-tablet">
	Hellow
</div>

<!-- 
	Com a diretiva `-desktop`, o estilo só será aplicado
	em telas de computadores e superiores
-->
<div class="is-size-1-desktop">
	Hellow
</div>
```

Pode-se juntar as classes responsivas para se ter uma melhor responsividade:
```html
<div class="is-size-3-mobile is-size-1-desktop is-size-2-tablet">
	Hellow
</div>
``` 


### Tabbet Content
Conteúdo em guias.

- `[index.html]`

```html
<div class="columns is-8 is-variable">
	<div class="column is-7-tablets">
		<!-- tabbed content -->
		<div class="tabs is-boxed">
			<ul>
				<li class="is-active" data-target="product-details">
					<a>Product Details</a>
  			</li>
				<li data-target="delivery-information">
					<a>Delivery Information</a>
  			</li>
			</ul>
		</div>

		<div class="px-2" id="tab-content">
			<div id="product-details">
  			<p>
  				Lorem, ipsum dolor sit amet consectetur adipisicing elit. Perferendis adipisci iusto maxime sunt doloribus illum.
  				Lorem ipsum dolor, sit, amet consectetur adipisicing elit. Incidunt aliquam excepturi officia illo fugiat sequi, voluptatibus perspiciatis at! Recusandae quod iure, error? Debitis?
  			</p>
			</div>

			<div id="delivery-information" class="is-hidden">
  			<p>
  				Lorem, ipsum dolor sit amet consectetur adipisicing elit. Perferendis adipisci iusto maxime sunt doloribus illum.
  				Lorem ipsum dolor, sit, amet consectetur adipisicing elit. Incidunt aliquam excepturi officia illo fugiat sequi, voluptatibus perspiciatis at! Recusandae quod iure, error? Debitis?
  			</p>
			</div>
		</div>
	</div>

	<div class="column is-5-tablet">
		<p>
			Lorem ipsum dolor sit amet consectetur adipisicing, elit. Nulla a ut odit beatae consectetur aut alias suscipit, officia natus inventore quod molestiae soluta? Lorem ipsum dolor sit amet consectetur, adipisicing elit.
		</p>
	</div>
</div>
</div>
```

- `[index.js]`

```js
// tabs
const tabs = document.querySelectorAll('.tabs li');
const tabContent = document.querySelectorAll('#tab-content > div');

tabs.foreach(( tab ) => {
	tab.addEventListener('click', () => {
		tabs.foreach(( item ) => item.classList.remove('is-active'));
		tab.classList.add('is-active');

		const target = tab.dataset.target;
		console.log(target);

		tabContent.foreach(( box ) => {
			if (box.getAttribute('id') === target) {
				box.classList.remove('is-hidden');
			}
			box.classList.add('is-hidden');
		});
	});
});
```

---

## Message Boxes
Caixas de mensagens.

```html
<!-- message box -->
<div class="message is-dark">
	<div class="message-header">
		<p>Earn Points with the Coffee Club </p>
	</div>

	<div class="message-body">
		<p>
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa numquam omnis autem quas sunt doloribus recusandae excepturi laboriosam doloremque itaque minus ratione, eligendi incidunt accusantium.
		</p>
	</div>	
</div>
```

---

## Buttons
Botões no Bulma.

```html
<buttton class="button is-primary">
	Add to Cart
</buttton>

<buttton class="button is-loading">
	Add to Cart
</buttton>
```

---


## Cards

```html
<!-- cards -->
<section class="section">
	<div class="container">
		<h3 class="title has-text-centered is-size-4">
			Related Products
		</h3>

		<div class="columns mt-5 is-8 is-variable is-centered">
			<div class="column is-4-tablet is-3-desktop">
				<div class="card">
					<div class="card-image has-text-centered px-6">
						<img src="assets/p1.png" alt="Product" />
					</div>

					<div class="card-content">
						<p>R1 12, 98</p>
						<p class="title is-size-5">
						  Cortardo Cup
						</p>
					</div>

					<footer class="card-footer">
						<p class="card-footer-item">
							<a href="#" class="has-text-gray">
								View		
							</a>
						</p>
					</footer>
				</div>
			</div>

			<div class="column is-4-tablet is-3-desktop">
				<div class="card">
					<div class="card-image has-text-centered px-6">
						<img src="assets/p2.png" alt="Product" />
					</div>

					<div class="card-content">
						<p>R1 12, 98</p>
						<p class="title is-size-5">
						  Clup Cluck
						</p>
					</div>

					<footer class="card-footer">
						<p class="card-footer-item">
							<a href="#" class="has-text-gray">
								View		
							</a>
						</p>
					</footer>
				</div>
			</div>

			<div class="column is-4-tablet is-3-desktop">
				<div class="card">
					<div class="card-image has-text-centered px-6">
						<img src="assets/p3.png" alt="Product" />
					</div>

					<div class="card-content">
						<p>R1 12, 98</p>
						<p class="title is-size-5">
						  Madaresco Expresso
						</p>
					</div>

					<footer class="card-footer">
						<p class="card-footer-item">
							<a href="#" class="has-text-gray">
								View
							</a>
						</p>
					</footer>
				</div>
			</div>
		</div>
	</div>
</section>
```

---

## Form Fields

```html
<form>
	<div class="field">
		<label for="" class="label">
			Name
		</label>
		<div class="control">
			<input type="text" class="input" placeholder="Name" />
		</div>
	</div>

	<div class="field">
		<label for="" class="label">
			Email
		</label>
		<div class="control">
			<input type="email" class="input" placeholder="Email" />
		</div>
	</div>

	<div class="field">
		<div class="control">
			<label for="term" class="checkbox">
				<input type="checkbox" name="term" />
					I agree to the <a href="#">terms & contidion</a>
			</label>
		</div>
	</div>

	<button class="button is-primary">
		Sig Up
	</button>
</form>
```

---

## Footer

```html
<!-- footer -->
<footer class="footer">
	<div class="content has-text-centered">
		<p>Copyright 2020 | Mr. Punk da SIlva </p>
	</div>
</footer>
```

---

## Nota do autor
Este é apenas um grande resumo das principais funcionalidades desta ferramenta, vejo que ela tem potencial e que pode ser sim útil, recomendo visitar a documentação oficial caso tenha ficado com dúvidas ou queira ver algo mais especifico.
- Documentação oficial com Masterclass: [https://cssmasterclass.io/](https://cssmasterclass.io/)
- Why Bulma CSS could be your new favorite framework: [https://devmountain.com/blog/why-bulma-css-could-be-your-new-favorite-framework/](https://devmountain.com/blog/why-bulma-css-could-be-your-new-favorite-framework/)
- Bulma Templates - é bom para pegar as coisas prontas: [https://bulmatemplates.github.io/bulma-templates/](https://bulmatemplates.github.io/bulma-templates/)
