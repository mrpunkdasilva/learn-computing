# Modulo 1 - ReactJS

## Propriedades

As propriedades são valores que podem ser acessados e passados para qualquer componente. 

São as informações ou dados necessarios para que aquele componente funcione.

### Usos

Deve se fazer duas coisas para que se possa usar props (propriedades):

- **Definir as props na criação do componente**
```jsx
<Dog name="Caramelo" age="12" />
```
~ Nesse exemplo, no componente `Dog`, foram passadas 2 props:

	+ `name`
	+ `age`

Sendo que as propssão passadas como atributos, assim como no HTML. 

Porém, como estamos usando JSX, pode-se usar também dessa forma:

```jsx
<Dog name={name} age={age} />
```

> Onde as `{}` irão dizer que dentro delas será colocado JavaScript, ou seja, usando as chaves posso colocar JS na escrita do componente


- **Definir as props no componente**

Para se usar de fato as props deve se declarar em forma de parametros as propriedades que se vai usar:

```jsx
function Dog(props) {
	return <h1>I am {props.name}, {props.age} years old<h1>;
}
```

No exemplo, o parametro props da função, é um objeto que vai servir para guardar as propriedades recebidas na instanciação do componente.

Quando acessamos `props.name`, quer dizer que:

	+ Acesse o objeto `props` e retorne o valor do atributo (ou, pode-se dizer, prop) `name`

**Pode se fazer isso também com destructing ou spread operator**

+ **Spread Operator**
```jsx
dog = { name: "Doug", age: 16 };

return <Dog {...dog} />;
```

`dog` é um objeto, e o spread operador vai "espalhar" o conteudo dele, sendo que ficaria assim:

```jsx
// os atriutos e valores usam o mesmo nome
// assim sendo mais rapido o uso
return <Dog name={name} age={age} />; 
```


+ **Destructing**
```jsx
function Dog({ name, age }) {
	return <h1>I am {name}, {age} years old<h1>;
}
```

Nesse exemplo, já não se instancia o objeto props, e sim o nome das variaveis `name` e `age`, o obj `props` foi 'desestruturado' ou 'destruido'. 

Aonde pegou os atributos de mesmo nome e criou duas variaveis vindas de `props`, de escopo local, sendo equivalente a isso:

```jsx
function Dog(props) {
	const name = props.name;
	const age = props.age;

	return <h1>I am {name}, {age} years old<h1>;
}
```

>  Com isso deixa mais performatico e verboso.
