<template>
  <div class="relative h-screen flex text-white">
    <!-- Barre latérale -->
    <div class="w-[13%] px-5 py-6 bg-black text-gray-400">
      <div class="flex">
        <img class="w-8" src="/images/logo.svg" alt="Spotiwind">
        <h1 class="text-white text-2xl ml-2 font-semibold">Spotiwind</h1>
      </div>
      <div class="mt-10 font-medium">
        <button class="mb-4 hover:text-white transition duration-300"><i class="fa-solid fa-house mr-5"></i> Accueil</button>
        <button class="mb-4 hover:text-white transition duration-300"><i class="fa-solid fa-magnifying-glass mr-5"></i> Rechercher</button>
        <button class="mb-4 hover:text-white transition duration-300"><i class="fa-solid fa-table-list mr-5"></i> Bibliothèque</button>
      </div>
      <div class="mt-10 font-medium">
        <button class="mb-4 hover:text-white transition duration-300"><i class="fa-solid fa-square-plus mr-5"></i> Créer une playlist</button>
        <button class="mb-4 hover:text-white transition duration-300"><i class="fa-solid fa-heart text-rose-400 mr-5"></i> Titres likés</button>
      </div>
      <hr class="mt-5 border-gray-700">
    </div>
    <!-- Contenu -->
    <div class="w-[87%] px-3 py-2 bg-neutral-900">Content</div>
    <!-- Barre de lecture -->
    <div class="absolute bottom-0 bg-neutral-900 w-full h-16 border-t border-neutral-800">Play bar</div>
  </div>
</template>