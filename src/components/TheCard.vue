<template>
    <div class="relative bg-white cursor-pointer p-8 border border-slate-300 rounded-3xl transition hover:-translate-y-2 hover:shadow-2xl lg:p-6 md:p-4">
      <img
          class="absolute top-8 left-8 lg:top-6 lg:left-6 md:top-4 md:left-4"
          :src="!isFavorite ? '/like-1.svg' : '/like-2.svg'"
          alt="Like 1"
          @click="onCLickFavorite"/>
      <img :src="imageUrl" alt="Sneakers">
      <p class="mt-2 lg:text-sm md:text-xs">{{ title }}</p>
      <div class="flex justify-between mt-5 lg:mt-3 md:mt-2">
        <div class="flex flex-col">
          <span class="text-slate-400 lg :text-sm md:lg:text-xs">Цена: </span>
          <b class="lg:text-sm md:text-xs"> {{ price }} руб.</b>
        </div>

        <img
            @click="onClickAdd"
            :src="!isAdded ? '/plus.svg' : '/checked.svg'"
            alt="Plus">
      </div>
    </div>
</template>


<script setup>
defineProps({
  imageUrl: String,
  title: String,
  price: Number,
  isFavorite: Boolean,
  isAdded: Boolean,
  onClickAdd: Function,
  onCLickFavorite: Function
})
</script>