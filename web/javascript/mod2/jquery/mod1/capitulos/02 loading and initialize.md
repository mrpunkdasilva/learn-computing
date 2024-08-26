# Learn JQuery


## Métodos de Carregamento e Inicialização

### Carregamento: 

- Para verificar se o elemento está carregado usa-se o método `ready`;
- Como por exemplo algo fundamental é todo a lógica acontecer quando o documento estiver carregado,
- ¬ ou seja, usamos o elemento `document` e verificamos se ele está lido ou carregado;

```js
[codigo de exemplo]

/*
* Assim que esse elemento do DOM for carregado será disparado o alert
*/ 
$( document ).ready(function () {
	alert('DOM CARREGADO!');
});
```
<br>

### Inicialização 

- Com o método `load` será executado o callback 
- ¬ assim que todos os elementos forem carregados na página

```js
[codigo de exemplo]

/*
* Assim que todos os elementos do DOM forem carregados será disparado o alert
*/ 
$( window ).load(function () {
	alert('JANELA CARREGADA!');
});
```
