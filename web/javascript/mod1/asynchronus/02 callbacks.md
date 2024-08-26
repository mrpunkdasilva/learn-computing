# Learn Asynchronus JavaScript

## Callback
Callbacks são de modo simples uma função dentro de outra função. Ou seja, pense assim teremos uma primeira função que irá ter uma relação com uma segunda função que será chamada dentro da primeira.

Exemplo:

```js
// Callback
// Use o `call_nomeFunction`
const steps = (call_stepOne, call_stepTwo) => {
	console.log("~ This is steps);

	console.log("|> Call step one...");
	console.log(call_stepOne());

	console.log("|> Call step two...");
	console.log(call_stepTwo());
};

const stepOne() {
	console.log("STEP ONE");
};
const stepTwo() {
	console.log("STEP TWO")
};


steps(stepOne, stepTwo);
```

## Callback Hell (Inferno de Retorno de Chamada)
Deve se tomar cuidado para não chegar no nível de um Callback Hell, já que isso é uma má pratica. Por varios motivos: codigo fica mais complexo e dificil de se fazer uma manutenção ou mesmo entender ele.

```js
let production = () => {
	setTimeout(() => {
		console.log("Order received, starting production...");

		setTimeout(() => {
			console.log("The fruit has been chopped");

			setTimeout(() => {
				console.log(`${stocks.Liquid[0]} and ${sotcks.Liquids[1]} was added`);

				setTimeout(() => {
					console.log("The machine was started");

					setTimeout(() => {
						console.log(`ice dream was placed on ${stocks.Holders[0]}`);

						setTimeout(() => {
							console.log(`${stocks.Toppings[0]} was added as toppings`);

							setTimeout(() => {
								console.log("Serve ice scream");
							}, 2000);

						}, 3000);

					}, 2000);

				}, 1000);

			}, 1000);

		}, 2000);

	}, 0000);
};
```