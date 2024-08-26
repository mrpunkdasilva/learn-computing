# Learn Sass


## Variáveis e Import

### Import
Para se importar estilos de um outro arquivo usa-se a diretiva: 
**Sintaxe |>** 
`@import 'stylesheet.scss';`
- Assim o arquivo que recebeu a importação terá todos os estilos do arquivo importado

### Variaveis
Um dos superpoderes especiais do Sass são as variaveis, já que é a forma de criar e como elas são tratas quando usadas com o `import` tornam o uso delas mais reutilizaveis.
**Sintaxe |>** 
```scss
$color-orang: #fff;
$font-body: 'Roboto, cursive';
```
- As variaveis devem ter como prefixo o dolar ($)
