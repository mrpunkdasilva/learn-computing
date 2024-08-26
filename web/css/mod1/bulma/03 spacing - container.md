# Learn Bulma


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
<br>

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

<br>
<hr>
<br>

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

