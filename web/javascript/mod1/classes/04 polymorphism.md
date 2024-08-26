# Learn JavaScript Class

## Polimorfismo

É um dos pilares que serve para fazer uma junção e mistura de classes. Exemplo, tem uma classe "Animal" que é a classe pai da class "Dog", as duas tem um método que chamado: `makeSound`, ele faz um som. Ao criarmos a classe Dog e herdar a classe Animal, herdamos por tabela o método `makeSound`, mas um cachorro faz "Woof Woof" ou "Au Au Au" só que na super classe retorna "Generic Sound". 
Para resolver isso, usamos o "Polimorfismo" justamente para adaptar as classes filhas a abstração do problema.

Exemplo:

```js
class Animal {
	constructor(_name, _age, _type) {
		this.name = _name;
		this.age  = _age;
	}

	makeSound() {
		console.log("Generic Sound ~_~");
	}
}

class Dog extends {
	constructor(_name, _age, _type) {
		super(_name, _age, _type);
		this.type = _type;
	}

	makeSound() {
		console.log("Au Au Au");
	}
}

const doguinho = new Dog("Caramelo", 12, "Viralata");

doguinho.makeSound();
```