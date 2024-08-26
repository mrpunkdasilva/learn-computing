# Learn Sass


## Funções
São blocos de codigo pré-prontos do do proprio Sass ou mesmo personalizado em que você mesmo cria.
**! As funções existentes estão na documentação oficial ou mesmo na W3CSchools**

### Algumas funções já existentes:

- `darken`
	+ Vai servir para deixar uma cor escura, ou seja **colocar escuridão em** alguma cor
	+ Sintaxe: 
	```scss
		@mixin button-style($background, $color) {
		background: $background;
		color: $color;

		&:hover {
			background: darken($background, 5%);
		}
	}
	```

- `desaturate`
	+ Vai servir para mexer na desaturação da cor, ou seja, mexer na quantidade de cinza existente na cor
	+ Sintaxe: 
	```scss
	@mixin button-style($background, $color) {
		background: $background;
		color: $color;

		&:hover {
			background: desaturate($background, 5%);
		}
	}
	```

- `mix`
	+ Vai servir para misturar as cores passadas, podendo misturar duas cores, a partir de calculos feitos internamente
	+ Sintaxe: 
	```scss
	@mixin button-style($background, $color) {
		background: $background;
		color: $color;

		&:hover {
			background: desaturate($background, 5%);
			color: mix($color, purple);
		}
	}
	```

- `grayscale`
	+ Vai servir para dar uma escala de cinza na cor passada
	+ Sintaxe: 
	```scss
	@mixin button-style($background, $color) {
		background: $background;
		color: $color;

		&:hover {
			background: desaturate($background, 5%);
			color: mix($color, purple);
			text-decoration-style: dotted;
			text-decoration-color: grayscale($background);
		}
	}
	```
