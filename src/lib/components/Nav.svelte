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
    <div class="icons">
        <a href="https://www.linkedin.com/company/burkeconstructiongroup">
            <i class="fa fa-linkedin" aria-hidden="true"></i>
        </a>
        <a href="https://www.linkedin.com/company/burkeconstructiongroup"> 
            <i class="fa fa-instagram" aria-hidden="true"></i>
        </a>
        <a href="https://www.facebook.com/BurkeConstructionGroupInc/">
            <i class="fa fa-facebook" aria-hidden="true"></i>
        </a>
        <a href="https://www.youtube.com/channel/UCvopoFV385wOPjFQPDb6k5A">
            <i class="fa fa-youtube" aria-hidden="true"></i>
        </a>
    </div>

    <div class="Logo">
        <h3>Legacy 5</h3>
    </div>



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
</div>

<style>
    .navContainer {
        display: flex;
        justify-content: center;
        flex-direction: row;
        column-gap: 65rem;
        flex-wrap: wrap;
    }

    .icons {    
        display:flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
    }

    i {
        padding:0.4rem;
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
        color: #fff; /* White text color */
        font-weight: bold;
        transition: color 0.3s ease; /* Smooth transition for hover effect */
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