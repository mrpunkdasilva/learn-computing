# Modulo 1 - ReactJS

## Renderização

Ele manipula os elementos da DOM atraves do seu ferramental.

Atraves da class ReactDOM pode-se renderizar e manipular o DOM:

```jsx
ReactDOM.createRoot(
  document.getElementById('root')
).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
) 
``` 


**! não precisa colocar extençãode arquivos js, jsx, tsx, ts. React já cuida disso !**
