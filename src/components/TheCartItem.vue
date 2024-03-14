<template>
  <div class="border-sky-100 border p-4 rounded-xl flex gap-4 items-center">
    <img class="w-16 h-16" src="/sneakers/sneakers-1.jpg" alt="Sneakers">
    <div class="flex flex-col">
      <p>Кроссовки Nike Air Max 270</p>
      <div class="flex justify-between mt-2">
        <b>12990 руб.</b>
        <img class="opacity-40 hover:opacity-100 cursor-pointer transition" @click="console.log(111)" src="/close.svg" alt="">
      </div>
    </div>
  </div>
</template>