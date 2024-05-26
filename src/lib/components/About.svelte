<div class="AboutContainer">
    <div class="AboutText">
        <h1>Our Mission</h1>
        
        <p> 
            Our mission is to cultivate generational wealth while fostering vibrant local communities, 
            guided by our commitment to supporting churches and empowering single mothers. Through 
            strategic investments and collaborative partnerships, we strive to build a sustainable 
            legacy of prosperity and compassion, ensuring that future generations thrive economically 
            and socially.
        </p>
        
    </div>
    
    <div class="ImagesContainer">
        <div class="AboutImage">
            <img src="Poolside.jpg" alt="It's over. We're back. It's so over. We're so back">
        </div>
    
        <div class="StarImage">
            <img src="DivineSavior.png" alt="Pic of Divine Savior Academy">
        </div>
    </div>

</div>

<style>
    .AboutContainer{
        color: white;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        width: 100rem;
        padding: 5rem;
        flex-wrap: calc(100vw/3);
        gap: 5px;
    }
    .ImagesContainer {
        display: flex;
        flex-direction: row;
        justify-content: center;
        column-gap: 0.11rem;
        width: 100%;
        height: 400px;
    }
    img {
        height: 300px;
    }

    .AboutText {
        font-size: 20px;
        color: black;
    }

    @media (max-width: 900px){
        .AboutContainer {
            width: 15rem;
            flex-direction: column;
            padding: 2px;
        }
        .ImagesContainer{
            flex-direction: column;
            padding: 2px;
            align-items: center;
        }
        img {
            height: 200px;
        }
       
    }
</style>