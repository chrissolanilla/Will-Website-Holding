<script>
    import Navbar from "$lib/components/Nav.svelte";
    import Contact from "$lib/components/Contact.svelte";
</script>

<div class="Navbar">
    <Navbar />
</div>

<div class="PageContainer">
    <div class="TitleContainer">
        <h1>Ocean Isles Fishing Village</h1>
    </div>

    <div class="BodyContainer">
        <div class="Row1">
            <div class="Text">
                <div>
                    Location: Marathon, Florida
                </div>
                <div>
                    <p>Completion Date: November 2022</p>
                </div>
                <p>
                    Description: Ocean Isles Fishing Village is an oceanfront complex in the 
                    heart of the Florida Keys. This 108,000-square-foot property was rebuilt 
                    with 126 concrete block units.
                </p>
                <p>
                    With extensive site work, this complex now features a brand new community 
                    center, an elevated pool overlooking the Atlantic Ocean, and a rebuilt 
                    marina. Units are two stories of modern living space totaling about 800 
                    s.f. with a full-sized kitchen, living room, bath, and bedroom.
                </p>
            </div>
            <div class="Image">
                <img src="https://bcginc.wpenginepowered.com/wp-content/uploads/2023/02/DJI_0437-scaled-600x400.jpg" alt="Ocean Isles">
            </div>
        </div>

        <div class="Row2">
            <img class="img1" src="https://bcginc.wpenginepowered.com/wp-content/uploads/2023/03/DJI_0433-scaled-600x400.jpg" alt="Pier">
            
            <img class="img2" src="https://bcginc.wpenginepowered.com/wp-content/uploads/2023/03/DJI_0440-scaled-600x400.jpg" alt="Above Ocean Isles">

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
        width: 100rem;
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
        padding-left: 12.5rem;
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

</style>