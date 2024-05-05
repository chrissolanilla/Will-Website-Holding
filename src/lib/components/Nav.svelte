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
        <li><a href="#" on:click|preventDefault={() => scrollToContent("About")}>About</a></li>
        <li><a href="#" on:click|preventDefault={() => scrollToContent("Approach")}>Approach</a></li>
        <li><a href="#" on:click|preventDefault={() => scrollToContent("Values")}>Core Values</a></li>
        <li><a href="#" on:click|preventDefault={() => scrollToContent("Target")}>Target Markets</a></li>
        <li><a href="#" on:click|preventDefault={() => scrollToContent("Team")}>Team</a></li>
        <li><a href="#" on:click|preventDefault={() => scrollToContent("Contact")}>Contact</a></li>
    </ul>
</nav>