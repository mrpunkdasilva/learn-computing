# Modulo 1 - ReactJS

<!-- TOC -->
* [Modulo 1 - ReactJS](#modulo-1---reactjs)
  * [Hooks](#hooks)
  * [useEffect](#useeffect)
    * [useEffect Assync](#useeffect-assync)
<!-- TOC -->

## Hooks
São funções feitas para ligar e conectar os recursos de estados e ciclo de vida do React a partir de componentes funcionais, isso acontece, pois, o React agora recomenda usar componentes funcionais já que conseguem ser independentes e mais faceis de usar.

-  Por convenção a primeira palavra de um Hook deve ser:
`use`
  - exemplo |> `useMyHook` - `useState`


## useEffect
O useEffect é executado automaticamente sempre que o componente é renderizado.

- A estrutura do useEffect é da seguinte forma:
```jsx
useEffect(() => {
 // Dentro do objeto devemos colocar todas. ações que serão executadas.
    

// Os arrays definem quais os estados que o useEffect depende.
  }, [dependencies]);
```

- `dependencies`:
  + -> se não for colocado nada ele executara apenas uma vez
  + -> se for passado um state, ele executara toda vez que o state for alterado

+ exemplo |>
```js
useEffect(() => {
    fetch("https://api.github.com/users/msNullus")
    .then(( response ) => response.json())
    .then(({ user, avatar_url }) => {

      setUser({
        name: user,
        avatar: avatar_url
      });

    });
  }, []);
```

### useEffect Assync
Fazendo requisições assíncronas utilizando o Hook useEffect

+ Como o useEffect não aceita ser criado de modo assíncrono, deve se usar uma função para chamar os dados de modo assincrono, e assim dentro do Hook chame a função:

```js
useEffect(() => {
    async function fetchData() {
      const response = await fetch("https://api.github.com/users/msNullus");
      const data = await response.json();
      console.log("DADOS =>", data);

      setUser({
        name: data.name,
        avatar: data.avatar_url,
      });
      
    }
    fetchData();
  }, []);
```