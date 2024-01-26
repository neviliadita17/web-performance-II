<template>
    <NuxtImg 
        v-memo="[]"
        :alt="anime.title"
        format="avif"
        :src="anime.images.webp.image_url" 
        width="200px"
        height="300px"/>

        <div class="text-sm px-1 py-2">{{ anime.title }}</div>
</template>

<script>
export default {
    props: {
        anime: {
            type: Object,
            required: true
        }
    }
}
</script>