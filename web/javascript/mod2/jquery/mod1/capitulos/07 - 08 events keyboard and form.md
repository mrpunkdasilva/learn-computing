# Learn JQuery


## Eventos de Teclado e Fórmulario


### Teclado 
**Exemplos: **

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

- **Fazendou um placeholder com JQuery:**
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