# Learn Bulma


## Grid Columns 
Construir columns layout com Bulma se torna mais simples e responsivo:

1. Adicine `columns` que será o container da coluna

2. Adicine `column` que será um elemento dentro do container

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

	💡 Convenção de nomenclatura
	Cada classe modificadora é nomeada de acordo com quantas colunas você deseja de 12. 
	Então, se você quiser 7 colunas de 12, use .is-7

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
