<script>
	import Navbar from "$lib/components/Nav.svelte";
	import About from "$lib/components/About.svelte";
	import Mission from "$lib/components/MissionStatement.svelte";
	import CoreValues from "$lib/components/CoreValues.svelte";
	import TargetMarkets from "$lib/components/TargetMarkets.svelte";
	import Team from "$lib/components/Team.svelte";
	import Contact from "$lib/components/Contact.svelte";
	import { onMount } from "svelte";

	// code for the carousel
	//because its svelte we need the life cycle onMount thing
	onMount(() => {
		//select all the elements in the DOM(document it think) with the data attribute
		const buttons = document.querySelectorAll("[data-carousel-button]");
		const slides = document.querySelector("[data-slides]");

		//function so we dont have to code our thing twice
		function changeSlide(offset) {
			const activeSlide = slides.querySelector("[data-active]");
			let newIndex = [...slides.children].indexOf(activeSlide) + offset;
			if (newIndex < 0) newIndex = slides.children.length - 1;
			if (newIndex >= slides.children.length) newIndex = 0;

			slides.children[newIndex].dataset.active = true;
			delete activeSlide.dataset.active;
		}

		buttons.forEach(button => {
			button.addEventListener("click", () => {
				console.log("clicked")
				const offset = button.dataset.carouselButton === "next" ? 1 : -1;
				changeSlide(offset);
			});
		});

		// autoplay functionality
		const interval = setInterval(() => {
			changeSlide(1);
		}, 5000); // Change every 5 seconds

		return () => clearInterval(interval); // Clean up intervals
	});
</script>

<!-- carousel testing -->
<div class="StartContainer">
	<section aria-label="Newest Photos" class="carousel-section">
		<div class="carousel" data-carousel>
			<button class="button carousel-button prev" data-carousel-button="prev"> &#8656;</button>
			<button class="button carousel-button next" data-carousel-button="next"> &#8658;</button>
			<ul data-slides>
				<li class="slide" data-active>
					<img src="https://images.unsplash.com/photo-1487958449943-2429e8be8625?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Real-Estate">
				</li>
				<li class="slide">
					<img src="https://images.unsplash.com/photo-1582407947304-fd86f028f716?q=80&w=1992&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Real-Estate">
				</li>
				<li class="slide">
					<img src="https://images.unsplash.com/photo-1462206092226-f46025ffe607?q=80&w=2074&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Real-Estate">
				</li>
			</ul>
		</div>
	</section>
	<Navbar />
	<div class="contentMain">
		<h1>Legacy 5</h1>
	</div>
</div>
<div class="bgImg2">
	<img src="starBG.jpg" alt="background" />
	<div class="wrapper">
		<div id="Mission"><Mission /></div>
	</div>
</div>

<div class="wrapper">
	<div id="About"><About /></div>
</div>

<div class="wrapper core">
	<div id="Values"><CoreValues /></div>
</div>
<!--
<div class="wrapper">
	<div id="Target"><TargetMarkets /></div>
</div>
-->
<div class="wrapper">
	<div id="Team"><Team /></div>
</div>
<div class="wrapper">
	<div id="Contact"><Contact /></div>
</div>

<style>
	*, *::before, *::after {
		box-sizing: border-box;
	}

	:global(body) {
		margin: 0;
		padding: 0;
	}

	ul {
		list-style-type: none;
		padding: 0;
		margin: 0;
	}

	.carousel-section {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		z-index: 0; /* Adjusted z-index */
	}

	.carousel {
		width: 100%;
		height: 100%;
		position: relative;
	}

	.slide {
		position: absolute;
		inset: 0;
		opacity: 0;
		transition: 200ms opacity ease-in-out;
		transition-delay: 200ms;
	}

	.slide > img {
		display: block;
		width: 100%;
		height: 100%;
		object-position: center;
		object-fit: cover;
	}

	.slide[data-active] {
		opacity: 1;
		transition-delay: 0;
		z-index: 1;
	}

	.carousel-button {
		z-index: 10;
		position: absolute;
		background: none;
		border: none;
		font-size: 4rem;
		top: 50%;
		transform: translateY(-50%);
		color: rgba(255, 255, 255, 0.5);
		cursor: pointer;
		border-radius: 0.25rem;
		/* padding: 0 0.5rem 0.8rem 0.5rem; */
		padding: 0 0 0.75rem 0;
		background-color: rgba(0, 0, 0, 0.1);
	}

	.carousel-button:hover,
	.carousel-button:focus {
		color: white;
		background-color: rgba(0, 0, 0, 0.2);
	}
	.carousel-button:focus {
		outline: 1px solid black;
	}

	.carousel-button.prev {
		left: 2rem;
	}

	.carousel-button.next {
		right: 2rem;
	}

	.StartContainer {
		color: white;
		width: 100%;
		height: 100vh;
		position: relative;
		overflow: hidden;
	}

	.contentMain {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		position: relative;
		z-index: 5; /* Adjusted z-index */
		pointer-events: none; /* Disable pointer events */
		margin-top: 9rem;
	}

	.contentMain h1 {
		font-size: 8rem;
		pointer-events: auto; /* Enable pointer events for h1 */
		color: rgb(51, 51, 51);
		text-shadow:  1px 1px 2px rgb(46, 1, 1),
		0 0 1em rgb(228, 220, 220),
		0 0 0.2em rgb(211, 218, 125);
	}

	.wrapper {
		display: flex;
		flex-direction: row;
		justify-content: center;
		width: 100%;
		padding: 0 20px;
	}

	#Mission {
		width: 100rem;
	}

	.bgImg2 img {
		width: 100%;
		height: 45rem;
		position: absolute;
		z-index: -1;
	}

	.core {
		background-color: rgb(135, 184, 188);
		width: auto;
	}

	@media (max-width: 900px) {
		.bgImg2 img {
			width: 100%;
			height: 1650px;
		}
	}
</style>
