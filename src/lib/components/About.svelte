<div class="AboutContainer">
    <div class="AboutText">
        <h1>About</h1>
        
        <p> Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
            Proin eleifend sem eget felis bibendum maximus. Vestibulum ullamcorper eu quam vel lacinia. 
            Nunc imperdiet fermentum urna. Cras vitae condimentum enim. 
            Fusce urna est, cursus vehicula nisi sed, cursus rhoncus erat. Pellentesque sed suscipit ipsum, 
            sit amet efficitur dolor. Donec dictum eu ante ut sollicitudin. Maecenas lobortis vitae erat quis pellentesque. 
            Sed at augue quis est condimentum elementum in sed sem. Cras eu congue ligula. Nulla fermentum est id augue scelerisque, 
            at scelerisque nisl tincidunt.
        </p>
        
    </div>
    
    <div class="ImagesContainer">
        <div class="AboutImage">
            <img src="Poolside.jpg" alt="It's over. We're back. It's so over. We're so back">
        </div>
    
        <div class="StarImage">
            <img src="starLight.jpg" alt="Second pic on website">
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
        column-gap: 5rem;
        width: 100%;
        height: 400px;
    }
    .ImagesContainer {
        display: flex;
        flex-direction: row;
        justify-content: center;
        column-gap: 0.11rem;
        width: 100%;
        height: 400px;
    }
    .AboutImage img{
        height: 300px;
        
    }
    .StarImage img{
        height:300px;
    }

    .AboutText {
        color: black;
        width: auto;
        margin: 0 auto;
        font-size: 20px;
        padding-left: 50px;
        display: block;
        position: relative;
    }
</style>