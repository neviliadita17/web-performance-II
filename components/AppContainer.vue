<template>
    <div class="my-3 px-4">
        <div class="flex items-center justify-between">
            <div class="text-[24px]">{{ title }}</div>
            <input 
                type="text" 
                class="border rounded-md py-1 px-2" 
                placeholder="Search..."/>
        </div>
        <slot />
    </div>
    
</template>

<script>
export default {
    props: {
        title: {
            type: String,
            default: 'Page Title'
        }
    }
}
</script>