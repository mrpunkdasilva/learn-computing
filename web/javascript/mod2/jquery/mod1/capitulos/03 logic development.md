# Learn JQuery


## Lógica de Desenvolvimento do JQuery

- No JQuery funciona com seletores, podemos selecionar elementos com ele, atravez de:
	+ Tag
		+ exemplo |> `$('h1')`
	+ Classe
		+ exemplo |> `$('.minhaClasse')`
	+ ID
		+ exemplo |> `$('#meuID')`

- Assim que selecionado é passado todas as funções nativas do JQuery, as ações são voltadas a eventos


### Seletores (formas de)

##### Métodos

- **Para adicionar atributos CSS no elemento usa-se: `.css()`**
	+ Sintaxe:
		```js
		//-> passando apenas um atributo:
		$('h1').css("color", "#f66");

		//-> passando mais de um atributo:
		$( 'a' ).css({ color: "#9ff", textDecoration: 'underline' });
		```
- **Para o elemento inicializar já escondido: `.hide()`**
	+ Sintaxe:
		```js
		$('h1').hide();
		```

- **Dar um tempo entre eventos, usa-se: `.delay()`**
	+ O tempo deverá ser informado em microsegundos;
	+ Sintaxe:
		```js
		$('h1').delay('1000');
		```
- **Fazer com que o elemento selecionado aparecerá: `.fadeIn()`**
	+ O parametro slow - definirá que ele aparecerá de forma lenta;
	+ Sintaxe:
		```js
		$('h1').fadeIn('slow');
		```

- **Para setar um text dentro de um elemento: `.text()`**
	+ O parametro slow - definirá que ele aparecerá de forma lenta;
	+ Sintaxe:
		```js
		$('h1').text('Learn JQuery in DevPunk');
		```

#### Modos de encadeamento de comandos:
- **Obs: Podemos colocar todos os métodos de modo individualmente ou seja, separados:**
	```js
	/*
	*>> Individualmente
	*/
	$( 'h1' ).css("color", "#f66");
	$( 'h1' ).hide();
	$( 'h1' ).delay('1000');
	$( 'h1' ).fadeIn('slow');
	$( 'h1' ).text('Learn JQuery in DevPunk');
	```


- **Obs: Podemos colocar todos os métodos de modo inline ou seja, na mesma linha:**
	```js
	/*
	*>> Inline
	*/
	$( 'h1' ).css("color", "#f66").hide().delay('1000').fadeIn('slow').text('Learn JQuery in DevPunk');
	```

- **Obs: Podemos colocar todos os métodos de modo inline ou seja, na mesma linha:**
	```js
	/*
	*>> Bloco
	*/
	$( 'h1' )
		.css("color", "#f66")
		.hide()
		.delay('1000')
		.fadeIn('slow')
		.text('Learn JQuery in DevPunk');
	```

### Eventos
- ***Para os eventos eles são métodos proprios JQuery, sendo que deve-se passar um callback para quando o evento for chamado*

#### Click
Para o evento de click usa-se:
```js
$(button).click(function () {
	alert("HEELO DARK HELL!!!");
});
```

**-> Hey, guys! Não podemos esquecer que pode-se usar arrow function ao inves de funções anônima ao usar callbacks, podemos usar assim:**
```js
$(button).click(() => {
	alert("HEELO DARK HELL!!!");
});
```
