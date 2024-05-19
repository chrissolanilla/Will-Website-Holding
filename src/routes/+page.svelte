<script>
    import Navbar from "$lib/components/Nav.svelte"
    import About from "$lib/components/About.svelte"
    import Approach from "$lib/components/Approach.svelte"
    import CoreValues from "$lib/components/CoreValues.svelte"
    import TargetMarkets from "$lib/components/TargetMarkets.svelte"
    import Team from "$lib/components/Team.svelte"
    import Contact from "$lib/components/Contact.svelte"
</script>

<div class = "StartContainer">
    <div class = "bgImg">
        <img src = "starBG.jpg" alt = "background"/>
    </div>
    <Navbar />
    <div class="contentMain">

        <h1>Welcome to Bill Website</h1>
        <p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
    </div>
</div>

<div class="wrapper">
    <div id="About"><About /></div>
</div>

<div class = "bgImg2">
    <img src = "starBG.jpg" alt = "background"/>
    <div class="wrapper">
        <div id="Approach"><Approach /></div>
    </div>
</div>
    
<div class="wrapper core">
    <div id="Values"><CoreValues /></div>
</div>
<div class="wrapper">
    <div id="Target"><TargetMarkets /></div>

</div>
<div class="wrapper">
    <div id="Team"><Team /></div>

</div>
<div class="wrapper">
    <div id="Contact"><Contact /></div>

</div>


<style>
     :global(body) {
        margin: 0;
        padding: 0;
     }
    div {
        overflow-x: hidden;
       
    }
    .StartContainer {
        color: white;
        width: 100%;
        height: 400px;
        
    }
    .StartContainer img{
        width: 100%;
        height: 400px;
        position: absolute;
        z-index: -1;
    }
    .contentMain {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        
    }
    .wrapper {
        display: flex;
        flex-direction: row;
        justify-content: center;
        width: 100%;
        padding: 0 20px;
    }   
    #Approach {
        width: 100rem;
    }
    .bgImg2 img{
        width: 100%;
        height: 45rem;
        position: absolute;
        z-index: -1;
    }
    .core {
        background-color: rgb(135, 184, 188);
        width: auto;
    }

    @media (max-width: 900px) {
        .bgImg2 img {
            width: 100%;
            height: 1650px
        }
    }
</style>