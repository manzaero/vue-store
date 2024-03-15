<template>
  <div class="fixed top-0 left-0 h-full w-full bg-black z-10 opacity-70"></div>
  <div class="bg-white w-1/5 h-full fixed right-0 top-0 z-20 p-6">
    <the-drawer-head/>


    <the-cart-item-list/>

    <div class="flex flex-col gap-4 mt-7">
      <div class="flex gap-2">
        <span>Итого: </span>
        <div class="flex-1 border-b border-dashed"></div>
        <b>12 9000 ₽</b>
      </div>

      <div class="flex gap-2">
        <span>Налог 5%: </span>
        <div class="flex-1 border-b border-dashed"></div>
        <b>1 074 ₽</b>
      </div>

      <button :disabled="true" class="cursor-pointer bg-lime-500 w-full rounded-xl py-3 text-white hover:bg-lime-600 active:bg-lime-700 transition disabled:bg-slate-400 mt-4">Оформить заказ</button>
    </div>
  </div>

</template>

<script setup>
import TheDrawerHead from "@/components/TheDrawerHead.vue";
import TheCartItemList from "@/components/TheCartItemList.vue";
</script>