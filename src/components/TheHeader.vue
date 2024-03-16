<template>

  <header class="flex justify-between border-b border-slate-200 px-10 py-8 md:py-4 md:text-xs md:-mt-8 md:-pl-2 md:px-4">
    <div class="flex items-center gap-4">
      <img src="/logo.png" alt="Logo" class="w-10 md:w-6 md:hidden ">
      <div>
        <h2 class="text-xl font-bold uppercase md:text-xs">Sneakers</h2>
        <p class="text-slate-400 lg:hidden">Магазин лучших кроссовок</p>
      </div>
    </div>

    <ul class="flex items-center gap-5">
      <li class="flex items-center gap-3 text-slate-500 hover:text-black cursor-pointer">
        <img src="/cart.svg" alt="Cart">
        <p class="ease-in-out font-bold duration-500 sm:hidden">1205 руб.</p>
      </li>
      <li class="flex items-center gap-3 text-slate-500 hover:text-black cursor-pointer">
        <img src="/heart.svg" alt="Favorites">
        <p class="ease-in-out duration-500 sm:hidden">Закладки</p>
      </li>
      <li class="flex items-center gap-3 text-slate-500 hover:text-black cursor-pointer">
        <img src="/profile.svg" alt="Profile">
        <p class="ease-in-out duration-500 sm:hidden">Профиль</p>
      </li>
    </ul>
  </header>

</template>
