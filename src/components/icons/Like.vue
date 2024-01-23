<template>
    <button>
        <i :class="{'text-green-500' : like==true}" class="fa-solid fa-heart"></i>
    </button>
</template>
<script setup>
    defineProps({
        like: Boolean,
    })
</script>