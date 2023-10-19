<script>
  import { ShoppingCart } from "svelte-heros-v2";
  import { push } from "svelte-spa-router";

  export let params = {};
</script>

<p>
  {JSON.stringify(params)}
</p>

<div class="m-auto flex flex-col w-4/6">
  <div class="flex w-full">
    <img src="/images/avokado.png" class="h-80" />
    <div class="font-bold flex flex-col justify-start items-start h-full">
      <p class="text-[60px] mt-4">Avokado</p>
      <p class="text-green-600 text-[50px]">120₽</p>
      <div class="w-full flex flex-col">
        <div class="w-full flex justify-between my-2">
          <button class="px-4 py-2 text-white bg-red-400">-</button>
          <span class="text-3xl">1</span>
          <button class="px-4 py-2 text-white bg-green-400">+</button>
        </div>
        <button
          on:click={() => push(`/cart`)}
          class="flex gap-1 bg-green-400 text-white mx-auto px-2 py-2 rounded-md mt-2 cursor-pointer hover:text-white w-full justify-center"
          ><ShoppingCart />В корзину</button
        >
      </div>
    </div>
  </div>
  <div>
    <p class="text-justify text-md">
      Разнообразный и богатый опыт начало повседневной работы по формированию
      позиции способствует подготовки и реализации существенных финансовых и
      административных условий. Не следует, однако забывать, что рамки и место
      обучения кадров играет важную роль в формировании соответствующий условий
      активизации. С другой стороны начало повседневной работы по формированию
      позиции требуют определения и уточнения форм развития. Не следует, однако
      забывать, что дальнейшее развитие различных форм деятельности позволяет
      выполнять важные задания по разработке соответствующий условий
      активизации. Повседневная практика показывает, что новая модель
      организационной деятельности обеспечивает широкому кругу (специалистов)
      участие в формировании направлений прогрессивного развития. Задача
      организации, в особенности же реализация намеченных плановых заданий
      представляет собой интересный эксперимент проверки дальнейших направлений
      развития.
    </p>
  </div>
</div>
