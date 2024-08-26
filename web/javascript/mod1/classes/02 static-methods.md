# Learn JavaScript Class

## Static Methods
Com esse tipo de método não é necessario criar instancias para se ter acesso aos métodos.

Para usar basta usar a key-word `static` antes do nome do métodos:

```js
	static isValidDimension(width, height) {
		return width === height;
	}
```

Para implementar, instancia a classe chamando o método

```js
console.log(Square.isValidDimension(7, 6));
```