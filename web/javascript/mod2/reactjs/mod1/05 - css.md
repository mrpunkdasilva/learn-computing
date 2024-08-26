# Modulo 1 - ReactJS

<!-- TOC -->
* [Modulo 1 - ReactJS](#modulo-1---reactjs)
  * [Inserindo CSS](#inserindo-css)
<!-- TOC -->

## Inserindo CSS

Para colocar CSS nas paginas use:

**! sempre deve ter as extenções dearquivos CSS !**

```js
import './styles/global.css';
```	

### Organização 

Organização dos arquivos CSS no projeto:

```markdown
src
 |
 |__ styles
 |	 |
 |	 |__ global.css
 |
 |__ pages
      |
      |__ Home
           |__ index.jsx (todo conteudo da pagina)
           |
           |__ style.css (estilos da pagina)
```
		
*no React não precisa definir que o `import` de Home será:*


```js
import Home from './pages/Home/index.jsx';
```

Já que por padrão ele buscara o `index` daquela pasta, ou seja, ficando assim:

```js
import Home from './pages/Home';
```