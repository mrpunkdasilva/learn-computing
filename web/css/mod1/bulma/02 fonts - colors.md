# Learn Bulma

	💡 A maioria das classes do Bulma começam: `is` e `has`

## Fonts e Colors
Veremos como trabalhar com fontes e cores no Bulma.


### Fonts

#### Size (Tamnho)
- Para trabalhar com fontes usamos a diretiva: `is-size-<number>`
- `<number>` é um número que varia de **1 a 7**

+ Exemplos
```html
<h1 class="is-size-1">Hello, Bulma</h1>
<h2 class="is-size-2">Hello, Bulma</h2>
<h3 class="is-size-3">Hello, Bulma</h3>
<p class="is-size-7">Hello, Bulma</p>
```


<br>

#### Cases (Tipo de caixa)
- Definir os tipos de caixa para textos.
- Deve-se usar a diretiva: `is-<case>`
- `<case>` seria o uma das caixas que podem ser usadas: **lowercase**, **uppercase** e **capitalize**;

+ Exemplos: 
```html
<h1 class="is-size-4 is-uppercase">Hello dark again</p>
<p class="is-lowercase">HellFIRE again</p>
<p class="is-capitalize">I am back to hell</p>
```


<br>

#### Style (Estilo)
- Alguns estilos podem ser usados como no exemplo:

+ Exemlo:
```html
<p class="is-size-4 is-uppercase is-italic">Hello dark again</p>
```


<br>

### Weight (Peso)
- Para tal regra usa-se: `has-font-weight-<value>` 
- `<value>` valor do peso da fonte, podendo ser por exemplo: bold, light

+ Exemplos:
```html
<p class="is-size-7 is-uppercase is-italic has-font-weight-bold">
	Hello dark again
</p>
```


<br>

### Align (Alinhamento)
- Definir alinhamento do texto: `has-text-<align>`
- `<align>` valor do alinhamento do texto, podendo ser: **left** (default, padrão), **centered**, **right** , **justify***

+ Exemplos:
```html
<h1 class="is-size-7 has-font-weight-bold has-text-centered">
	Dark Souls 2
</h1>
```


<br>

### Classes compostas para fontes
Elas são de título e subtitulo. 

+ Exemplos:
```html
<h2 class="title">Title</h2>
<h3 class="subtitle">Subtitle</h3>
<h1 class="title has-text-centered">
	Dark Souls 2
</h1>
```

	💡 Classes compostas são regras de estilos vindas dessas outras classes que possuem um papel mais génerico
	na estilização de um elemento em tela, como por exemplo: um título.


<br>
<hr>

## Colors
No Bulma existe cores padrões com suas respecivas classes como: cores de ações e entre outras.

### Cores de ações:
São cores que por sua vez representam uma determinada ação:
```html
<p class="has-text-primary">I'm primary text</p>
<p class="has-text-warning">I'm warning text</p>
<p class="has-text-danger-light">I'm danger text</p>
<p class="has-text-info">I'm info text</p>
<p class="has-text-success">I'm success text</p>

<!-- 
Temas de cores claro ou escuro referente a cor padrão do Bulma 
-->
<p class="has-text-dark">I'm dark text</p>
<p class="has-text-light">I'm light text</p>	
```
	
	💡 Para tornar as cores mais claras ou escuras como se fossem temas usa-se: 
	Exemplos: text-success-light ou text-success-dark. 
	Ou seja basta adicionar deve-se: light (claro) ou dark (escuro)


### Cores de fundo 
As cores de fundo no Bulma funcinam assim: `has-background-<value>-<teme>`
	
- `<value>` é nome da cor correspondende ao que o Bulma possui;
- `<teme>` (opcional) sendo o tema da cor, se será: dark ou light

+ Exemplos:
```html
<p class="has-text-primary has-background-light">I'm primary text</p>
<p class="has-text-warning has-background-danger">I'm warning text</p>
<p class="has-text-light has-background-primary-dark">I'm light text</p>
```