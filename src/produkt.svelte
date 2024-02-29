<script>
    import {location,push} from "svelte-spa-router";
    export let params = {};
</script>

<h1>PRODUKT 1</h1>
<h3>{params.id}</h3>