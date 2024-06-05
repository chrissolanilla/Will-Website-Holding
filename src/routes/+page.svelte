<script>
    import Navbar from "$lib/components/Nav.svelte";
    import About from "$lib/components/About.svelte";
    import Mission from "$lib/components/MissionStatement.svelte";
    import Team from "$lib/components/Team.svelte";
    import Contact from "$lib/components/Contact.svelte";
    import { onMount } from "svelte";
    import Portfolio from "../lib/components/Portfolio.svelte";

    function scrollToContent() {
        const contentElement = document.getElementById("Mission");
        if (contentElement) {
            contentElement.scrollIntoView({
                behavior: "smooth",
                block: "start",
            });
        }
    }
    // code for the carousel
    //because its svelte we need the life cycle onMount thing
    let hiddenElements = [];
    let observer;
    onMount(() => {
        if ("IntersectionObserver" in window) {
            observer = new IntersectionObserver((entries) => {
                entries.forEach((entry) => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add("show");
                    } else {
                        entry.target.classList.remove("show");
                    }
                });
            });

            hiddenElements = document.querySelectorAll(".hidden");

            hiddenElements.forEach((el) => observer.observe(el));
        }
        window.addEventListener("load", () => {
            const hiddenElements = document.querySelectorAll(".hidden");
            hiddenElements.forEach((el) => observer.observe(el));
        });
        //select all the elements in the DOM(document it think) with the data attribute
        const buttons = document.querySelectorAll("[data-carousel-button]");
        const slides = document.querySelector("[data-slides]");
        //this is for the scroll animations
        hiddenElements.forEach((el) => observer.observe(el));
        //function so we dont have to code our thing twice
        function changeSlide(offset) {
            const activeSlide = slides.querySelector("[data-active]");
            let newIndex = [...slides.children].indexOf(activeSlide) + offset;
            if (newIndex < 0) newIndex = slides.children.length - 1;
            if (newIndex >= slides.children.length) newIndex = 0;

            slides.children[newIndex].dataset.active = true;
            delete activeSlide.dataset.active;
        }

        buttons.forEach((button) => {
            button.addEventListener("click", () => {
                console.log("clicked");
                const offset =
                    button.dataset.carouselButton === "next" ? 1 : -1;
                changeSlide(offset);
            });
        });

        // autoplay functionality
        const interval = setInterval(() => {
            changeSlide(1);
        }, 5000); // Change every 5 seconds

        return () => clearInterval(interval); // Clean up intervals
    });

    //code to have scroll animations
</script>

<!-- carousel testing -->
<div class="StartContainer">
    <section aria-label="Newest Photos" class="carousel-section">
        <div class="carousel" data-carousel>
            <button
                class="button carousel-button prev"
                data-carousel-button="prev"
            >
                &#8656;</button
            >
            <button
                class="button carousel-button next"
                data-carousel-button="next"
            >
                &#8658;</button
            >
            <ul data-slides>
                <li class="slide" data-active>
                    <img
                        src="https://images.unsplash.com/photo-1487958449943-2429e8be8625?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                        alt="Real-Estate"
                    />
                </li>
                <li class="slide">
                    <img
                        src="https://images.unsplash.com/photo-1582407947304-fd86f028f716?q=80&w=1992&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                        alt="Real-Estate"
                    />
                </li>
                <li class="slide">
                    <img
                        src="https://images.unsplash.com/photo-1462206092226-f46025ffe607?q=80&w=2074&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                        alt="Real-Estate"
                    />
                </li>
            </ul>
        </div>
    </section>
    <div class="Navbar">
        <Navbar />
    </div>
    <div class="contentMain">
        <h1>Investing in Tomorrow's Opportunities</h1>
        <p>
            Legacy 5 empowers you to build a prosperous future through strategic
            private equity investments.
        </p>
        <button
            id="downArrowButton"
            on:click={scrollToContent}
            style="pointer-events: all; background: transparent; border: none;"
        >
            <svg
                width="75"
                height="35"
                version="1.1"
                viewBox="-2 -2 196 100"
                xmlns="http://www.w3.org/2000/svg"
            >
                <path
                    d="m12 12 84 72 84-72"
                    fill="none"
                    stroke="black"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="24"
                    style="paint-order:stroke fill markers"
                ></path>
                <path
                    d="m12 12 84 72 84-72"
                    fill="none"
                    stroke="grey"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="15"
                    style="paint-order:stroke fill markers"
                ></path>
            </svg>
        </button>
    </div>
</div>

<div class="wrapper missionBG">
    <div id="Mission" class="hidden"><Mission /></div>
</div>

<div class="wrapper portfolioBG">
    <div id="Portfolio" class="hidden"><Portfolio /></div>
</div>

<div class="wrapper about" id="test">
    <div id="About" class="hidden"><About /></div>
</div>

<div class="wrapper team">
    <div id="Team" class="hidden"><Team /></div>
</div>
<div></div>
<div class="wrapper contact">
    <div id="Contact" class="hidden"><Contact /></div>
</div>

<style>
    *,
    *::before,
    *::after {
        box-sizing: border-box;
    }

    :global(body) {
        margin: 0;
        padding: 0;
        overflow-x: hidden;
    }
    :global(.hidden) {
        opacity: 0;
        transition: all 0.5s;
        filter: blur(5px);
        transform: translateX(-100%);
    }
    :global(.show) {
        opacity: 1;
        filter: blur(0);
        transform: translateX(0);
    }
    /* Staggered animations for each child */
    :global(.statChild) {
        opacity: 0; /* Start hidden */
        transform: translateX(-100%);
        transition:
            opacity 0.5s,
            transform 0.5s; /* Base transition */
    }
    :global(.show .statChild) {
        opacity: 1;
        transform: translateX(0);
    }
    :global(.show .statChild:nth-child(1)) {
        transition-delay: 0.2s;
    }
    :global(.show .statChild:nth-child(2)) {
        transition-delay: 0.4s;
    }
    :global(.show .statChild:nth-child(3)) {
        transition-delay: 0.6s;
    }
    ul {
        list-style-type: none;
        padding: 0;
        margin: 0;
    }
    .Navbar {
        background-color: #ffffff;
        z-index: 9999999;
        position: relative;
    }
    .portfolioBG {
        background-color: #6da3bb;
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
        /* background-color: blue; */
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

    #downArrowButton {
        margin-top: 22rem;
    }
    .slide[data-active] {
        opacity: 1;
        transition-delay: 0;
        z-index: 0;
        /* background-color: red; this also dosent work  */
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
        width: 100vw;
        height: 98vh;
        position: relative;
        overflow: hidden;
        /* background-color: blue; this dosent show  */
    }

    .contentMain {
        display: flex;
        flex-direction: column;
        /* row-gap: 14rem; */
        justify-content: center;
        align-items: center;
        position: relative;
        z-index: 5; /* Adjusted z-index */
        pointer-events: none; /* Disable pointer events */
        background-color: rgba(0, 0, 0, 0.5); /*this works */
        height: 98vh;
    }

    .contentMain h1 {
        margin-bottom: 0;
        font-size: 6rem;
        pointer-events: auto; /* Enable pointer events for h1 */
        /* color: rgb(51, 51, 51); */
        text-shadow:
            1px 1px 2px rgb(54, 245, 245),
            0 0 1em rgb(228, 220, 220),
            0 0 0.2em rgb(63, 93, 230);
        text-align: center; /*fixes mobile view */
    }

    .contentMain p {
        font-size: 2rem;
        text-align: center; /*fixes mobile view */
        pointer-events: auto;
    }
    .contentMain button {
        pointer-events: auto;
    }
    .contentMain svg {
        bottom: 0%;
    }

    .wrapper {
        display: flex;
        flex-direction: row;
        justify-content: center;
        width: 100%;
        padding: 0 20px;
    }

    .about {
        background: #ced6d9;
        color: black;
    }

    .team {
        background: linear-gradient(to top, #102f58 0%, #5785a9 100%);
    }
    .contact {
        background-color: black;
        color: white;
    }

    #Mission {
        max-width: 100rem;
    }

    @media (max-width: 900px) {
        :global(html) {
            overflow-x: hidden;
        }
        :global(body) {
            max-width: 100%;
            overflow-x: hidden;
        }
        ul {
            overflow-x: hidden;
        }
        section::before {
            overflow-x: hidden;
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 99999;
        }
        .contentMain h1 {
            font-size: 50px;
            padding: 20px;
            /* background-color: rgba(0,0,0,0.7); */
        }
        .contentMain {
            height: 85vh;
            padding: 20px;
            /* background-color: rgba(0,0,0,0.7); */
        }
        .contentMain p {
            font-size: 6rem;
        }
        .carousel-button.prev {
            left: 0.1rem;
            font-size: 2rem;
        }

        .carousel-button.next {
            right: 0.1rem;
            font-size: 2rem;
        }
        .contentMain p {
            font-size: 1.2rem; /* Reduced font size for mobile */
            text-align: center;
        }

        #downArrowButton {
            margin-top: 9.5rem;
        }
    }
</style>
