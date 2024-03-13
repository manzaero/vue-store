<template>

  <header class="flex justify-between border-b border-slate-200 px-10 py-8">
    <div class="flex items-center gap-4">
      <img src="/logo.png" alt="Logo" class="w-10">
      <div>
        <h2 class="text-xl font-bold uppercase">Sneakers</h2>
        <p class="text-slate-400">Магазин лучших кроссовок</p>
      </div>
    </div>

    <ul class="flex items-center gap-5">
      <li class="flex items-center gap-3 text-slate-500 hover:text-black cursor-pointer">
        <img src="/cart.svg" alt="Cart">
        <b class="ease-in-out duration-500">1205 руб.</b>
      </li>
      <li class="flex items-center gap-3 text-slate-500 hover:text-black cursor-pointer">
        <img src="/heart.svg" alt="Favorites">
        <p class="ease-in-out duration-500">Закладки</p>
      </li>
      <li class="flex items-center gap-3 text-slate-500 hover:text-black cursor-pointer">
        <img src="/profile.svg" alt="Profile">
        <p class="ease-in-out duration-500">Профиль</p>
      </li>
    </ul>
  </header>

</template>
