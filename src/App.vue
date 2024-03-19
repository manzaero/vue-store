<script setup>
import TheHeader from "@/components/TheHeader.vue";
import TheCardList from "@/components/TheCardList.vue";
import TheDrawer from "@/components/TheDrawer.vue";
import {onMounted, ref, watch} from "vue";
import axios from "axios";

const items = ref([])
const sortBy = ref('')
const searchQuery = ref('')

const onChange = (event) => {
  sortBy.value = event.target.value
}

onMounted(async ()=> {
  try {
    const {data} = await axios.get('https://f1d654f1728ec1d0.mokky.dev/items')
    items.value = data
  } catch (e) {
    console.log(e)
  }
})

watch(sortBy, async () => {
  const {data} = await axios.get('https://f1d654f1728ec1d0.mokky.dev/items?sortBy=' + sortBy.value)
  items.value = data
})
</script>

<template>
<!--  <the-drawer/>-->
  <div class="bg-white w-4/5 m-auto bg-white rounded-xl shadow-xl mt-14">

    <the-header/>

    <div class="p-10 lg:p-8 md:p-4">
      <div class="flex justify-between items-center mb-8 md:mb-4 sm:mb-2">

        <h2 class="text-3xl font-bold lg:text-xl sm:text-xs">Все кроссовки</h2>

        <div class="flex justify-between gap-4 lg:gap-1">
          <select
              @change="onChange"
              class="rounded-md py-2 px-3 border outline-none bg-white lg:h-8 lg:py-0 lg:px-1 md:hidden">
            <option value="name">По названию</option>
            <option value="price">Сначала дешёвые</option>
            <option value="-price">Сначала дорогие</option>
          </select>
          {{sortBy}}
          <div class="relative sm:p-0">
            <img class="absolute left-3 top-3 lg:left-2 lg:top-2 sm:hidden" src="/search.svg" alt="">
            <input
                placeholder="Поиск"
                class="border rounded-md py-2 pl-10 pr-4 outline-none focus:border-gray-400 lg:h-8 lg:py-0 lg:pl-7 lg:pr-2 sm:max-w-20 sm:p-2 sm:text-sm"
                v-model="searchQuery">
            {{searchQuery}}
          </div>
        </div>
      </div>

      <div class="mt-10 lg:mt-8">
        <the-card-list :items="items"/>
      </div>
    </div>
  </div>
</template>

<style scoped>
</style>
