<script>
    function scrollToContent(param) {
        const contentElement = document.getElementById(param);
        if (contentElement) {
            contentElement.scrollIntoView({behavior:"smooth",block:"start"})
        }
    }
</script>

<nav>
    <ul>
        <li><a href="#about" on:click|preventDefault={() => scrollToContent("About")}>About</a></li>
        <li><a href="#approach" on:click|preventDefault={() => scrollToContent("Approach")}>Approach</a></li>
        <li><a href="#values" on:click|preventDefault={() => scrollToContent("Values")}>Core Values</a></li>
        <li><a href="#target" on:click|preventDefault={() => scrollToContent("Target")}>Target Markets</a></li>
        <li><a href="#team" on:click|preventDefault={() => scrollToContent("Team")}>Team</a></li>
        <li><a href="#Contact" on:click|preventDefault={() => scrollToContent("Contact")}>Contact</a></li>
    </ul>
</nav>

<style>
    nav {
    background-color: #0b162e; /* Dark background */
    padding-bottom: 2em;
    width: 100%;
    margin-left: 0;
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
        color: #fff; /* White text color */
        font-weight: bold;
        transition: color 0.3s ease; /* Smooth transition for hover effect */
    }
    a:hover {
        color: #1e90ff; /* Change color on hover */
    }
</style>