<template>
  <div class="fixed top-0 left-0 h-full w-full bg-black z-10 opacity-70"></div>
  <div class="bg-white w-1/5 h-full fixed right-0 top-0 z-20 p-6">
    <the-drawer-head/>
    <the-cart-item/>
  </div>

</template>

<script setup>
import TheDrawerHead from "@/components/TheDrawerHead.vue";
import TheCartItem from "@/components/TheCartItem.vue";
</script>