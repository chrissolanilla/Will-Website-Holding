<script>
	function scrollToContent(param) {
		const contentElement = document.getElementById(param);
		if (contentElement) {
			contentElement.scrollIntoView({behavior:"smooth",block:"start"})
		}
	}
</script>

<svelte:head>
	<script src="https://kit.fontawesome.com/0bb12270a5.js" crossorigin="anonymous"></script>
</svelte:head>

<div class="navContainer">
	<div class="logoConainer">

		<svg width="65" height="80" viewBox="0 0 14 17" fill="none" xmlns="http://www.w3.org/2000/svg">
			<path d="M0.744 14V13.424L1.44 13.316C1.592 13.292 1.692 13.24 1.74 13.16C1.788 13.08 1.812 12.928 1.812 12.704V6.848C1.812 6.648 1.784 6.512 1.728 6.44C1.68 6.36 1.576 6.308 1.416 6.284L0.744 6.176V5.6H4.176V6.176L3.384 6.296C3.232 6.32 3.128 6.368 3.072 6.44C3.024 6.504 3 6.64 3 6.848V13.34H4.356C4.628 13.34 4.856 13.316 5.04 13.268C5.232 13.212 5.396 13.116 5.532 12.98C5.676 12.836 5.804 12.64 5.916 12.392C6.028 12.144 6.144 11.824 6.264 11.432H6.924L6.624 14H0.744Z" fill="black"/>
			<path d="M9.068 16.182C8.66933 16.182 8.288 16.1257 7.924 16.013C7.56867 15.9003 7.24367 15.7183 6.949 15.467C6.65433 15.207 6.403 14.8733 6.195 14.466L6.793 13.998C7.11367 14.414 7.45167 14.713 7.807 14.895C8.171 15.077 8.574 15.168 9.016 15.168C9.39733 15.168 9.718 15.0813 9.978 14.908C10.2467 14.7347 10.4503 14.4877 10.589 14.167C10.7363 13.8377 10.81 13.452 10.81 13.01C10.81 12.49 10.6583 12.0567 10.355 11.71C10.0603 11.3547 9.627 11.177 9.055 11.177C8.70833 11.177 8.40067 11.2247 8.132 11.32C7.86333 11.4153 7.59033 11.541 7.313 11.697L6.884 11.242L7.326 6.9H11.863L11.85 7.251L11.551 8.174H8.041L7.755 10.722C8.02367 10.566 8.301 10.4447 8.587 10.358C8.88167 10.2713 9.185 10.228 9.497 10.228C10.0517 10.228 10.5283 10.345 10.927 10.579C11.3257 10.8043 11.6333 11.1207 11.85 11.528C12.0667 11.9267 12.175 12.386 12.175 12.906C12.175 13.4347 12.1013 13.907 11.954 14.323C11.8067 14.7303 11.5943 15.0727 11.317 15.35C11.0397 15.6187 10.7103 15.8267 10.329 15.974C9.95633 16.1127 9.536 16.182 9.068 16.182Z" fill="#798ED8"/>
		</svg>
		<h1>Legacy 5</h1>
	</div>
	
	<nav>
		<ul>
			<li><a href="#mission" on:click|preventDefault={() => scrollToContent("Mission")}>Mission</a></li>
			<li><a href="#portfolio" on:click|preventDefault={() => scrollToContent("Portfolio")}>Portfolio</a></li>
			<li><a href="#about" on:click|preventDefault={() => scrollToContent("About")}>About</a></li>
			<li><a href="#values" on:click|preventDefault={() => scrollToContent("Values")}>Core Values</a></li>
			<li><a href="#team" on:click|preventDefault={() => scrollToContent("Team")}>Team</a></li>
			<li><a href="#Contact" on:click|preventDefault={() => scrollToContent("Contact")}>Contact</a></li>
		</ul>
	</nav>
</div>

<style>
	svg {
		padding-bottom: 1rem;
	}
	.logoConainer {
		display: flex;
		text-wrap: nowrap;
		column-gap: 1rem;
	}
	.navContainer {
		display: flex;
		justify-content: center;
		flex-direction: row;
		column-gap: 60rem;
		color: black;
		flex-wrap: wrap;
	}


	nav {
		padding: 2em;
		display: flex;
		align-items: center;
		justify-content: center;
		z-index: 1000; /* Ensure it's above other content */
	
	}

	ul {
		list-style: none;
		padding: 0;
		margin: 0;
		display: flex;
		justify-content: space-between;
	}

	li {
		margin-right: 20px;
	}

	a {
		text-decoration: none;
		color: #222020; /* White text color */
		font-weight: bolder;
		font-size: larger;
		transition: color 0.3s ease; /* Smooth transition for hover effect */
		z-index: 1000;
	}

	a:hover {
		color: #1e90ff; /* Change color on hover */
	}

	@media (max-width: 900px) {
		.navContainer {
			width: 21rem;
		}
	}


</style>