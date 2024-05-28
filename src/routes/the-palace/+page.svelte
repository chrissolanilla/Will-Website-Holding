<script>
    import Navbar from "$lib/components/Nav.svelte";
    import Contact from "$lib/components/Contact.svelte";
</script>

<div class="Navbar">
    <Navbar />
</div>

<div class="PageContainer">
    <div class="TitleContainer">
        <h1>The Palace At Weston</h1>
    </div>

    <div class="BodyContainer">
        <div class="Row1">
            <div class="Text">
                <div>
                    Location: Weston, Florida
                </div>
                <p>
                    Description: The Palace at Weston is situated on 25 acres of residentially zoned land in Weston. 
                    The Palace includes 350 condominium units. The units are two and three bedrooms, and each unit 
                    has a covered terrace. The four buildings and 32 villas are surrounding a central lake. The 
                    Mediterranean style buildings are situated in such a way that each building has breathtaking 
                    views of the lake and they interconnected with meandering walking paths. The Palace includes a 
                    man made lake with surrounding jogging paths as well as a pool, two spas, fitness center, aerobics 
                    room, day spa/beauty salon, billiard room, card rooms, library, wellness center, bar/lounge, 
                    dining event rooms, and a coffee/ shop.
                </p>
            </div>
            <div class="Image">
                <img src="https://bcginc.wpenginepowered.com/wp-content/uploads/2015/07/The_Palace_1.jpg" alt="Weston Palace">
            </div>
        </div>

        <div class="Row2">
            <img class="img1" src="https://bcginc.wpenginepowered.com/wp-content/uploads/2015/07/The_Palace_11.jpg" alt="Weston Palace">
            
            <img class="img2" src="https://bcginc.wpenginepowered.com/wp-content/uploads/2015/07/The_Palace_3.jpg" alt="Weston Palace">

        </div>
        
    </div>
</div>

<div class="wrapper contact">
	<div id="Contact"><Contact /></div>
</div>


<style>
    .Navbar{
        background-color: #c5c5c5;
    }
    .wrapper {
		display: flex;
		flex-direction: row;
		justify-content: center;
		width: 100%;
		padding: 0 20px;
	}
    .contact{
		background: linear-gradient(to bottom, #333333 0%, #414242 100%);
		color: white;
	}
    .BodyContainer{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 2rem;
        flex-wrap: calc(100vw/3);
        gap: 5px;
    }
    .Text{
        width: 600px;
        margin: 0;
        font-size: 20px;
        display: block;
        position: relative;
    }
    .TitleContainer{
        margin-left: 20rem;
        margin-bottom: -2rem;
    }
    .Row1{
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        width: 100rem;
        padding: 1rem;
        flex-wrap: calc(100vw/3);
        gap: 50px;
    }
    .Row2{
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        width: 100rem;
        padding: 1rem;
        flex-wrap: calc(100vw/3);
        gap: 50px;
    }
    img{
        height: 400px;
        width: 600px;
    }

</style>