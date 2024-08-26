# Learn Sass


## Nesting

Nesting seletor proprio do Sass que serve como o `this`, servindo para referenciar a `esse` elemento. Ou seja usando estaria dizendo que determinado estilo será colcado a _esse elemento_;
Esse seletor é indicado pelo simbolo de `&`;

**Exemplos |>**

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
