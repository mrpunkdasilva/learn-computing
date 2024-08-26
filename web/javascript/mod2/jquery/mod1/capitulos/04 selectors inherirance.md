# Learn JQuery


## Selectores Hierárquicos

- Selecionando elememtos filhos:

**exemplo |>**

```js
// -> está selecionando a tag (elemento) p dentro da elemento pai que contém a classe content
$('.content p')
```

<hr>

- Selecionando filhos diretos do elemento:

**exemplo |>**


```js
$('.div1 > span').css({ color: 'red' });
```

- Selecionando o primeiro elemento após o selecionado

**exemplo |>**

<hr>

- Selecionando todos os elemento após o selecionado

**exemplo |>**

```js
$('.p1 ~ p').css({ fontWeight: '400' });
```
