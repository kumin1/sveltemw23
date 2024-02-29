<script>
  import {setContext, getContext} from "svelte";
  import {writable} from "svelte/store";
  import * as bootstrap from 'bootstrap';
  import Router, {location, link, push, pop} from "svelte-spa-router";

  import Strona2 from "./produkty.svelte";
  import Index from "./index.svelte";
  import Menu from "./menu.svelte";
  import produkty from "./produkty.svelte";
  import produkt from "./produkt.svelte";
  let imie = "Czesław";

  let strony = {
    '/': Index,
    '/produkty': produkty,
    '/produkty/:id': produkt,

    '*': Index,
  }
</script>

<main>
  <Menu />
  <Router routes={strony} />
</main>