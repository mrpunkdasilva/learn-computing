# Learn JQuery

**Table of Contents**

- [Introdução](#introdu%C3%A7%C3%A3o)
- [Install](#install)
- [Métodos de Carregamento e Inicialização](#m%C3%A9todos-de-carregamento-e-inicializa%C3%A7%C3%A3o)
  - [Carregamento:](#carregamento)
  - [Inicialização](#inicializa%C3%A7%C3%A3o)
- [Lógica de Desenvolvimento do JQuery](#l%C3%B3gica-de-desenvolvimento-do-jquery)
  - [Seletores](#seletores)			
    - [Métodos](#m%C3%A9todos)
    - [Modos de encadeamento de comandos:](#modos-de-encadeamento-de-comandos)
	- [Eventos](#eventos)
		- [Click](#click)
- [Selectores Hierárquicos](#selectores-hier%C3%A1rquicos)
- [Eventos de Navegadores](#eventos-de-navegadores)
- [Eventos de Mouse](#eventos-de-mouse)
	- [Click](#click)
	- [Dois Clicks](#dois-clicks)
	- [Focus](#focus)
	- [Hover](#hover)
	- [Mouse Down](#mouse-down)
	- [Mouse Enter](#mouse-enter)
	- [Mouse Over / Leave](#mouse-over--leave)
	- [Mouse Move](#mouse-move)
	- [Onde conseguir mais](#onde-conseguir-mais)
- [Eventos de Teclado e Formulário](#eventos-de-teclado-e-formul%C3%A1rio)
	- [Teclado](#teclado)
	- [Fórmulario](#f%C3%B3rmulario)
	- [Onde conseguir mais](#onde-conseguir-mais)
- [Efeitos Básicos](#efeitos-b%C3%A1sicos)

---

## Introdução 

- **JQuery** é uma **biblioteca** JavaScript, criada para **facilitar a escrita de código JS** nas páginas web
- Tendo algumas vantagens e sua utilização é grande na web:
  + A biblioteca é **pequena** e **rápida**;
  + Possui uma facilidade maior na escrita de código;
  + Gera um **grande** poder para utilizar o JS
  + É **cross-browser** (multi-browsers)

---

## Install
Para instalar o **JQquery**, ou seja, usa-lo há algumas formas:
+ Pode-se apenas colocar o endereço remoto do **JQuery** usando **JSDelivr**:
  + `<script src="https://cdn.jsdelivr.net/npm/jquery@3.6.1/dist/jquery.min.js"></script>` 
+ Usando **npm** ou **yarn**:
  - `npm install jquery`
  - ` yarn add jquery`
+ Ou mesmo, a mais comum que é baixando ele:
  - Vá no site: `https://jquery.com/`
  - Click em **Download**, instale a versão **uncompressed**

> É recomendável que se coloque o arquivo dentro da pasta `js`, criada dentro de seu projeto 

---

## Métodos de Carregamento e Inicialização

### Carregamento: 

- Para verificar se o elemento está carregado usa-se o método `ready`;
- Como por exemplo algo fundamental é todo a lógica acontecer quando o documento estiver carregado,
  - ou seja, usamos o elemento `document` e verificamos se ele está lido ou carregado;
```js
[codigo de exemplo]

/*
* Assim que esse elemento do DOM for carregado será disparado o alert
*/ 
$( document ).ready(function () {
	alert('DOM CARREGADO!');
});
```

### Inicialização 

- Com o método `load` será executado o callback 
  - assim que todos os elementos forem carregados0 na página

```js
[codigo de exemplo]

/*
* Assim que todos os elementos do DOM forem carregados será disparado o alert
*/ 
$( window ).load(function () {
	alert('JANELA CARREGADA!');
});
```

---

## Lógica de Desenvolvimento do JQuery

- No JQuery funciona com seletores, podemos selecionar elementos com ele, através de:
  + **Tag:**
   + exemplo |> `$('h1')`
  + **Classe:**
   + exemplo |> `$('.minhaClasse')`
  + **ID:**
   + exemplo |> `$('#meuID')`

> Assim que selecionado é passado todas as funções nativas do JQuery, as ações são voltadas a eventos

### Seletores

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
  + O tempo deverá ser informado em microssegundos;
  + Sintaxe:
```js
$('h1').delay('1000');
```

- **Fazer com que o elemento selecionado aparecerá: `.fadeIn()`**
  + O parâmetro slow - definirá que ele aparecerá de forma lenta;
  + Sintaxe:
```js
$('h1').fadeIn('slow');
```

- **Para setar um text dentro de um elemento: `.text()`**
  + O parâmetro slow - definirá que ele aparecerá de forma lenta;
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
Para os eventos eles são métodos proprios JQuery, sendo que deve-se passar um callback para quando o evento for chamado

#### Click
- Para o evento de click usa-se:
```js
$(button).click(function () {
	alert("HEELO DARK HELL!!!");
});
```

- **Hey, guys! Não podemos esquecer que pode-se usar arrow function ao inves de funções anônima ao usar callbacks, podemos usar assim:**
```js
$(button).click(() => {
	alert("HEELO DARK HELL!!!");
});
```
---

## Selectores Hierárquicos

- Selecionando elementos filhos:
  - **exemplo |>**
```js
// -> está selecionando a tag (elemento) p dentro da elemento pai que contém a classe content
$('.content p')
```

- Selecionando filhos diretos do elemento:
  - **exemplo |>**
```js
$('.div1 > span').css({ color: 'red' });
```

- Selecionando todos os elemento após o selecionado
  - **exemplo |>**
```js
$('.p1 ~ p').css({ fontWeight: '400' });
```

---

## Eventos de Navegadores

- **Evento de erro na imagem**
  - _Sintaxe_:
```js
$('img').error(function () {
	let imagem = $(this).attr('src');
	alert(``);

	$('img').attr('src', 'img/error.png');
});
```

- **Evento de resize 
  - Irá redimensionar a imagem referente a largura e espessura da janela quando o evento resize da janela for acionado
  - _Sintaxe_:
```js
	let widthWindow  = $(window).width();
	let heightWindow = $(window).height();

	$('img')
		.width(widthWindow)
		.height(heightWindow);

	$(window).resize(function () {
		$('img')
			.width(widthWindow)
			.height(heightWindow);
	});
```

<hr>

- **Evento de scroll**
```js
// -> Rotina simples	
$('body').css("height", "7000px");
$(window).scroll(function () {
	$('img').fadeOut('1000');
});	

// -> Rotina setando a imagem conforme o valor do scrollTop pelo evento de scroll
$(window).scroll(function () {
	let top = $(window).scrollTop();
	console.log(top);

	if (top > 400) {
		$('img').fadeOut('1000');
	} else {
		$('img').fadeIn('1000');
	}
});
```

---

## Eventos de Mouse

### Click
```js
$('.ev1').click(function () {
	$(this).css("background", "#ccc");
	ex.text("Você clicou!");
});
```

### Dois Clicks
```js
$('.ev2').dbClick(function () {
	$(this).css("background", "#ccc");
	ex.text("Você clicou duas vezes");
});
```

### Focus
```js
$('.ev3')
	.focusin(function () {
		$(this).css("background", "#ccc");
		ex.text("Você deu o focus");
	})
	.focusout(function () {
		$(this).css("background", "#000");
		ex.text("Você tirou o focus");
	});
```

### Hover
```js
$('.ev4').hover(function () {
		$(this).css("background", "#ccc");
		ex.text("Passou o mouse");
	});
```

### Mouse Down
```js
$('.ev5')
	.mousedown(function () {
		$(this).css("background", "#ccc");s
		ex.text("Você apertou o botão do mouse");	
	}).mouseup(function () {
		$(this).css("background", "#000");
		ex.text("Você soltou o botão do mouse");
	});
```

### Mouse Enter
```js
let qtdeEntradasMouse = 0;
$('.ev6')
	.mouseenter(function () {
		qtdeEntradasMouse++;
		ex.text(`$Entradas do Mouse: ${qtdeEntradasMouse}`);
	})
	.mouseout(function () {
		ex.text("Saída do Mouse");
	});
```

### Mouse Over / Leave
```js
let qtdeEntradasMouseEv7 = 0;
$('.ev7')
	.mouseover(function () {
		qtdeEntradasMouseEv7++;
		ex.text(`Mouse Over: ${qtdeEntradasMouseEv7}`);
	})
	.mouseleave(function () {
		ex.text("Mouse Leave");
	});
```

### Mouse Move
```js
$('.ev8').mousemove(function (move) {
	let localX = move.pageX();
	let localY = move.pageY();

	ex.text(`Movimento X: ${localX}px | Movimento Y: ${localY}px` );
});
```

### Onde conseguir mais 
Para saber mais vá em: [https://api.jquery.com/category/events/mouse-events/](https://api.jquery.com/category/events/mouse-events/)

---


## Eventos de Teclado e Formulário

### Teclado 
**Exemplos:**

- **Primeiro exemplo:**
	```js
	$('.key').keypress(function () {
		let text = $(this).val();
		ex.text(text);
	});
	```

- **Segundo exemplo:**
	```js
	$('.key').keydown(function () {
		let text = $(this).val();
		ex.text(text);
	});
	```

- **Terceiro exemplo:**
	```js
	$('.key').keyup(function () {
		let text = $(this).val();
		ex.text(text);
	});
	```

- **Fazendo um placeholder com JQuery:**
	```html
	[index.html]
	<form action="">
		<label>
			<input type="text"  class="place" title="Digite seu nome" />
		</label>
		<label>
			<input type="text"  class="place" title="Digite seu nome" />
		</label>
		<label>
			<input type="text"  class="place" title="Digite seu nome" />
		</label>

		<label>
			<textarea rows="10" class="place key" title="Digite seu nome" />
			</textarea>
		</label>

		<label>
			<button>Botão</button>
			<button>Enviar</button>
		</label>
	</form>
	```

	```js
	[script.js]
	$('.place').each(function () {

		let input = $(this);
		let place = $(this).attr("title");

		input
			.val(place)
			.css("color", "#ccc")
			.focusin(function () {
				input.css("color", "#000");

				if (input.val() == place) {
					input.val('');
				}
			})
			.focusout(function () {
				if (input.val() == '') {
					input.css("color", "#ccc");
					input.val(place);
				}
			});

	});
	```

### Fórmulario
**Exemplos: **

- **Primeiro exemplo:**
	```js
	let ex = $('.ex1');

	$('.ev1')
		.focus(function () {
			ex.text($(this).attr('title'));
		})
		.keyup(function () {
			if ($(this).val() == 'pontocom') {
				$('.ev2').focus();
			}
		});
	```

- **Segundo exemplo:**
	```js
	// será executado callback assim que houver mudança, ou seja, 
	// ¬ assim que mudar o conteudo do input, ele vai chamar a função passada
	$('.ev1').change(function () {
		ex.text(`Campo Alterado: ${$(this).val()}`)
	});
	```

- **Terceiro exemplo:**
	```js
	$('.ev2').blur(function () {
		ex.text(`Saída do campo: ${$(this).attr('name')}`)
	});
	```

- **Quarto exemplo:**
	```js
	$('.selecionar').click(function () {
		// -> irá selecionar o texto do input
		$('.ev3').select();

		$('form').submit(function () {
			// -> fará com que o submit não sejá enviado
			return false;
		});
	});
	```

### Onde conseguir mais 
Para saber mais vá em: 
- Eventos de Teclado: [https://api.jquery.com/category/events/keyboard-events/](https://api.jquery.com/category/events/keyboard-events/)
- Eventos de Form: [https://api.jquery.com/category/events/form-events/](https://api.jquery.com/category/events/form-events/)

---

## Efeitos Básicos

Podemos também usar efeitos e animações básicas e usuais providas diretamente pelo JQuery, para saber mais vá em:
- [https://api.jquery.com/category/effects/](https://api.jquery.com/category/effects/)
