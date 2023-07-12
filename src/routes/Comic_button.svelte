<script>
	import loadComic from '../routes/Comic/+page.svelte';
</script>

<div class="center-screen">
	<a href="/Comic" class="no-underline">
		<button class="comic-button">Comic</button>
	</a>
</div>

<style>
	.center-screen {
		display: flex;
		align-items: center;
		justify-content: center;
		height: 30vh;
	}

	.no-underline {
		text-decoration: none;
	}

	.comic-button {
		justify-content: center;
		align-items: center;
		font-family: 'Mukta Vaani', sans-serif;
		font-size: 20px;
		width: 100px;
		height: 40px;
		color: #09244b;
		border-radius: 8px;
		border: 1px solid #09244b;
		background-color: aliceblue;
	}
	.comic-button:hover {
		border: none;
		background-image: url('$lib/images/comic-bg-img.png');
		background-repeat: no-repeat;
		background-size: cover;
		background-position: center;
		margin: 20px;
		background-color: aliceblue;
		border: 1px solid #09244b;
	}
</style>
