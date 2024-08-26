# Learn JavaScript Class

## Herança e Extends
A Herança é um dos pilares do POO que consiste e criar um classe géneria para conter as informações basicas de um dado objeto e que tenha outras classes filhas que herdem, ou seja, receba essas informações. Podendo, sobreescrever ou criar novas "informações" para essas classes filhas.

**Exemplo**:
```js
// -> Classe Pai Super Classe
class Person {
	constructor(_name, _age) {
		this.name = _name;
		this.age  = _age; 
	}

	describe() {
		console.log(`I am ${this.name} and I am ${this.age}`)
	}
}

// -> Para herdar a classe Person usa-se a key-word: `extends` 
class Programmer extends Person {
	constructor (_name, _age, _yearsOfExperience) {
		// -> para usar os atributos da Classe Pai é necessario usar a função `super`
		super(_name, _age);

		this.yearsOfExperience = _yearsOfExperience;
	}

	code() {
		console.log(`${this.name} is coding :P`);
	}
}
```

