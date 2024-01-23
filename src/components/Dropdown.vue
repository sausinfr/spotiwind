<template>
    <div class="absolute z-10 w-56 bg-neutral-700 flex flex-col text-sm rounded p-1 shadow-md">
        <button v-for="item in items" class="group relative text-left p-2 hover:bg-neutral-600 rounded">
            <div class="flex justify-between items-center">
                <span>{{ item.title }}</span>
                <CaretRight v-if="item.icon == 'CaretRight'"></CaretRight>
            </div>
            <div class="absolute left-[100%] top-0 hidden group-hover:block">
                <Dropdown v-if="item.items != null" :items="item.items"></Dropdown>
            </div>
        </button>
    </div>
</template>
<script setup>
import CaretRight from './icons/CaretRight.vue';
defineProps({
    items: Array,
})
</script>