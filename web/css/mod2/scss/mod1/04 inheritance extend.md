# Learn Sass


## Herança Extend
Um dos superpoderes é o extend do Sass onde um elemento herda os estilos de um outro elemento já criado. 

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

- Com **extend**, deve-se usalo para gerar heranças de elementos:
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