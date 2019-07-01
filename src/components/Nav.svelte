<script>
	export let segment;
</script>

<style>
	nav {
		display: flex;
		flex-direction: column;
		border-bottom: 1px solid var(--main-fg-color);
		padding-bottom: 0.5em;
	}

	.theme-container {
		display: flex;
		flex-direction: row;

		margin: 0;
		padding: 0;
	}

	.selected {
		text-decoration: underline dotted;
	}

	a { 
		margin-right: 10px;
		margin-bottom: 0.25em;
		padding-bottom: 0;
		text-decoration: none;
	}

	a:hover {
		text-decoration: line-through dotted var(--main-fg-color);
		transition: 0.1s;
	}

	a:active { 
		border: none;
	}

	button, p {
		font-family: 'SF Mono';
		color: var(--main-fg-color);
		background-color: var(--main-bg-color);

		padding: 0;
		margin: 0;

		border: none;
	}
</style>

<nav>
	<a class='{segment === undefined ? "selected" : ""}' href='.'>home</a>
	<a class='{segment === "about" ? "selected" : ""}' href='about'>about</a>
		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
	<a rel=prefetch class='{segment === "blog" ? "selected" : ""}' href='blog'>blog</a>
	<!-- for the night/dark theme toggle
	<div class="theme-container">
		<button class="theme-button" id="night-theme-button">night</button>
		<p>/</p>
		<button class="theme-button" id="day-theme-button">day</button>
	</div>
	-->
</nav>
