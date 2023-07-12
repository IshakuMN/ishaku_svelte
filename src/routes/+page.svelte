<script>
	import Header from './header.svelte';
	import ComicButton from './Comic_button.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="home" content="home" />
</svelte:head>

<Header />

<body />

<ComicButton />

<style>
	body {
		background-image: url($lib/images/bg_image.svg);
		background-repeat: no-repeat;
		background-size: cover;
	}
</style>
