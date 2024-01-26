<template>
    <AppContainer title="Anime List">
        <div class="grid grid-cols-3 md:grid-cols-5 gap-x-3 gap-y-4 my-4">
            <div 
                v-for="(item, index) in items"
                :key="index"
                class="bg-gray-200">
                
                <LazyAnimeCard :anime="item" />
            </div>
        </div>
        
    </AppContainer>
</template>

<script>
export default {
    data() {
        return {
            items: {}
        }
    },

    mounted() {
        this.fetchAnimeList()
    },

    methods: {
        async fetchAnimeList() {
            const resp = await fetch('https://api.jikan.moe/v4/anime')
            const body = await resp.json()
            this.items = body.data
            console.log(resp)
        }
    }
}
</script>