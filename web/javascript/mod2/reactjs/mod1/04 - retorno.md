# Modulo 1 - ReactJS

<!-- TOC -->
* [Modulo 1 - ReactJS](#modulo-1---reactjs)
  * [Retorno](#retorno)
<!-- TOC -->


## Retorno

A regra do JSX é de que deve se retornar apenas um elemento, ou seja não se pode ter isso aqui:

```jsx
function App() {

	// retornando dois elementos
	return ( 
		<h1>Hello World!!</h1>
		<h1>Hello World!!</h1>
	);

}
```

Devendo apenas retornar um unico elemento:

```jsx
function App() {

	// retornando um elemento
	return ( 
		<h1>Hello World!!</h1>
	);

}
```

Outras formas:

1. Encapsulando em outro Elemento

```jsx
function App() {

	// retornando um elemento
	return ( 
		<div>
			<h1>Hello World!!</h1>
		</div>
	);

}
```

2. React Fragment - serve para encapsular elementos, mas não sendo nenhuma elemento. Funcionando só para indicar que existe um 'element wrraped'. Assim retornando apenas um elemento.

```jsx
function App() {

	
	return ( 
		<>
			<h1>Hello World!!</h1>
		</>
	);

}
```