<script>
    import {location,push} from "svelte-spa-router";
    import SvgIcon from '@jamescoyle/svelte-icon';
    import {mdiBorderAll,mdiBorderAllVariant} from "@mdi/js";
</script>

<nav class="navbar navbar-expand-lg bg-body-tertiary">
    <div class="container-fluid">
        <a class="navbar-brand" href="#">Miodywambierzyce</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                <li class="nav-item">
                    <a class="nav-link active" aria-current="page" on:click={() => {push('/')} }>Strona główna</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" on:click={()=> {push('/produkty')}}>Produkty</a>
                </li>
            </ul>
        </div>
    </div>
</nav>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400..700&display=swap');
    .navbar-brand{
        font-family: "Dancing Script", cursive;
        font-size: 40px;
    }
    .navbar-nav a:hover{
        color: orange;
    }
</style>