<script>
	import { onMount } from 'svelte';
	import emblaCarouselSvelte from 'embla-carousel-svelte'
	import Autoplay from 'embla-carousel-autoplay'

	let options = { loop: false }  
	let plugins = [Autoplay()]
	let items = [
		"https://bcginc.wpenginepowered.com/wp-content/uploads/2023/02/DJI_0353-HDR-scaled-600x400.jpg",
		"https://bcginc.wpenginepowered.com/wp-content/uploads/2023/02/DJI_0437-scaled-600x400.jpg",
		"https://bcginc.wpenginepowered.com/wp-content/uploads/2015/08/Solar-Stock-Pic-for-Webpage-600x400.jpeg",
		"https://bcginc.wpenginepowered.com/wp-content/uploads/2015/07/The_Palace_1.jpg",
		"https://bcginc.wpenginepowered.com/wp-content/uploads/2015/07/KWCH_1.png",
		"https://bcginc.wpenginepowered.com/wp-content/uploads/2020/03/Woodland_Lodge_Pet_Resort_Front_Low_Light-REDUCED-SIZWE-scaled-800x415.jpg"
	];
</script>

<h1>Our Projects</h1>
<div class="portfolioContainer">
	
	<div class="my-slider">
		<div class="embla" use:emblaCarouselSvelte="{{ options, plugins }}">
			<div class="embla__container">
					<div class="embla__slide">
						<div class="propertyContainer">
							<a href="/cheeca-lodge">
								<img src={items[0]} alt="property" />
								<p class="description">Cheeca Lodge & Spa</p>

							</a>
						</div>
						<div class="propertyContainer">
							<a href="/ocean-isles">
								<img src={items[1]} alt="property"/>
								<p class="description">Ocean Isles Fishing Vilalge</p>

							</a>
						</div>
						<div class="propertyContainer">
							<a href="/bahamas-solar">
								<img src={items[2]} alt="property"/>
								<p class="description">Bahamas Solar Project</p>

							</a>
						</div>	
					</div>
					<div class="embla__slide">
						<div class="propertyContainer">
							<a href="/the-palace">
								<img src={items[3]} alt="property"/>
								<p class="description">The Palace at Weston</p>

							</a>
						</div>
						<div class="propertyContainer">
							<a href="/key-west-city-hall">
								<img src={items[4]} alt="property"/>
								<p class="description">Key West City Hall</p>

							</a>
						</div>
						<div class="propertyContainer">
							<a href="/woodland-pet-lodge">
								<img src={items[5]} alt="property"/>
								<p class="description">Woodland Pet Lodge</p>

							</a>
						</div>
					</div>
				</div>
		</div>
		
	</div>
	
</div>

<style>

	h1{
		color: white;
	}
	.propertyContainer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		text-align: center;
	}
	.description {
		margin-left: 1.2rem;
	}
	.embla {
		overflow: hidden;
	}
	.embla__container {
		display: flex;
		padding:  2rem 0 1rem 0;
	}
	.embla__slide {
		flex: 0 0 100%;
		min-width: 0;
		display: flex;
		justify-content: center;
		column-gap: 3rem;
	}
	h1 {
		text-align: center;
	}
	.portfolioContainer {
		display: flex;
		padding: 1rem;
		width: 100rem;
		justify-content: center;
	}
	.my-slider {
		display: flex;
		column-gap: 1rem;
		background-color: rgb(61, 180, 228);
		border-radius: 1rem;
		padding: 1rem;
		width: 100rem;
		overflow: hidden;
		position: relative;
		color: white;
	}

	img {
		width: 400px;
		height: 333px;
		margin: 0 1rem;
		border-radius: 0.5rem;
	}
	.carousel-button {
		background-color: #007BFF;
		border: none;
		color: white;
		padding: 10px 20px;
		text-align: center;
		text-decoration: none;
		display: inline-block;
		font-size: 16px;
		margin: 4px 2px;
		cursor: pointer;
	}
</style>
