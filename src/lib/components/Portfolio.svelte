<script>
	import { onMount } from 'svelte';
	import 'tiny-slider/dist/tiny-slider.css';

	let items = [
		"https://bcginc.wpenginepowered.com/wp-content/uploads/2023/02/DJI_0353-HDR-scaled-600x400.jpg",
		"https://bcginc.wpenginepowered.com/wp-content/uploads/2023/02/DJI_0437-scaled-600x400.jpg",
		"https://bcginc.wpenginepowered.com/wp-content/uploads/2015/08/Solar-Stock-Pic-for-Webpage-600x400.jpeg"
	];

	onMount(async () => {
		const { tns } = await import('tiny-slider/src/tiny-slider');

		tns({
			container: '.my-slider',
			items: 1,
			slideBy: 'page',
			autoplay: true,
			controls: true,
			nav: true
		});
	});
</script>

<div class="portfolioContainer">
	<h1>Look at our projects!</h1>
	<div class="my-slider">
		{#each items as item}
			<div>
				<img src={item} alt="Real-Estate">
			</div>
		{/each}
	</div>
</div>

<style>
	.portfolioContainer {
		width: 100%;
		padding: 20px;
	}

	.my-slider {
		width: 100%;
		height: 400px;
	}

	.my-slider img {
		width: 100%;
		height: auto;
		object-fit: cover;
	}

	.tns-controls {
		display: flex;
		justify-content: space-between;
		position: absolute;
		top: 50%;
		width: 100%;
		transform: translateY(-50%);
	}

	.tns-controls button {
		background-color: #007bff;
		color: white;
		border: none;
		padding: 10px;
		cursor: pointer;
		margin: 5px;
	}

	.tns-controls button:disabled {
		background-color: #cccccc;
	}
</style>
