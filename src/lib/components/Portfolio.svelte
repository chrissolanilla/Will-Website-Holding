<script>
    import { onMount } from "svelte";
    import emblaCarouselSvelte from "embla-carousel-svelte";
    import Autoplay from "embla-carousel-autoplay";

    let options = { loop: false };
    let plugins = [Autoplay()];
    let items = [
        {
            src: "https://bcginc.wpenginepowered.com/wp-content/uploads/2023/02/DJI_0353-HDR-scaled-600x400.jpg",
            name: "Cheeca Lodge & Spa",
            link: "/cheeca-lodge",
        },
        {
            src: "https://bcginc.wpenginepowered.com/wp-content/uploads/2023/02/DJI_0437-scaled-600x400.jpg",
            name: "Ocean Isles Fishing Village",
            link: "/ocean-isles",
        },
        {
            src: "https://bcginc.wpenginepowered.com/wp-content/uploads/2015/08/Solar-Stock-Pic-for-Webpage-600x400.jpeg",
            name: "Bahamas Solar Project",
            link: "/bahamas-solar",
        },
        {
            src: "https://bcginc.wpenginepowered.com/wp-content/uploads/2015/07/The_Palace_1.jpg",
            name: "The Palace at Weston",
            link: "/the-palace",
        },
        {
            src: "https://bcginc.wpenginepowered.com/wp-content/uploads/2015/07/KWCH_1.png",
            name: "Key West City Hall",
            link: "/woodland-pet-lodge",
        },
        {
            src: "https://bcginc.wpenginepowered.com/wp-content/uploads/2020/03/Woodland_Lodge_Pet_Resort_Front_Low_Light-REDUCED-SIZWE-scaled-800x415.jpg",
            name: "Woodland Pet Lodge",
            link: "/woodland-pet-lodge",
        },
    ];

    onMount(() => {
        const updateOptions = () => {
            if (window.innerWidth < 900) {
                options = { loop: false, slidesToScroll: 1 };
            } else {
                options = { loop: false, slidesToScroll: 3 };
            }
        };
        window.addEventListener("resize", updateOptions);
        updateOptions();
    });
</script>

<h1>Our Projects</h1>
<div class="portfolioContainer">
    <div class="my-slider">
        <div class="embla" use:emblaCarouselSvelte={{ options, plugins }}>
            <div class="embla__container">
                {#each items as item, index}
                    <div class="embla__slide">
                        <div class="propertyContainer">
                            <a href={item.link}>
                                <img src={item.src} alt="property" />
                                <button class="itembuttonname">
                                    {item.name}
                                </button>
                                <!-- <p class="description">{item.name}</p> -->
                            </a>
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </div>
</div>

<style>
    .itembuttonname {
        /* margin-right: 1rem; */
        margin-left: 1rem;
        margin-top: 0.5rem;
        font-weight: bold;
    }
    h1 {
        color: white;
        text-align: center;
    }

    .propertyContainer {
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
    }

    .itembuttonname {
        padding: 10px 20px;
        background-color: #e8e4d8;
        color: rgb(0, 0, 0);
        border: none;
        border-radius: 5px;
        cursor: pointer;
        font-size: 1rem;
        transition: background-color 0.3s ease;
    }
    .itembuttonname:hover {
        background-color: #5699a3;
    }

    .embla {
        overflow: hidden;
        width: 100%;
    }

    .embla__container {
        display: flex;
        padding: 2rem 0 1rem 0;
        gap: 1rem;
    }

    .embla__slide {
        flex: 0 0 calc(33.33% - 1rem); /* Adjusted to ensure spacing */
        min-width: calc(33.33% - 1rem); /* Adjusted to ensure spacing */
        display: flex;
        justify-content: center;
        box-sizing: border-box;
    }

    .portfolioContainer {
        display: flex;
        padding: 1rem;
        width: 100%;
        justify-content: center;
    }

    .my-slider {
        display: flex;
        background-color: rgb(169, 220, 240);
        border-radius: 1rem;
        padding: 1rem;
        margin-right: 1.8rem;
        width: 100%;
        overflow: hidden;
        position: relative;
        color: white;
        box-sizing: border-box;
    }

    img {
        width: 100%;
        max-width: 400px;
        height: 266.67px;
        margin: 0 1rem;
        border-radius: 0.5rem;
    }
    img:hover {
        transform: scale(1.1);
        transition: 0.3s ease;
    }

    a:link {
        color: black;
    }
    a:visited {
        color: black;
    }
    /* Mobile Styles */
    @media (max-width: 900px) {
        .embla__slide {
            flex: 0 0 100%;
            min-width: 100%;
            padding: 0;
        }

        .propertyContainer {
            width: 100%;
            padding: 0 1rem;
        }

        .my-slider {
            flex-direction: column;
            width: 60%;
            gap: 0;
            margin-right: 2rem;
        }

        img {
            width: 100%;
            height: 266.67px;
            margin: 0;
        }
    }
</style>
