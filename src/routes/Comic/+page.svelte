<script lang="ts">
	import { onMount } from 'svelte';

	interface ComicData {
		id: number;
		img: string;
		safe_title: string;
		year: number;
		month: number;
		day: number;
	}

	let comicData: ComicData | null = null;

	async function loadComic() {
		const email: string = 'i.march@innopolis.university';
		const apiUrl: string = `https://fwd.innopolis.university/api/hw2?email=${email}`;

		try {
			const response = await fetch(apiUrl);
			const data: string = await response.text();
			const comicId: number = parseInt(data, 10);

			const comicUrl: string = `https://fwd.innopolis.university/api/comic?id=${comicId}`;
			const comicResponse = await fetch(comicUrl);
			comicData = await comicResponse.json();
		} catch (error) {
			console.log(error);
		}
	}

	onMount(loadComic);
</script>

<svelte:head>
	<title>comic</title>
	<meta name="Comic" content="desplays comic image" />
</svelte:head>

<div class="image-figure">
	{#if comicData}
		<img src={comicData.img} alt="Comic Image" id="comicImage" />
		<h3 id="comicTitle">Title: {comicData.safe_title}</h3>
		<h3 id="comicDate">
			Date: {new Date(comicData.year, comicData.month - 1, comicData.day).toLocaleDateString()}
		</h3>
	{/if}
</div>

<style>
	.image-figure {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 50vh;
		padding-top: 80px;
	}

	.image-figure img {
		max-width: 100%;
		max-height: 100%;
	}

	h3 {
		text-align: center;
		font-size: 1.2rem;
		font-weight: 500;
		line-height: 1.5;
		color: #09244b;
		font-family: 'Mukta Vaani', sans-serif;
	}
	.image-figure h3 {
		margin-bottom: 0px;
	}
</style>
