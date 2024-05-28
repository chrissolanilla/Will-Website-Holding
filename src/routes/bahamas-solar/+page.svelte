<script>
    import Navbar from "$lib/components/Nav.svelte";
    import Contact from "$lib/components/Contact.svelte";
</script>

<div class="Navbar">
    <Navbar />
</div>

<div class="PageContainer">
    <div class="TitleContainer">
        <h1>Bahamas Solar Project</h1>
    </div>

    <div class="BodyContainer">
        <div class="Row1">
            <div class="Text">
                <div>
                    Location: Bahamas
                </div>
                <div>
                    <p>Completion Date: 2020</p>
                </div>
                <p>
                    Description:  A 1.5 megawatt (MW) Micro Grid Solar system with 2 MW battery backup on a private island located in the Bahamas.
                </p>
            </div>
            <div class="Image">
                <img src="https://bcginc.wpenginepowered.com/wp-content/uploads/2023/07/1686917416581.jpeg" alt="Solar panels">
            </div>
        </div>

        <div class="Row2">
            <img class="img1" src="https://bcginc.wpenginepowered.com/wp-content/uploads/2023/07/1686917414197.jpeg" alt="Solar Panels">
            
            <img class="img2" src="https://bcginc.wpenginepowered.com/wp-content/uploads/2023/07/1686917414151.jpeg" alt="Solar Panels">

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