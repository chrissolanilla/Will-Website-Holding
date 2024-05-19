<div class="ValuesContainer">
    <div class="ValuesText">
        <h1>Core Values</h1>
        <p>
            Our values represent the core of our essence as a real estate investment 
            firm and provide the framework for our daily and long term relationships. 
            Through collaboration and thoughtful diligence, we are able to perform 
            seamless executions of investments from start to finish. Our integrity is 
            of the utmost importance as a fiduciary agent, and our family office 
            approach provides the disciplined agility necessary to identify emerging market trends.
        </p>
    </div>
    
    <div class="CoreValuesImg">
        <img src="coreValue.png" alt="We pride ourselves on the core values of Gooning, Edging, and Jelqing">
    </div>
</div>

<style>
    .ValuesContainer{
        background-color:rgb(135, 184, 188);
        width: 100rem;
        display: flex;
        flex-direction: row-reverse;
        justify-content: center;
        align-items: center;
        gap: 20px;
        flex-wrap: calc(100vw/3);
        box-sizing: border-box;
        padding: 120px 0px 100px 0px;
    }
    
    .CoreValuesImg, .ValuesText {
        flex: 1; /* Makes both divs take equal space */
    }

    .ValuesText {
        color: white;
        font-size: 20px;
        padding-left: 20px; /* Adjusted padding */
    }
    @media (max-width: 900px) {
        .ValuesContainer {
            flex-direction: column; /* Stacks the items vertically on smaller screens */
            padding: 1rem; /* Further reduce padding */
            width: 20rem;
        }
        .ValuesText {
            padding-left: 0; /* Remove left padding on small screens */
        }
        img {
            height: 250px;
        }
    }
</style>