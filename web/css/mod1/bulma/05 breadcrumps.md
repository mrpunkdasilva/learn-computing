# Learn Bulma


## Breadcrumps
Breadcumps (migalhas de pão), links de páginas, funcionam para direcinar o usuario da página em que ele está. Desse jeito: `ORM / Sequelize / Start`

**Exemplo**:

```html
<!-- breadcumps -->
<section class="section pt-4 pb-0">
	<nav class="breadcrumb" aria-label="breadcrumbs">
	  <ul>
	    <li>
	    	<a href="#">
	    		Dev Punk
	    	</a>
	    </li>
	    <li>
	    	<a href="#">
	    		Shop
	    	</a>
	    </li>
	    <li class="is-active">
	    	<a href="#" aria-current="page">
	    		Breadcrumb
	    	</a>
	    </li>
	  </ul>
	</nav>
</section>
```

<br>

### Alinhamento
As opções de alinhamento são: `is-centered` e `is-right`

- **Exemplo** `centered`: 

```html
<nav class="breadcrumb is-centered" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

- **Exemplo** `right`:

```html
<nav class="breadcrumb is-right" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

<br>

### Icons 
Pode-se ter icones também no breadcump

**Exemplo**:

```html
<nav class="breadcrumb" aria-label="breadcrumbs">
  <ul>
    <li>
      <a href="#">
        <span class="icon is-small">
          <i class="fas fa-home" aria-hidden="true"></i>
        </span>
        <span>Bulma</span>
      </a>
    </li>
    <li>
      <a href="#">
        <span class="icon is-small">
          <i class="fas fa-book" aria-hidden="true"></i>
        </span>
        <span>Documentation</span>
      </a>
    </li>
    <li>
      <a href="#">
        <span class="icon is-small">
          <i class="fas fa-puzzle-piece" aria-hidden="true"></i>
        </span>
        <span>Components</span>
      </a>
    </li>
    <li class="is-active">
      <a href="#">
        <span class="icon is-small">
          <i class="fas fa-thumbs-up" aria-hidden="true"></i>
        </span>
        <span>Breadcrumb</span>
      </a>
    </li>
  </ul>
</nav>
```

### Alternatives Separators
Existem 4 adicionais separatores, sendo eles: `has-arrow-separator`, `has-bullet-separator`, `has-dot-separator` e `has-succeeds-seprator`

- **Exemplo**:

```html
<nav class="breadcrumb has-arrow-separator" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

- **Exemplo**:

```html
<nav class="breadcrumb has-bullet-separator" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

- **Exemplo**:

```html
<nav class="breadcrumb has-bullet-separator" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

- **Exemplo**:

```html
<nav class="breadcrumb has-dot-separator" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

- **Exemplo**:

```html
<nav class="breadcrumb has-succeeds-separator" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

### Sizes
Os tamanhos nativos do Bulma são: `is-small`, `is-medium` e `is-large`

- **Exemplo**:

```html
<nav class="breadcrumb is-small" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

- **Exemplo**:

```html
<nav class="breadcrumb is-medium" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```

- **Exemplo**:

```html
<nav class="breadcrumb is-large" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Bulma</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Components</a></li>
    <li class="is-active"><a href="#" aria-current="page">Breadcrumb</a></li>
  </ul>
</nav>
```
