<script>
    function scrollToContent() {
		const contentElement = document.getElementById("About");
		if (contentElement) {
			contentElement.scrollIntoView({behavior:"smooth",block:"start"})
            console.log("TEST")
		}
	}
</script>
<div class="mission-container">
    <div class="overlay">
    <div class="mission-content">
        <h1>Investing with Integrity</h1>
        <p>At Legacy 5, we focus on Value-Add and Core-Plus strategies to yield appropriate risk-adjusted returns.</p>
        <p>Our goal is to enhance the value of Miami apartments through strategic investments and strong partnerships.</p>
        <button class="learn-more-button" on:click={scrollToContent("test")}>Learn More</button>
    </div>
    <div class="mission-details">
        <div class="detail">
            <h3><i class="fas fa-building"></i> High-Quality Properties</h3>
            <p>We identify properties with growth potential in desirable locations, ensuring sustainable value creation.</p>
        </div>
        <div class="detail">
            <h3><i class="fas fa-chart-line"></i> Return and Yield Driven</h3>
            <p>Our investments target both return-driven and yield-driven opportunities in multifamily, retail, and office sectors.</p>
        </div>
    </div>
</div>
</div>

<style>
.mission-container {
    position: relative;
    color: white;
    text-align: center;
    padding: 4rem;
}

.overlay {
    background: rgba(0, 0, 0, 0.5); /* Semi-transparent overlay */
    z-index: 1;
    border-radius: 15px;
    padding: 4rem;
}

.mission-content {
    position: relative;
    z-index: 2;
    margin-bottom: 30px;
}

.mission-content h1 {
    font-size: 3rem;
    color: #84b0d4;
    text-shadow: 1px 1px 2px red, 0 0 1em blue, 0 0 0.2em blue;
}

.mission-content p {
    font-size: 1.2rem;
    margin: 0 0 10px 0;
    color: #ffffff;
}

.learn-more-button {
    margin-top: 20px;
    padding: 10px 20px;
    background-color: #87b8bc;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1rem;
    transition: background-color 0.3s ease;
}

.learn-more-button:hover {
    background-color: #5699a3;
}

.mission-details {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    position: relative;
    z-index: 2;
}

.detail {
    max-width: 300px;
    margin: 10px;
    padding: 20px;
    background: rgba(255, 255, 255, 0.2);
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    text-align: left;
}

.detail h3 {
    color: #87b8bc;
    display: flex;
    align-items: center;
    margin-bottom: 10px;
}

.detail h3 i {
    margin-right: 10px;
    font-size: 1.5rem;
}

.detail p {
    font-size: 1rem;
    color: #ffffff;
}
</style>


