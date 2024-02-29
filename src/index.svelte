<script>
import SvgIcon from '@jamescoyle/svelte-icon';
import {mdiAccountKey} from '@mdi/js'
import {push} from "svelte-spa-router";
</script>

<header class="text-center header">Polecane</header>
<div class="polecane">
    <div class="polecane-item">
        <img alt="polecane-image" src="/src/images/product.png">
        <p>Miody</p>
    </div>
    <div class="polecane-item">
        <img alt="polecane-image" src="/src/images/product.png">
        <p>Miody</p>
    </div>
    <div class="polecane-item">
        <img alt="polecane-image" src="/src/images/product.png">
        <p>Miody</p>
    </div>
</div>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400..700&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
    .header{
        font-family: "Poppins", sans-serif;
        font-size: 40px;
    }
    .polecane{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        margin-left: auto;
        margin-right: auto;
        max-width: 1524px;
        padding: 15px;
        gap: 10px;
    }
    .polecane-item{
        display: flex;
        flex-direction: column;
        width: 100%;
        padding: 5px;
    }
    .polecane-item img{
        width: 100%;
        height: fit-content;
        border-radius: 15px;
        border: gray 1px solid;
        background-color: orange;
        transition: 0.5s;
    }
    .polecane-item img:hover{
        transform: scale(1.05);
        transition: 0.5s;
    }
    .polecane-item p {
        margin-top: 10px;
        text-align: center;
        font-family: "Poppins", sans-serif;
        font-size: 32px;
    }
</style>