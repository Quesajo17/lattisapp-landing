<script>
	import logo from '$lib/images/lattisicon.png';
</script>

<header>
	<div class="brand">
	<div class="brand-image">
		<a href="/">
			<img src={logo} class="appicon" alt="LattisIcon" />
		</a>
	</div>
		<a href="/"><p class="brand-name">Lattis</p></a>
	</div>


	<div class="links">
		<a href="https://www.blog.lattisapp.com">
			<p class="brand-name">Blog</p>
		</a>
	</div>

</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		 /* Add padding as needed */
	}

	.brand {
		display: flex;
		align-items: center;
		padding-left: 1em;
	}

	.brand-name {
		font-size: 1.5em;
		font-weight: 500;
		margin-left: 1em;
	}

	.brand-image {
		width: 2em;
		height: 2em;
		object-fit: contain;
		border-radius: 20%;
	}

	.links {
		display: flex;
		padding-right: 1em;
	}

	.appicon {
		width: 2em;
		height: 2em;
		object-fit: contain;
		border-radius: 20%;
	}



	a:hover {
		color: var(--color-text);
	}
</style>
