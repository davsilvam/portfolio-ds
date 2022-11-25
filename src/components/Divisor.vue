<script setup>
    const props = defineProps(['src'])
</script>

<template>
    <section class="w-full">
        <img class="w-full" :src="props.src">
    </section>
</template>