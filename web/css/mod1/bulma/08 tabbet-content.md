# Learn Bulma


## Tabbet Content
Conteúdo em guias.

- `[index.html]`

```html
<div class="columns is-8 is-variable">
	<div class="column is-7-tablets">
		<!-- tabbed content -->
		<div class="tabs is-boxed">
			<ul>
				<li class="is-active" data-target="product-details">
					<a>Product Details</a>
  			</li>
				<li data-target="delivery-information">
					<a>Delivery Information</a>
  			</li>
			</ul>
		</div>

		<div class="px-2" id="tab-content">
			<div id="product-details">
  			<p>
  				Lorem, ipsum dolor sit amet consectetur adipisicing elit. Perferendis adipisci iusto maxime sunt doloribus illum.
  				Lorem ipsum dolor, sit, amet consectetur adipisicing elit. Incidunt aliquam excepturi officia illo fugiat sequi, voluptatibus perspiciatis at! Recusandae quod iure, error? Debitis?
  			</p>
			</div>

			<div id="delivery-information" class="is-hidden">
  			<p>
  				Lorem, ipsum dolor sit amet consectetur adipisicing elit. Perferendis adipisci iusto maxime sunt doloribus illum.
  				Lorem ipsum dolor, sit, amet consectetur adipisicing elit. Incidunt aliquam excepturi officia illo fugiat sequi, voluptatibus perspiciatis at! Recusandae quod iure, error? Debitis?
  			</p>
			</div>
		</div>
	</div>

	<div class="column is-5-tablet">
		<p>
			Lorem ipsum dolor sit amet consectetur adipisicing, elit. Nulla a ut odit beatae consectetur aut alias suscipit, officia natus inventore quod molestiae soluta? Lorem ipsum dolor sit amet consectetur, adipisicing elit.
		</p>
	</div>
</div>
</div>
```


- `[index.js]`

```js
// tabs
const tabs = document.querySelectorAll('.tabs li');
const tabContent = document.querySelectorAll('#tab-content > div');

tabs.foreach(( tab ) => {
	tab.addEventListener('click', () => {
		tabs.foreach(( item ) => item.classList.remove('is-active'));
		tab.classList.add('is-active');

		const target = tab.dataset.target;
		console.log(target);

		tabContent.foreach(( box ) => {
			if (box.getAttribute('id') === target) {
				box.classList.remove('is-hidden');
			}
			box.classList.add('is-hidden');
		});
	});
});
```
