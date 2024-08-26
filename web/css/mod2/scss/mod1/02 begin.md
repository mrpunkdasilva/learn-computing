# Learn Sass


## Primeiros passos

- Para começar deve-se criar um arquivo contento os codigos sass + css

- Para buildar o projeto:
	`sass fileInput.scss:fileOutput.css`

- Para buildar o projeto em tempo real, usa-se o param:
	`sass --watch fileInput.scss:fileOutput.css`


### Um pouquinho:

- Um superpoder é o de conseguir aninhar (agrupar) estilos, conseguindo poupar mais código
```scss
p {

	span {
		background: red;	
	}

	b {
		background-color: black;
	}

}
```