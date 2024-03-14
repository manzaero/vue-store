<template>
    <div class="relative bg-white cursor-pointer p-8 border border-slate-400 rounded-3xl transition hover:-translate-y-2 hover:shadow-2xl">
      <img
          class="absolute top-8 left-8"
          :src="!isFavorite ? '/like-1.svg' : '/like-2.svg'" alt="Like 1"
          @click="onCLickFavorite"/>
      <img :src="imageUrl" alt="Sneakers">
      <p class="mt-2">{{ title }}</p>
      <div class="flex justify-between mt-5">
        <div class="flex flex-col">
          <span class="text-slate-400">Цена: </span>
          <b> {{ price }} руб.</b>
        </div>

        <img @click="onClickAdd" :src="!isAdded ? '/plus.svg' : '/checked.svg'" alt="Plus">
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