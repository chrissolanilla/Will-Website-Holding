<div class="ContactContainer">
    <div class="ContactTitle">
        <h1>Contact us</h1>
        <div class="ContactBody">
            <div class="Address">
                10145 NW 19th Street Doral, FL 33172
            </div>
            <div class="Phone">
                <b>Phone:</b>
                866-88-BURKE
            </div>
            <div class="Fax">
                <b>Fax:</b>
                (305) 468-6654
            </div>
            <div class="Email">
                <b>Email:</b>
                <a href="mailto:info@bcginc.net" style="color:wheat">info@bcginc.net</a>
            </div>
        </div>
    </div>
    <div class="icons">
		<a href="https://www.linkedin.com/company/burkeconstructiongroup">
			<i class="fa fa-linkedin" aria-hidden="true"></i>
		</a>
		<a href="https://www.instagram.com/burkeconstructiongroup"> 
			<i class="fa fa-instagram" aria-hidden="true"></i>
		</a>
		<a href="https://www.facebook.com/BurkeConstructionGroupInc/">
			<i class="fa fa-facebook" aria-hidden="true"></i>
		</a>
		<a href="https://www.youtube.com/channel/UCvopoFV385wOPjFQPDb6k5A">
			<i class="fa fa-youtube" aria-hidden="true"></i>
		</a>
	</div>
</div>


<style>
    .ContactContainer {
        width: 100%;
        max-width: 100rem;
        height: auto;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        column-gap: 5rem;
        padding: 2rem 1rem;
        color: white;
        background-color: black;
    }

    .ContactTitle h1 {
        margin-bottom: 1rem;
    }

    .ContactBody {
        display: flex;
        flex-direction: column;
        gap: 5px;
    }

    .icons {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        gap: 1rem;
    }

    i {
        padding: 0.4rem;
        color: white;
        font-size: 1.5rem;
    }

    /* Mobile Styles */
    @media (max-width: 900px) {
        .ContactContainer {
            flex-direction: column;
            align-items: center;
            text-align: center;
            padding: 1rem;
        }

        .ContactBody {
            align-items: center;
        }

        .icons {
            gap: 0.5rem;
            margin-top: 1rem;
        }

        i {
            font-size: 2rem;
        }
    }

</style>
