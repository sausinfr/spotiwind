<template>
  <div class="min-w-[768px] relative h-screen flex text-white">
    <!-- BARRE LATERALE -->
    <div class="w-[25%] px-5 py-6 bg-black text-gray-400 lg:w-[22%] xl:w-[18%] 2xl:w-[13%]">
      <div class="flex">
        <img class="w-8" src="/images/logo.svg" alt="Spotiwind">
        <h1 class="text-white text-2xl ml-2 font-semibold">Spotiwind</h1>
      </div>
      <div class="mt-10 font-medium flex flex-col items-start">
        <button class="mb-4 hover:text-white transition duration-300"><i class="fa-solid fa-house mr-5"></i> Accueil</button>
        <button class="mb-4 hover:text-white transition duration-300"><i class="fa-solid fa-magnifying-glass mr-5"></i> Rechercher</button>
        <button class="mb-4 hover:text-white transition duration-300"><i class="fa-solid fa-table-list mr-5"></i> Bibliothèque</button>
      </div>
      <div class="mt-10 font-medium flex flex-col items-start">
        <button class="mb-4 hover:text-white transition duration-300"><i class="fa-solid fa-square-plus mr-5"></i> Créer une playlist</button>
        <button class="mb-4 hover:text-white transition duration-300"><i class="fa-solid fa-heart text-rose-400 mr-5"></i> Titres likés</button>
      </div>
      <hr class="mt-5 border-gray-700">
    </div>
    <!-- CONTENU -->
    <Home></Home>
    <!-- BARRE DE LECTURE -->
    <div class="absolute bottom-0 bg-neutral-900 w-full h-24 border-t border-neutral-800">
      <div class="flex px-5 h-full justify-between">
        <!-- Artiste et titre la chanson -->
        <div class="flex items-center gap-x-5">
          <div>
            <img src="/images/thumb-stardust.jpg" alt="Stardust">
          </div>
          <div>
            <p class="text-sm"><a class="hover:underline" href="#">Bullet to My Heart</a></p>
            <p class="text-xs text-neutral-500"><a class="hover:underline" href="#">Stardust</a></p>
          </div>
          <div>
            <Like :like="true"></Like>
          </div>
        </div>
        <!-- Contrôles du lecteur -->
        <div class="w-2/5 flex flex-col justify-center">
          <div class="flex justify-center gap-x-6">
            <button class="text-xl text-neutral-500 hover:text-white transition duration-300"><i class="fa-solid fa-shuffle"></i></button>
            <button class="text-xl text-neutral-500 hover:text-white transition duration-300"><i class="fa-solid fa-backward-step"></i></button>
            <button class="text-3xl"><i class="fa-solid fa-circle-play"></i></button>
            <button class="text-xl text-neutral-500 hover:text-white transition duration-300"><i class="fa-solid fa-forward-step"></i></button>
            <button class="text-xl text-neutral-500 hover:text-white transition duration-300"><i class="fa-solid fa-repeat"></i></button>    
          </div>
          <div class="text-xs text-neutral-500 flex items-center gap-x-2 mt-1">
            <div>2:20</div>
            <div class="group w-full h-1 bg-neutral-500 rounded">
              <div class="relative bg-white group-hover:bg-green-500 w-1/2 h-1 rounded">
                <div class="absolute hidden group-hover:block right-0 -bottom-full -top-full w-3 h-3 bg-white rounded-full"></div>
              </div>
            </div>
            <div>4:40</div>
          </div>
        </div>
        <!-- Contrôles supplémentaires -->
        <div class="flex items-center gap-x-4">
          <button class="text-xl text-neutral-500 hover:text-white transition duration-300"><i class="fa-solid fa-play"></i></button>
          <button class="text-xl text-neutral-500 hover:text-white transition duration-300"><i class="fa-solid fa-microphone-lines"></i></button>
          <button class="text-xl text-neutral-500 hover:text-white transition duration-300"><i class="fa-solid fa-list-check"></i></button>
          <button class="text-xl text-neutral-500 hover:text-white transition duration-300"><i class="fa-solid fa-computer"></i></button>
          <div class="group w-24 flex items-center gap-x-2">
            <button class="text-xl text-neutral-500 group-hover:text-white transition duration-300"><i class="fa-solid fa-volume-high"></i></button>
            <div class="group w-full h-1 bg-neutral-500 rounded">
              <div class="relative bg-white group-hover:bg-green-500 w-2/3 h-1 rounded">
                <div class="absolute hidden group-hover:block right-0 -bottom-full -top-full w-3 h-3 bg-white rounded-full"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
import Home from './components/pages/Home.vue';
import Like from './components/icons/Like.vue';
</script>