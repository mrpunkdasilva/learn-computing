# Learn Bulma


## Responsive Classes
O Bulma fornece controle de algumas classes para se ter responsividade, através de classes do mesmo.

Sendo elas:

- `-mobile`
- `-tablet`
- `-desktop`
- `-widescreen`
- `-fullhd`

**Exemplos de uso:**
```html
<!-- 
	Esse tamanho será aplicado em todas as telas 
-->
<div class="is-size-1">
	Hellow
</div>

<!-- 
	Com a diretiva `-mobile`, o estilo só será aplicado
	em telas mobile (de celulares)
-->
<div class="is-size-1-mobile">
	Hellow
</div>

<!-- 
	Com a diretiva `-tablet`, o estilo só será aplicado
	em telas de tablets superiores
-->
<div class="is-size-1-tablet">
	Hellow
</div>

<!-- 
	Com a diretiva `-desktop`, o estilo só será aplicado
	em telas de computadores e superiores
-->
<div class="is-size-1-desktop">
	Hellow
</div>
```

Pode-se juntar as classes responsivas para se ter uma melhor responsividade:
```html
<div class="is-size-3-mobile is-size-1-desktop is-size-2-tablet">
	Hellow
</div>
``` 