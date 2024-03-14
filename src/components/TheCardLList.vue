<script setup>
import TheCard from "@/components/TheCard.vue";

const onClickAdd = () => {
  alert(111)
}

const onclickFavorite = () => {
  alert(222)
}
</script>

<template>
  <div class="grid grid-cols-4 gap-5">
    <the-card
        title="Мужские Кроссовки Nike Blazer Mid Suede"
        :price="12999"
        image-url="/sneakers/sneakers-1.jpg"
        :is-added="false"
        :is-favorite="false"
        :on-click-add="onClickAdd"
        :on-c-lick-favorite="onclickFavorite"/>
    <the-card/>
    <the-card/>
    <the-card/>
    <the-card/>
    <the-card/>
    <the-card/>
    <the-card/>
  </div>
</template>