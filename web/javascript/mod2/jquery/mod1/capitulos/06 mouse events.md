# Learn JQuery


## Eventos de Mouse

### Click
```js
$('.ev1').click(function () {
	$(this).css("background", "#ccc");
	ex.text("Você clicou!");
});
```

### Dois Clicks
```js
$('.ev2').dbClick(function () {
	$(this).css("background", "#ccc");
	ex.text("Você clicou duas vezes");
});
```

### Focus
```js
$('.ev3')
	.focusin(function () {
		$(this).css("background", "#ccc");
		ex.text("Você deu o focus");
	})
	.focusout(function () {
		$(this).css("background", "#000");
		ex.text("Você tirou o focus");
	});
```

### Hover
```js
$('.ev4').hover(function () {
		$(this).css("background", "#ccc");
		ex.text("Passou o mouse");
	});
```

### Mouse Down
```js
$('.ev5')
	.mousedown(function () {
		$(this).css("background", "#ccc");s
		ex.text("Você apertou o botão do mouse");	
	}).mouseup(function () {
		$(this).css("background", "#000");
		ex.text("Você soltou o botão do mouse");
	});
```

### Mouse Enter
```js
let qtdeEntradasMouse = 0;
$('.ev6')
	.mouseenter(function () {
		qtdeEntradasMouse++;
		ex.text(`$Entradas do Mouse: ${qtdeEntradasMouse}`);
	})
	.mouseout(function () {
		ex.text("Saída do Mouse");
	});
```

### Mouse Over / Leave
```js
let qtdeEntradasMouseEv7 = 0;
$('.ev7')
	.mouseover(function () {
		qtdeEntradasMouseEv7++;
		ex.text(`Mouse Over: ${qtdeEntradasMouseEv7}`);
	})
	.mouseleave(function () {
		ex.text("Mouse Leave");
	});
```

### Mouse Move
```js
$('.ev8').mousemove(function (move) {
	let localX = move.pageX();
	let localY = move.pageY();

	ex.text(`Movimento X: ${localX}px | Movimento Y: ${localY}px` );
});
```