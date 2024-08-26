# Learn Sass


## Mixin
Mixins são um dos poderes para se ter blocos de codigo mais reutilizaveis quando tem que fazer os mesmo estilos.

- Para funcionar devemos cria-lo:
	- **Ao usar mixins pode-se usar parametros e eles devem também ter o dólar como prefixo**
```scss
@mixin button-style($background, $color) {
	background: $background;
	color: $color;
}
```

- Assim que criados, para serem usados podemos inclui-los dentro de um determinado elemento passando seus devidos argumentos:
```scss
btn-laranja {	
	@extend .btn;
	@include button-style($background, $color);
}
```

**! Isso tudo consegue gerar ainda mais produtividade, reutilização e rapidez**
