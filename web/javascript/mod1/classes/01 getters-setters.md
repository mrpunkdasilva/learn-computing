# Learn JavaScript Class

## Getters and Setters
Os getters e Setters são métodos que definem grupos de métodos.

### Getters
Os getters funcionam como um método para retornar valores.
São criados assim:

**Criando:**

```js
class Square {
	constructor (_width) {
		this.width  = _width;
		this.height = _width;
	}

	// deve ter a palavra reservada 'get' antes do nome do getter
	get area () {
		return this.width * this.width;
	}
}
```

**Usando:**
```js
let square1 = new Square(23);
// ao ser instanciado o getter não é necessario os parênteses
// ¬ usa-se como um atributo
console.lo("AREA ====> ", square1.area);
```

### Setters
Os Setters se enquandram no grupo de métodos que serve para setar (modificar) valores de um atributo.

**Criando:**

```js
class Square {
	constructor (_width) {
		this.width  = _width;
		this.height = _width;
	}

	get area () {
		return this.width * this.width;
	}

	set area (area) {
		this.width  = Math.sqrt(area);
		this.height =  this.width;
	}
}
```


**Usando:**

```js

let square1 = new Square(23);
console.log(square1.width, "  X  ", square1.height);
console.lo("AREA ====> ", square1.area);

// deve ser modificado como se fosse um atributo
square1.area = 12;

console.lo("AREA ====> ", square1.area);
console.log(square1.width, "  X  ", square1.height);
```
