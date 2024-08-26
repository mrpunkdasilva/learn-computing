# Learn JavaScript Class

## Basic
Classes são moldes, para objetos que nelas terão: metodos e atributos. Elas não são usadas diretamente na logica da aplicação, mas sim é usado o seu objeto.

`Class -> Obect`

Propriedades de Instancia: o que ele tem
- nome
- idade
- altura

Metodos de Instancia: o que ela  faz
- correr
- falar
- nadar


### Criar uma classe:**
```js
class name {
	// code...
}	
```

### Diretiva this
A diretiva `this` é usado no escopo das classes para refenciar a propria classe. Sendo o mesmo que dizer: 'esse'

### Constructor:**

É o metodo que é executado assim que o objeto é criado, ou seja, uma unica vez.

Exemplo:

```js
class Rectangle {
	constructor() {
		console.log("The Rectangle is being created");
	}
}	

let myRectancle1 = new Rectangle();
```

Assim que criado aparecera no console do navegador: `"The Rectangle is being created"`

#### Usando argumentos passados pelo `constructor`:

```js
class Rectangle {
	constructor(_width, _height, _color) {
		console.log("The Rectangle is being created");

		this.width  = _width; 
		this.height = _height;
		this.color  = _color;
	}
}	

let myRectancle1 = new Rectangle(12, 3, "chocolate");
```

Ao fazer isso os atributos de instancia: `width`, `height`, `color`. Terão o valor passados pelo `constructor`


### Criando métodos génericos:
Para criar um método basta apenas fazer isso:
```js
class Rectangle {
	constructor(_width, _height, _color) {
		console.log("The Rectangle is being created");

		this.width  = _width; 
		this.height = _height;
		this.color  = _color;
	}
	
	// metodo para calcular área do retangulo
	getArea() {
		return this.width * this.height;
	}
}	
```