<template>
    <div class="w-[87%] bg-neutral-900 overflow-scroll">
        <!-- Top bar -->
        <div class="px-10 py-4 flex justify-between sticky top-0 z-20">
            <div class="text-2xl space-x-2">
                <button><i class="fa-solid fa-circle-chevron-left text-neutral-500"></i></button>
                <button><i class="fa-solid fa-circle-chevron-right text-neutral-500"></i></button>
            </div>
            <div class="space-x-4 flex items-center">
                <button class="px-4 py-1 bg-white rounded-full text-black text-sm font-semibold hover:scale-105">Découvrir
                    Premium</button>
                <button class="h-7 w-7 bg-neutral-700 rounded-full hover:scale-105"><i
                        class="fa-regular fa-bell"></i></button>
                <button class="h-7 w-7 rounded-full overflow-hidden hover:scale-105">
                    <img src="/images/avatar.jpg" alt="Avatar">
                </button>
            </div>
        </div>
        <div class="px-10 pt-10 pb-28">
            <div class="flex items-center justify-between">
                <h2 class="text-2xl font-semibold">Écoutés récemment</h2>
                <p class="font-semibold text-sm"><a href="#" class="text-neutral-400 hover:underline">Tout afficher</a></p>
            </div>
            <div class="mt-6 grid grid-rows-1 grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 2xl:grid-cols-7 gap-5">
                <Tile title="Def Leppard" sub-title="Artiste" image="/images/def-leppard.jpg"></Tile>
                <Tile title="One Desire" sub-title="Artiste" image="/images/one-desire.jpg"></Tile>
                <Tile title="Stardust" sub-title="Artiste" image="/images/stardust.jpg"></Tile>
                <Tile title="Highway To Heartbreak" sub-title="Stardust" image="/images/stardust-highway-to-heartbreak.jpg"
                    shape="square"></Tile>
                <Tile title="Bon Jovi" sub-title="Artiste" image="/images/bon-jovi.jpg"></Tile>
                <Tile title="Van Halen" sub-title="Artiste" image="/images/van-halen.jpg"></Tile>
                <Tile title="Whitesnake" sub-title="Artiste" image="/images/whitesnake.jpg"></Tile>
            </div>
            <div class="flex items-center justify-between mt-8">
                <h2 class="text-2xl font-semibold">Vos artistes préférés</h2>
                <p class="font-semibold text-sm"><a href="#" class="text-neutral-400 hover:underline">Tout afficher</a></p>
            </div>
            <div class="mt-6 grid grid-rows-1 grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 2xl:grid-cols-7 gap-5">
                <Tile title="Def Leppard" sub-title="Artiste" image="/images/def-leppard.jpg"></Tile>
                <Tile title="One Desire" sub-title="Artiste" image="/images/one-desire.jpg"></Tile>
                <Tile title="Stardust" sub-title="Artiste" image="/images/stardust.jpg"></Tile>
                <Tile title="Highway To Heartbreak" sub-title="Stardust" image="/images/stardust-highway-to-heartbreak.jpg"
                    shape="square"></Tile>
                <Tile title="Bon Jovi" sub-title="Artiste" image="/images/bon-jovi.jpg"></Tile>
                <Tile title="Van Halen" sub-title="Artiste" image="/images/van-halen.jpg"></Tile>
                <Tile title="Whitesnake" sub-title="Artiste" image="/images/whitesnake.jpg"></Tile>
            </div>
            <div class="flex items-center justify-between mt-8">
                <h2 class="text-2xl font-semibold">Réécoutez vos anciens favoris</h2>
                <p class="font-semibold text-sm"><a href="#" class="text-neutral-400 hover:underline">Tout afficher</a></p>
            </div>
            <div class="mt-6 grid grid-rows-1 grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 2xl:grid-cols-7 gap-5">
                <Tile title="Def Leppard" sub-title="Artiste" image="/images/def-leppard.jpg"></Tile>
                <Tile title="One Desire" sub-title="Artiste" image="/images/one-desire.jpg"></Tile>
                <Tile title="Stardust" sub-title="Artiste" image="/images/stardust.jpg"></Tile>
                <Tile title="Highway To Heartbreak" sub-title="Stardust" image="/images/stardust-highway-to-heartbreak.jpg"
                    shape="square"></Tile>
                <Tile title="Bon Jovi" sub-title="Artiste" image="/images/bon-jovi.jpg"></Tile>
                <Tile title="Van Halen" sub-title="Artiste" image="/images/van-halen.jpg"></Tile>
                <Tile title="Whitesnake" sub-title="Artiste" image="/images/whitesnake.jpg"></Tile>
            </div>
        </div>
    </div>
</template>
<script setup>
    import Tile from '../Tile.vue';
</script>