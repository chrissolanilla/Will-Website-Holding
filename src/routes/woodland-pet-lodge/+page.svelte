<script>
    import Navbar from "$lib/components/Nav.svelte";
    import Contact from "$lib/components/Contact.svelte";
</script>

<div class="Navbar">
    <Navbar />
</div>

<div class="PageContainer">
    <div class="TitleContainer">
        <h1>Woodland Lodge Pet Resort</h1>
    </div>

    <div class="BodyContainer">
        <div class="Row1">
            <div class="Text">
                <div>
                    Location: Doral, Florida
                </div>
                <div>
                    <p>Completion Date: 2016</p>
                </div>
                <p>
                    Description: Woodland Pet Resort, is Miami's premiere boarding facility for cats and dogs. 
                    Offering resort-style boarding, doggy daycare, training, and grooming.
                </p>
                <p>
                    This pet resort features 40 luxury pet condos with an interactive TV, cameras, and video 
                    giving owners access to view their pets during their stay. This project also included a new 
                    lobby, two kitchens, an outdoor pool, indoor daycare, and a social room for the pets.
                </p>
            </div>
            <div class="Image">
                <img src="https://bcginc.wpenginepowered.com/wp-content/uploads/2020/03/Woodland_Lodge_Pet_Resort_Front_Low_Light-REDUCED-SIZWE-scaled.jpg" alt="Woodland Lodge Pet Resort">
            </div>
        </div>

        <div class="Row2">
            <img class="img1" src="https://bcginc.wpenginepowered.com/wp-content/uploads/2020/04/Woodland_Lodge_Pet_Resort_Back-Reduced-Size-1.png" alt="Woodland Lodge Pet Resort">
            
            <img class="img2" src="https://bcginc.wpenginepowered.com/wp-content/uploads/2020/04/Woodland_Lodge_Pet_Resort_Reception-Reduced-Size.png" alt="Woodland Lodge Pet Resort">

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

    @media (max-width:900px){
        :global(html){
			overflow-x: hidden;
		}
		:global(body){
			max-width: 100%;
			overflow-x: hidden;
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
        .PageContainer{
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 2rem;
            flex-wrap: calc(100vw/3);
            gap: 5px;
        }
        .TitleContainer{
            margin-left: 0;
            margin-bottom: -2rem;   
        }
        .Row1{
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            width: 100rem;
            padding: 1rem;
            flex-wrap: calc(100vw/3);
            gap: 50px;
        }
        .Row2{
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            width: 100rem;
            padding: 1rem;
            flex-wrap: calc(100vw/3);
            gap: 50px;
        }
        .Text{  
            width: 300px;
            margin: 0;
            font-size: 20px;
            display: block;
            position: relative;
        }
    }

</style>