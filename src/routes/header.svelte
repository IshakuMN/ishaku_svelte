<script>
	import logo from '$lib/images/VectormyLogo.svg';
</script>

<header>
	<img src={logo} alt="logo" />
	<nav class="nav1">
		<a href="/Projects">Projects</a>
		<a href="/Articles">Articles</a>
		<a href="/Stack">Stack</a>
		<a href="/About">About</a>
	</nav>
</header>

<style>
	.nav1 {
		display: flex;
		align-items: center;
		position: fixed;
		left: 0;
		right: 0;
		top: 16px;
		display: flex;
		justify-content: center;
		font-family: 'Mukta Vaani', sans-serif;
	}

	.nav1 a {
		margin: 0 10px;
		text-decoration: none;
		font-weight: 400;
		font-size: 18px;
		padding-right: 5px;
		color: #09244b;
	}
</style>
