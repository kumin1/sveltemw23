<script>
    import SvgIcon from '@jamescoyle/svelte-icon';
    import {mdiBorderAll,mdiBorderAllVariant} from "@mdi/js";
    import {location,link} from "svelte-spa-router";
    import Button from "bootstrap/js/src/button.js";
    let price = 100;
    let sort = "grid";
/*
    function oneproduct(){
        let icon1 = document.getElementById('icon1')
        let icon2 = document.getElementById('icon2')
        icon1.style.border = '1px black solid';
        icon2.style.border = 'none';
    }
    function multiproduct(){
        let icon1 = document.getElementById('icon1')
        let icon2 = document.getElementById('icon2')
        icon2.style.border = '1px black solid';
        icon1.style.border = 'none';
    }
*/
</script>

<header class="text-center header">
    Produkty
</header>
<div class="icons">
    <div>
        <button id="icon1" class="{sort === 'list' ? 'border_black' : 'border_none'}" on:click={ ()=>{ sort = "list"} }>
        <label for="icon1"><SvgIcon class="icon" type="mdi" path="{mdiBorderAllVariant}"></SvgIcon></label>
        </button>
        <button id="icon2" class="{sort === 'grid' ? 'border_black' : 'border_none' }" on:click={ ()=>{sort = "grid"} }>
        <label for="icon2"><SvgIcon class="icon" type="mdi" path="{mdiBorderAll}"></SvgIcon></label>
        </button>
    </div>
    <div class="sorting-container">
        <select>
            <option class="option" value="domyslne">Domyślne</option>
            <option class="option" value="Od najwyższej">Od Najwyższej</option>
            <option class="option" value="Od najniższej">Od Najniższej</option>
            <option class="option" value="Nazwa Od A do Z">Nazwa Od A do Z</option>
            <option class="option" value="Nazwa Od Z do A">Nazwa Od Z do A</option>
        </select>
    </div>
</div>


<div class="{sort === 'list' ? 'product-container-list' : 'product-container-grid'}">
    <div class="product">
        <a href="#/produkty/1" class="link">
        <img alt="product-image" src="/src/images/product.png">
        <p class="product-name">Miód Rzepakowy</p>
        <p class="displayed-price">{price}zł</p>
        </a>
        <div class="product-buttons">
            <label for="1"><input type="radio" name="1" value="30zl" id="1" checked>400g</label>
            <label for="1"><input type="radio" name="1" value="50zl" id="2" >800g</label>
            <label for="1"><input type="radio" name="1" value="80zl" id="3" >1200g</label>
        </div>
        <p class="produce-description">lorem ipsum lorem ipsum lorem ipsum lorem ipsum </p>
    </div>

    <div class="product">
        <a href="#" class="link">
        <img alt="product-image" src="/src/images/product.png">
        <p class="product-name">Miód Rzepakowy</p>
        <p class="displayed-price">{price}zł</p>
        </a>
        <div class="product-buttons">
            <label for="2"><input type="radio" name="2" value="30zl" id="4" >400g</label>
            <label for="2"><input type="radio" name="2" value="40zl" id="5" checked>800g</label>
            <label for="2"><input type="radio" name="2" value="60zl" id="6" >1200g</label>
        </div>
        <p class="produce-description">lorem ipsum lorem ipsum lorem ipsum lorem ipsum </p>
    </div>

    <div class="product">
        <a href="#" class="link">
        <img alt="product-image" src="/src/images/product.png">
        <p class="product-name">Miód Rzepakowy</p>
        <p class="displayed-price">{price}zł</p>
        </a>
        <div class="product-buttons">
            <label for="3"><input type="radio" name="3" value="30zl" id="7" >400g</label>
            <label for="3"><input type="radio" name="3" value="40zl" id="8" checked>800g</label>
            <label for="3"><input type="radio" name="3" value="60zl" id="9" >1200g</label>
        </div>
        <p class="produce-description">lorem ipsum lorem ipsum lorem ipsum lorem ipsum </p>

    </div>

    <div class="product">
        <a href="#" class="link">
        <img alt="product-image" src="/src/images/product.png">
        <p class="product-name">Miód Rzepakowy</p>
        <p class="displayed-price">{price}zł</p>
        </a>
        <div class="product-buttons">
            <label for="4"><input type="radio" name="4" value="30zl" id="10" >400g</label>
            <label for="4"><input type="radio" name="4" value="40zl" id="11" checked>800g</label>
            <label for="4"><input type="radio" name="4" value="60zl" id="12" >1200g</label>
        </div>
        <p class="produce-description">lorem ipsum lorem ipsum lorem ipsum lorem ipsum </p>
    </div>

</div>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Ubuntu:ital,wght@0,300;0,400;0,500;0,700;1,300;1,400;1,500;1,700&display=swap');
    .border_none {
        border: 1px solid transparent;
        background-color: white;
    }
    .border_black {
        border: 1px solid black;
        background-color: rgb(211, 211, 211);
    }
    input[type="radio"]{
        display: none;
    }
    .header{
        font-size: 30px;
    }
    .icons{
        width: 400px;
        justify-content: space-around;
        display: flex;
        height: fit-content;
        border-radius: 15px;
        margin-left: auto;
        margin-right: auto;
        vertical-align: center;
    }
    .icons button{
        border-radius: 15px;
    }
    .icons label{
        padding: 6px 4px;
    }
    .icons button:hover{
        border: black 1px solid;
    }
    .sorting-container{
        margin-top: auto;
        margin-bottom: auto;
    }
    .sorting-container select{
        display: block;
        border: none;
        appearance: none;
        text-align: left;
    }
    .product-container-list{
        display: flex;
        flex-wrap: wrap;
        align-items: flex-start;
        max-width: 500px;
        margin-top: 30px;
        margin-left: auto;
        margin-right: auto;
    }
    .product-container-grid{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr;
        max-width: 1628px;
        gap: 20px;
        padding: 25px;
        margin-left: auto;
        margin-right: auto;
    }
    .product{
        display: flex;
        flex-direction: column;
        text-align: center;
        width: 100%;
        border-radius: 25px;
        min-height: 450px;
        max-height: 450px;
        transition: 0.5s;
        margin-top: 30px;
    }
    .product:hover{
        transform: scale(1.05);
        box-shadow: 0 0 10px 5px rgba(0, 0, 0, 0.3);
        transition: transform 0.5s, box-shadow 0.5s;
    }
    .product img{
        width: fit-content;
        margin-top: 20px;
        margin-left: auto;
        margin-right: auto;
    }
    .product-buttons{
        display: flex;
        flex-wrap: wrap;
        margin: 10px auto;
    }
    .product-buttons label{

        margin-right: 5px;
        margin-left: 5px;
        padding: 5px 10px;
        border-radius: 10px;
        border: 1px solid transparent;
    }
    .product-buttons label:hover{
        border: 1px solid black;
    }
    input[type="radio"]:checked + label{
        border: 2px solid black;
    }
    .produce-description{
        margin-left: 20px;
        margin-right: 20px;
    }
    .displayed-price{
        font-size: 20px;
        font-weight: bold;
        margin-bottom: 5px;
    }
    .product-name{
        font-size: 24px;
        font-family: "Ubuntu", sans-serif;
    }
    .link{
        text-decoration: none;
        color: inherit;
    }
</style>