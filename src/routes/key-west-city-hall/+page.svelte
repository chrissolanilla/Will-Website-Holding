<script>
    import Navbar from "$lib/components/Nav.svelte";
    import Contact from "$lib/components/Contact.svelte";
</script>

<div class="Navbar">
    <Navbar />
</div>

<div class="PageContainer">
    <div class="TitleContainer">
        <h1>Key West City Hall</h1>
    </div>

    <div class="BodyContainer">
        <div class="Row1">
            <div class="Text">
                <div>
                    Location: Key West, Florida
                </div>
                <div>
                    <p>Completion Date: December 2016</p>
                </div>
                <p>
                    Description: This project featured the conversion of Archer Elementary School into the new City Hall for Key
                    West, Florida. The building was designed as a completely new structure within the historic outer walls of
                    the 1920s building. The historic Auditorium now serves as the Commission Chamber for the City of Key West,
                    with the other areas serving as office spaces for the City's many departments.
                </p>
                <p>
                    Many of the building's original elements were reused within the building, including seating from the historic
                    Auditorium, trusses from the original roof structure, and historic metal windows. In addition, all of the
                    heart pine wood from the original structure was reclaimed for use in the building or in other buildings in
                    town.
                </p>
                <p>
                    This project is LEED Platinum and features solar array panels, rainwater cisterns, advanced communications
                    systems, security, and eco-friendly site amenities. The City Hall was also awarded USGBC's “Most Outstanding”
                    project in 2018.
                </p>
            </div>
            <div class="Image">
                <img src="https://bcginc.wpenginepowered.com/wp-content/uploads/2020/03/MAIN-KEY-WEST-CITY-HALL-PIC-600x400.png" alt="Key West City Hall">
            </div>
        </div>

        <div class="Row2">
            <img class="img1" src="https://bcginc.wpenginepowered.com/wp-content/uploads/2020/04/KWCH_4-scaled-600x400.jpg" alt="Key West City Hall">

            <img class="img2" src="https://bcginc.wpenginepowered.com/wp-content/uploads/2020/04/KWCH_3-600x400.jpg" alt="Key West City Hall">

        </div>

    </div>
</div>

<div class="wrapper contact">
	<div id="Contact"><Contact /></div>
</div>


<style>
    .Navbar{
        background-color: white;
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
