<script setup>
import TheCard from "@/components/TheCard.vue";

defineProps({
  items: Array
})

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
        :items="items"
        v-for="item in items"
        :key="item.id"
        :title="item.title"
        :price="item.price"
        :image-url="item.imageUrl"
        :is-added="false"
        :is-favorite="false"
        :on-click-add="onClickAdd"
        :on-c-lick-favorite="onclickFavorite"/>
  </div>
</template>