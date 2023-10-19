<script lang="ts">
  import Router from 'svelte-spa-router'
  import {item, cart, index} from './pages'
  import {Card, Header} from './lib'

  const routes = {
    '/': index,
    '/cart': cart,
    '/item/:id': item,
  }
</script>

<main class="flex flex-col">
  <Header/>
  <Router {routes}/>
</main>

<style>

</style>
