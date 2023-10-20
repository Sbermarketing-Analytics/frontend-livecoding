<script>
  import {push, pop, replace} from 'svelte-spa-router'
  import { ShoppingCart } from "svelte-heros-v2";

  export let id = 1
</script>

<div class="w-48 h-64 shadow-md border-2 rounded-xl flex flex-col items-center cursor-pointer m-2 pt-4"
  on:click={() => push(`/item/${id}`)}
>
  <img src="/images/avokado.png" class="h-24" />
  <p>Avokado</p>
  <p class="text-green-900">120₽</p>
  <div class="w-full flex justify-evenly mt-2">
    <button class="px-2 py-0 text-white bg-red-400">-</button>
    <span>1</span>
    <button class="px-2 py-0 text-white bg-green-400">+</button>
  </div>
  <button
    on:click={() => push(`/cart`)}
    class="flex gap-1 bg-green-400 text-white px-2 py-1 rounded-md mt-2 cursor-pointer hover:text-white"
    href="/#/cart"><ShoppingCart />В корзину</button
  >
</div>
