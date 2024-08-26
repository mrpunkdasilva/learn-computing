# Learn Asynchronus JavaScript

## Async / Await
Async e Await é vinheram para resolver ajudar a mehorar ainda mais o uso das Promisses.

Com o `async` a função é determinada com assincrona, ou seja, seu fluxo vai ser independente. 
Para definir quando uma ação deve esperar para ser executada, escutando até ir para a outra ação

- Deve se usar o async assim, em **functions** e **arrow functions**
```js
async function sayHello() {
	console.log("Say Hello");
}

const sayHello = async () => {
	console.log("Say Hello");
};
```

- Ao usar awaitdevemos usar antes da instrução a ter essa espera: 
```js
await time(2000);
console.log(`Serve ice cream`);
```