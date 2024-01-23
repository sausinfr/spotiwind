<template>
  <div class="relative">
    <div @click="$event => showMenu = false" @contextmenu.prevent = "$event => showMenu = true" class="group p-4 bg-neutral-800 hover:bg-neutral-700 transition rounded cursor-pointer">
      <div class="relative">
        <div class="overflow-hidden" v-bind:class="{
          'rounded': shape == 'square',
          'rounded-full': shape !='square'
        }">
          <img class="w-full h-full object-cover" v-bind:src="image" v-bind:alt="title">
        </div>
        <button
          class="absolute right-2 bottom-2 translate-y-5 opacity-0 group-hover:translate-y-0 group-hover:opacity-100 transition duration-300 bg-green-500 w-12 h-12 rounded-full"><i
            class="fa-solid fa-play text-black text-xl pl-1"></i></button>
      </div>
      <div class="mt-4">
        <h3 class="font-semibold overflow-hidden text-ellipsis line-clamp-1">{{ title }}</h3>
        <p class="mt-1 text-neutral-500 text-xs overflow-hidden text-ellipsis line-clamp-2">{{ subTitle }}</p>
      </div>
    </div>
    <Dropdown v-if="showMenu" :style="`left: ${x}px; top:${y}px`" :items="[
      {
        title: 'Ajouter à la playlist',
        icon: 'CaretRight',
        items: [
          {
            title: 'Créer une playlist',
            icon: null,
            items: null
          },
          {
            title: 'Ma playlist 1',
            icon: null,
            items: null
          }
        ]
      },
      {
        title: 'Sauvegarder dans Titres Likés',
        icon: null,
        items: null
      },
      {
        title: 'Ajouter à la liste d\'attente',
        icon: null,
        items: null
      },
      {
        title: 'Accéder à l\'artiste',
        icon: null,
        items: null
      },
      {
        title: 'Partager',
        icon: 'CaretRight',
        items: [
          {
            title: 'Copier le lien vers l\'album',
            icon: null,
            items: null
          },
          {
            title: 'Intégrer l\'album',
            icon: null,
            items: null
          }
        ]
      }
    ]"></Dropdown>
  </div>
</template>
<script setup>
import { ref } from 'vue';
import Dropdown from './Dropdown.vue';
defineProps({
  title: String,
  subTitle: String,
  image: String,
  shape: String
})

const x = 180;
const y = 200;
const showMenu = ref(false);
</script>