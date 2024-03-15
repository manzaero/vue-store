<script setup>
import TheHeader from "@/components/TheHeader.vue";
import TheCardList from "@/components/TheCardList.vue";
import TheDrawer from "@/components/TheDrawer.vue";
import {onMounted, ref} from "vue";
import axios from "axios";

const items = ref([])
onMounted(async() => {
  try {
    const {data} = await axios
        .get('https://f1d654f1728ec1d0.mokky.dev/items')
    items.value = data
  } catch (e) {
    console.log(e.message)
  }
})
</script>

<template>
<!--  <the-drawer/>-->
  <div class="bg-white w-4/5 m-auto bg-white rounded-xl shadow-xl mt-14">

    <the-header/>

    <div class="p-10">
      <div class="flex justify-between items-center">
        <h2 class="text-3xl font-bold mb-8">Все кроссовки</h2>

        <div class="flex justify-between gap-4">
          <select class="rounded-md py-2 px-3 border outline-none">
            <option>По названию</option>
            <option>Сначала дешёвые</option>
            <option>Сначала дорогие</option>
          </select>

          <div class="relative">
            <img class="absolute left-3 top-3" src="/search.svg" alt="">
            <input
                placeholder="Поиск"
                class="border rounded-md py-2 pl-10 pr-4 outline-none focus:border-gray-400">
          </div>
        </div>
      </div>

      <div class="mt-10">
        <the-card-list :items="items"/>
      </div>
    </div>
  </div>
</template>

<style scoped>
</style>
