# Learn Bulma


## Navbar (Desktop e Mobile)

	[index.html]

```html
<nav class="navbar has-shadow is-white">
	<!-- logo - brand  -->
	<div class="navbar-brand">
  	<a href="index.html" class="navbar-item">
  		<img 
  			src="https://via.placeholder.com/780x150.png" 
  			style="max-height: 70px;"
  			class="py-2 px-2" 
  		/>
  	</a>

  	<button class="navbar-burger" id="burger">
  		<span></span>
  		<span></span>
  		<span></span>
  	</button>
	</div>

	<!-- menu - links -->
	<div class="navbar-menu" id="nav-links">
		<div class="navbar-end">
			<a href="#" class="navbar-item">
				Minha conta
			</a>
			<a href="#" class="navbar-item">
				Cart (0)
			</a>
		</div>
	</div>
</nav>

<script src="index.js" defer></script>	
```

	[index.js]

```js
// module menu
const burgerIcon = document.querySelector("#burger");
const navbarMenu =  document.querySelector("#nav-links");

burgerIcon.addEventListener("click", () => {
	navbarMenu.classList.toggle("is-active");
});

```