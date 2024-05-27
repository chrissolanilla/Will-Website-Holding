<script>
    import Navbar from "$lib/components/Nav.svelte";
    import Contact from "$lib/components/Contact.svelte";
</script>

<div class="Navbar">
    <Navbar />
</div>

<div class="PageContainer">
    <div class="TitleContainer">
        <h1>Cheeca Lodge & Spa</h1>
    </div>

    <div class="BodyContainer">
        <div class="Row1">
            <div class="Text">
                <div>
                    Location: Islamorada, Florida
                </div>
                <div>
                    <p>Completion Date: November 2022</p>
                </div>
                <p>Description: As Islamorada embraces its transformation, Cheeca Lodge and Spa are ready to grow alongside it. 
                    Acknowledging the surge in tourists flocking to the renowned “Sporting Fishing Capital of the World,” the 
                    resort embarked on an expansion endeavor to meet the escalating demands of this increasingly popular 
                    destination.
                </p>
                <p>
                    The expansion project involved the construction of a new wing, consisting of 43 contemporary rooms and suites, 
                    each offering awe-inspiring ocean views. Additionally, a cutting-edge conference center has been incorporated, 
                    featuring two spacious ballrooms, a well-equipped kitchen, and inviting bars. This conference center is 
                    designed to cater to a diverse range of events, including weddings, conferences, and more, Furthermore, as 
                    part of the initiative, five affordable housing units have been added to the property.
                </p>
            </div>
            <div class="Image">
                <img src="https://bcginc.wpenginepowered.com/wp-content/uploads/2023/02/DJI_0353-HDR-scaled-600x400.jpg" alt="Cheeca Lodge and Spa">
            </div>
        </div>
        
    </div>
</div>
<img class="img1" src="https://bcginc.wpenginepowered.com/wp-content/uploads/2023/03/DJI_0382-HDR-scaled-600x400.jpg" alt="Cheeca from behind">

<img class="img2" src="https://bcginc.wpenginepowered.com/wp-content/uploads/2023/03/5D589518-D366-45EF-861D-A82BED00DC17-scaled-600x400.jpg" alt="Inside Cheeca">

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
        padding: 5rem;
        flex-wrap: calc(100vw/3);
        gap: 5px;
    }
    .Text{
        width: auto;
        margin: 0 auto;
        font-size: 20px;
        padding-left: 50px;
        display: block;
        position: relative;
    }
    .Row1{
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        width: 100rem;
        padding: 5rem;
        flex-wrap: calc(100vw/3);
        gap: 50px;
    }
    img{
        left:50px;
    }

</style>